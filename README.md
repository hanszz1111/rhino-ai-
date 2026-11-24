# Rhino AI 工业设计技能库

面向实体产品的 Codex 技能集，覆盖参考图与机芯输入、产品定义、Rhino 建模、曲面优化、工艺与验收。可按任务选用其中一项，也可按一个产品的设计阶段组合调用。

## 产品定义与工艺

| 技能 | 适用任务 |
| --- | --- |
| [工业产品设计](skills/industrial-product-design/SKILL.md) | 比较造型方案，锁定真实基准、交互、人机和分件 |
| [CMF 开发](skills/industrial-cmf-development/SKILL.md) | 定义颜色、材料及表面工艺，同视角评审与样板验证 |
| [工艺与 DFM](skills/industrial-process-dfm/SKILL.md) | 复核注塑、CNC、钣金、增材和包胶的几何约束 |

## Rhino 建模与验收

| 技能 | 适用任务 |
| --- | --- |
| [建模顺序](skills/rhino-modeling-sequence/SKILL.md) | 排定基准、母面、分件、壳体、嵌件和细节的建模先后 |
| [参考装配与真实接口](skills/rhino-reference-assembly/SKILL.md) | 由机芯、原屏幕、PCB、镜组和原端盖提取接口与装配基准 |
| [NURBS 光顺](skills/rhino-nurbs-fairing/SKILL.md) | 优化截面、控制曲面偏差，核对曲率梳与反射 |
| [曲面接平面](skills/rhino-surface-to-plane/SKILL.md) | 保留定位平面，构建和检查 G1、G2 衔接 |
| [渐消面](skills/rhino-surface-runout/SKILL.md) | 比较凹深、宽度和收尾方案，核对薄壁与两端高光 |
| [圆角与倒角](skills/rhino-edge-rounding/SKILL.md) | 选择圆弧、直倒角、变半径或曲率过渡，诊断薄壁和角区失败 |
| [切割补面](skills/rhino-trim-and-patch/SKILL.md) | 处理交线、分割、修剪、补片和闭合 |
| [嵌件与装配配合](skills/rhino-inlay-fit/SKILL.md) | 设计嵌槽、座肩、装配方向和间隙 |
| [模型验收](skills/rhino-model-validation/SKILL.md) | 验证实体、光顺、配合及保存后的文件状态 |

## 按任务组合

- **从参考图出方案**。工业产品设计 → 建模顺序 → NURBS 光顺 → CMF → 模型验收。
- **机芯外壳改款**。参考装配确定原零件与开孔 → 建模顺序规划外壳 → 渐消面与曲面接平面 → 嵌件落座 → 工艺与 DFM。
- **保轮廓做局部修面**。NURBS 光顺诊断 → 曲面接平面、渐消面或切割补面 → 在原截面上复测偏差与连续性。

## 在 Codex 中调用

把所需的独立技能目录复制到本机 Codex 技能目录 ~/.codex/skills/，每个目录保留自己的 SKILL.md。随后可按名称调用，如 $rhino-surface-runout、$rhino-reference-assembly。

需要控制 Rhino 时，可配置 RhinoMCP。查阅 GitHub 上的原始技能、曲面工具和工艺实现时，请从来源索引选择与任务匹配的入口。 [RhinoMCP](https://github.com/jingcheng-chen/rhinomcp) · [GitHub 来源索引](SOURCES.md)
