# Photo to Comic

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827.svg)](SKILL.md)

把一张照片重构成一页真正有分镜、有主题、有视觉母题的漫画。

Photo to Comic 是一个面向 Codex 的照片漫画化 Skill。它不会把同一张照片反复裁切，也不会只叠加“动漫滤镜”；它会先阅读照片中的人物、空间、动作、道具与情绪关系，再设计可信的新机位和相邻时刻，最终生成一张紧凑、完整上色的多格漫画页。

> Turn one photograph into an authored multi-panel comic page with source-grounded storytelling, camera invention, motif continuity, and a stable Painterly Comic Animation style.

## 它解决什么问题

常见的照片漫画化结果容易出现：

- 每格只是原图的远景、中景和近景裁切；
- 首格和末格内容重复；
- 多格从上到下堆叠成过长的条漫截图；
- 人物、服装、道具或环境跨格漂移；
- 关键道具在特写里反而结构不完整；
- 成图像淡彩线稿、半写实照片或混合画风。
- 提示里虽然写了 painterly，成图却仍是统一硬描边、光滑色块和两段式明暗的普通赛璐璐动漫。

Photo to Comic 把这些问题变成可检查的工作合同，而不是只依赖一段宽泛的提示词。

## 核心能力

- **自适应分格**：自动选择至少 3 格，只保留具有叙事增量的画面。
- **场景世界重建**：照片定义人物、空间和物件关系，但不锁死原相机。
- **有理由的新机位**：把平视、仰视、俯视、侧面、肩后、反打或物件视角当作候选；只有能增强叙事、美感或空间表达时才采用，不为了凑角度而换角度。
- **动作推演**：只创造照片证据能够支持的短时相邻动作，不凭空编造事件。
- **视觉母题系统**：从伞、鞋、倒影、草穗、电塔、背带或其他显著元素中选择主母题与次级母题。
- **道具完成度锁**：统一道具的数量、轮廓、构件、材质、接触方式和跨格细节层级。
- **紧凑漫画页**：默认生成准确竖版 `2:3` 多列拼页，而不是单列长图。
- **绘画动画漫画风格**：借鉴 painterly-frame 的抽象渲染方法，但只控制色彩、形面、笔触、材质和边缘；默认必须明显是手绘动画漫画，而不是干净赛璐璐动漫。主格约用 `5–9` 个大色形，小辅助格约用 `3–6` 个，保留三组明度、连接笔触、共享光照和断续/消失边缘，不锁源图构图、姿势、视线或比例。
- **材质绘画证据图**：按当前照片为天空、植物、皮肤、头发、衣料、道路、石材、金属等实际出现的材质分别规定笔触方向、形面、边缘与反光；至少在三种重要材质上能看出不同的手绘构造，而不是全图套同一油画纹理。
- **三尺度画风验收**：缩略图看不规则大形和边缘节奏，单格看连接笔触、形面与共享光照，局部看材质差异和非矢量完整轮廓；任一尺度仍像普通 clean cel anime 就判定默认画风失败。
- **显式平涂备用模式**：用户要求赛璐璐、硬边或不透明平涂时，切换为完整彩色 `Finished Luminous Cel Comic`，而不是让绘画笔触与平涂规则混杂。
- **双重质量检查**：分别检查照片连续性与漫画分镜创作是否成立。

## 默认输出

- 一张完整漫画页；
- 至少 3 格，常见为 3–8 格；
- 默认宽高比为竖版 `2:3`；
- 四格以上采用多列、嵌格或错落拼页；
- 默认无文字，避免乱码；
- 默认采用 `Painterly Comic Animation` 绘画动画漫画风格：大色形先行、三组明度、连接笔触、材质化局部笔触和丢失/找回边缘；提示开头先锁定“手绘动画漫画、非干净赛璐璐”，避免后续动漫脸或轮廓词把画风带偏；
- 用户明确要求赛璐璐/硬边平涂时，切换到 `Finished Luminous Cel Comic` 备用模式；
- 用户明确要求黑白、水彩、铅笔或其他媒介时，切换为对应的统一完成度规则。

## 工作流程

```text
一张照片
  → Source Story Card：区分事实、推断与不可改动锚点
  → Scene World Model：重建支持面、景深、邻接和可用机位
  → Camera Opportunity Map：判断换机位是否真的增加叙事、美感与可信度
  → Theme & State Change：确定主题与短时变化
  → Prop/Motif Bible：选择主导道具或视觉母题
  → Panel Difference Map：为每格分配镜头、动作和信息增量
  → Page/Colour Family Lock：冻结页形、时间天气与调色家族；逐格允许重组明度和局部曝光
  → Material Paint Proof Map：按源图材质指定可见的笔触、形面、边缘与反光证据
  → Painterly Render Contract：形面、连接笔触、共享光照、材质与边缘层级
  → Style Fingerprint + Completion Lock：冻结全页画风与完成度
  → 生成一张 2:3 多列漫画页
  → Source Continuity + Sequence Authorship 双质量门
```

## 安装

将仓库克隆到 Codex 的个人 Skills 目录：

```bash
git clone https://github.com/zcjunn/photo-to-comic.git "${CODEX_HOME:-$HOME/.codex}/skills/photo-to-comic"
```

重新载入 Codex 后即可自动触发，也可以显式调用：

```text
Use $photo-to-comic to turn this photo into a finished comic page.
```

## 使用示例

上传一张照片后，可以直接说：

```text
用 Photo to Comic 把这张照片生成一页漫画，分格数量根据内容决定。
```

```text
用 $photo-to-comic 重构这张照片，重点表现雨伞、倒影和人物与环境的关系。
```

```text
用 $photo-to-comic 做成黑白漫画页，保留人物、服装和场景关系。
```

也支持只输出完整制作方案而不生图，或审查已有漫画页的连续性、版式、道具和画风问题。

## 目录结构

```text
photo-to-comic/
├── SKILL.md                         # 入口、触发条件与核心合同
├── agents/openai.yaml              # Codex 界面名称与默认调用提示
├── evals/evals.json                # 45 个行为回归案例
└── references/
    ├── source-story-card.md         # 源照片证据、场景世界与连续性
    ├── style-research.md            # 风格研究、Style Fingerprint
    ├── painterly-comic-adapter.md  # painterly-frame 方法的漫画化适配
    ├── sequence-engine.md           # 自适应分格、机位与版式引擎
    ├── prompt-compiler.md           # 生产提示词编译和预检
    └── quality-gate.md              # 双质量门与定向修正规则
```

## 设计原则

1. 照片是事实锚点和故事种子，不是逐格复制的底图。
2. 连续性保护人物、物件和空间世界，而不是保护原始镜头。
3. 新镜头必须由照片可见的空间关系支持，并且带来叙事或美感收益；没有收益时可以不换机位。
4. 无论是否换机位，每格都必须改变信息、动作、焦点关系、景别、母题意义或画面结构，不能只是裁切。
5. 线条只在关键重叠、表情、接触和轮廓转折处断续出现；大色形、分组明度、形面、连接笔触和共享光照共同承担最终完成度，默认不允许完整均匀描边或光滑赛璐璐色带。
6. 跨格锁定身份比例、时间天气、调色家族、笔触场、材质语法与完成度；头轴、视线、表情、姿势、明度归属和局部曝光由每格分镜决定。
7. 参考流行漫画或 painterly-frame 方法时只提取通用视觉语言，不复制具体作者、角色、作品世界或页面。

## 隐私与参考图边界

- 用户提供的照片只用于当前漫画生成任务。
- 不进行反向搜图、公开上传或无关保存。
- 默认只把用户当前的源照片发送给图像生成工具。
- 风格参考仅用于抽象分析；除非用户明确授权，不作为额外生成输入。
- 仓库不包含示例用户照片或生成结果。

## 验证

可以使用 Codex 自带的 Skill 校验器检查结构：

```bash
python ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ~/.codex/skills/photo-to-comic
```

行为评测位于 [`evals/evals.json`](evals/evals.json)，共 45 个案例，覆盖最低三格、可选且有理由的多机位、零换机位但非裁切叙事、首尾去重、固定 2:3 拼页、道具完成度、歧义物件、Painterly Comic Animation 连续性、手绘风格优先级、材质绘画证据、三尺度验收、身份与表演变量分离、显式平涂/黑白媒介覆盖等情况。

## License

[MIT](LICENSE) © 2026 zcjunn
