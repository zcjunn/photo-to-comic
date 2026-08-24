# VibeComic

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827.svg)](SKILL.md)

把一张照片重构成一页真正有分镜、有主题、有视觉母题的漫画。

VibeComic 是一个面向 Codex 的照片漫画化 Skill。它不会把同一张照片反复裁切，也不会只叠加“动漫滤镜”；它会先阅读照片中的人物、空间、动作、道具与情绪关系，再设计可信的新机位和相邻时刻，最终生成一张紧凑、完整上色的多格漫画页。

> Turn one photograph into an authored multi-panel comic page with source-grounded storytelling, camera invention, motif continuity, and a stable finished-color cel-comic style.

## 它解决什么问题

常见的照片漫画化结果容易出现：

- 每格只是原图的远景、中景和近景裁切；
- 首格和末格内容重复；
- 多格从上到下堆叠成过长的条漫截图；
- 人物、服装、道具或环境跨格漂移；
- 关键道具在特写里反而结构不完整；
- 成图像淡彩线稿、半写实照片或混合画风。

VibeComic 把这些问题变成可检查的工作合同，而不是只依赖一段宽泛的提示词。

## 核心能力

- **自适应分格**：自动选择至少 3 格，只保留具有叙事增量的画面。
- **场景世界重建**：照片定义人物、空间和物件关系，但不锁死原相机。
- **可信的新机位**：根据地面、前景、路线、遮挡和景深关系设计低机位、侧面、肩后、俯视或物件视角。
- **动作推演**：只创造照片证据能够支持的短时相邻动作，不凭空编造事件。
- **视觉母题系统**：从伞、鞋、倒影、草穗、电塔、背带或其他显著元素中选择主母题与次级母题。
- **道具完成度锁**：统一道具的数量、轮廓、构件、材质、接触方式和跨格细节层级。
- **紧凑漫画页**：默认生成准确竖版 `2:3` 多列拼页，而不是单列长图。
- **完整彩色动漫风格**：默认使用完整不透明铺色、2–4 级赛璐璐明暗、结构性轮廓和统一的角色/背景完成度。
- **双重质量检查**：分别检查照片连续性与漫画分镜创作是否成立。

## 默认输出

- 一张完整漫画页；
- 至少 3 格，常见为 3–8 格；
- 默认宽高比为竖版 `2:3`；
- 四格以上采用多列、嵌格或错落拼页；
- 默认无文字，避免乱码；
- 默认采用 `Finished Luminous Cel Comic` 完整彩色赛璐璐风格；
- 用户明确要求黑白、水彩、铅笔或其他媒介时，切换为对应的统一完成度规则。

## 工作流程

```text
一张照片
  → Source Story Card：区分事实、推断与不可改动锚点
  → Scene World Model：重建支持面、景深、邻接和可用机位
  → Theme & State Change：确定主题与短时变化
  → Prop/Motif Bible：选择主导道具或视觉母题
  → Panel Difference Map：为每格分配镜头、动作和信息增量
  → Style Fingerprint + Completion Lock：冻结全页画风与完成度
  → 生成一张 2:3 多列漫画页
  → Source Continuity + Sequence Authorship 双质量门
```

## 安装

将仓库克隆到 Codex 的个人 Skills 目录：

```bash
git clone https://github.com/zcjunn/vibe-comic.git "${CODEX_HOME:-$HOME/.codex}/skills/vibe-comic"
```

重新载入 Codex 后即可自动触发，也可以显式调用：

```text
Use $vibe-comic to turn this photo into a finished comic page.
```

## 使用示例

上传一张照片后，可以直接说：

```text
用 VibeComic 把这张照片生成一页漫画，分格数量根据内容决定。
```

```text
用 $vibe-comic 重构这张照片，重点表现雨伞、倒影和人物与环境的关系。
```

```text
用 $vibe-comic 做成黑白漫画页，保留人物、服装和场景关系。
```

也支持只输出完整制作方案而不生图，或审查已有漫画页的连续性、版式、道具和画风问题。

## 目录结构

```text
vibe-comic/
├── SKILL.md                         # 入口、触发条件与核心合同
├── agents/openai.yaml              # Codex 界面名称与默认调用提示
├── evals/evals.json                # 34 个行为回归案例
└── references/
    ├── source-story-card.md         # 源照片证据、场景世界与连续性
    ├── style-research.md            # 风格研究、Style Fingerprint
    ├── sequence-engine.md           # 自适应分格、机位与版式引擎
    ├── prompt-compiler.md           # 生产提示词编译和预检
    └── quality-gate.md              # 双质量门与定向修正规则
```

## 设计原则

1. 照片是事实锚点和故事种子，不是逐格复制的底图。
2. 连续性保护人物、物件和空间世界，而不是保护原始镜头。
3. 新镜头必须由照片可见的空间关系支持。
4. 每格必须改变信息、动作、视点或母题意义。
5. 线条服务于结构，色块和分组明暗承担最终完成度。
6. 参考流行漫画时只提取通用视觉语言，不复制具体作者、角色、作品世界或页面。

## 隐私与参考图边界

- 用户提供的照片只用于当前漫画生成任务。
- 不进行反向搜图、公开上传或无关保存。
- 默认只把用户当前的源照片发送给图像生成工具。
- 风格参考仅用于抽象分析；除非用户明确授权，不作为额外生成输入。
- 仓库不包含示例用户照片或生成结果。

## 验证

可以使用 Codex 自带的 Skill 校验器检查结构：

```bash
python ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ~/.codex/skills/vibe-comic
```

行为评测位于 [`evals/evals.json`](evals/evals.json)，覆盖最低三格、自由机位、首尾去重、固定 2:3 拼页、道具完成度、歧义物件、完整彩色风格和显式媒介覆盖等情况。

## License

[MIT](LICENSE) © 2026 zcjunn
