# Rhino AI 建模技能

面向 Rhino 工业产品设计的 Codex 技能集，覆盖从建模顺序到装配和存盘验收。

| 技能 | 用途 |
|---|---|
| [建模顺序](skills/rhino-modeling-sequence/SKILL.md) | 确定基准、母面、分件、壳体、嵌件和细节的建模先后 |
| [圆角与倒角](skills/rhino-edge-rounding/SKILL.md) | 选择圆弧、直倒角、变半径或曲率过渡，诊断薄壁和角区失败 |
| [曲面接平面](skills/rhino-surface-to-plane/SKILL.md) | 保留定位平面，构建和检查 G1、G2 衔接 |
| [切割补面](skills/rhino-trim-and-patch/SKILL.md) | 处理交线、分割、修剪、补片和闭合 |
| [渐消面](skills/rhino-surface-runout/SKILL.md) | 设计宽度、高差或半径的渐消，并处理过渡末端 |
| [嵌件与装配配合](skills/rhino-inlay-fit/SKILL.md) | 设计嵌槽、座肩、装配方向和间隙 |
| [模型验收](skills/rhino-model-validation/SKILL.md) | 验证实体、光顺、配合及保存后的文件状态 |

## 在 Codex 中调用

将需要使用的技能目录复制到本机 Codex 技能目录 `~/.codex/skills/`。每个目录须保留自己的 `SKILL.md`。随后可按名称调用，例如 `$rhino-modeling-sequence`。

需要控制 Rhino 时，可配置 [RhinoMCP](https://github.com/jingcheng-chen/rhinomcp)。各技能末尾附对应的 Rhino 官方文档和公开参考。
