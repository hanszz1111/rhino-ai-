# GitHub 来源索引

这里登记查阅的上游技能、代码和工具。仓库中的技能是面向 Rhino 的原创整理，第三方技能与源码由各自上游发布。GitHub 链接固定到查阅时的提交。

按项目选择可迁移的方法。Rhino、FreeCAD 和 OCCT 的连续性选项、容差及布尔行为需要在实际内核中验证。

## 产品定义与造型

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [Engineering Design Skills](https://github.com/cmudrc/engineering-design-skills/blob/08780ce4b94f0e7c125e00255873a35d2013aca4/README.md) | 技能集 | 按设计阶段选择问题定义、候选方案与评价方法。 |
| [Industrial Product Design with GB/T Handoff](https://github.com/beiming183-cloud/industrial-product-design-gbt/blob/3463f40973dc1fae2e84fd80a151b0b262dec5ce/README.md) | 技能 | 物理产品定义、参考图、人因、外观与工程交付。工程要求需要本项目自己的输入和量测。 |
| [Claude Product Designer Skill](https://github.com/shawnlix/claude-product-designer-skill/blob/76c2b29194674a4dc936d44894dd14045ea6521b/SKILL.md) | 技能 | 参考从简报到造型、壳内空间、机制与 CMF 的阶段顺序。 |
| [Buro Industrial Designer](https://github.com/getburo/buro-free/blob/86cd7e849bee7b04b159644afdb6a9abd0f4a7c8/skills/industrial-designer/SKILL.md) | 技能 | 参考人机操作、握持和产品形态的评审问题。 |
| [Industrial Design Skill](https://github.com/emirerdo/industrial-design-skill/blob/e643991c18894f47e60046ca06b35ca0c0a702cb/skills/industrial-design/SKILL.md) | 技能 | 先看等比整体体量，再比较边缘层级、分缝和功能开口。 |

## 工程图与图像重建

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [CAD Drawing to Model](https://github.com/Anson2251/cad-drawing-to-model-skill/blob/7470b5c9f2b7e092a0a799f3b56d1fd4628e686e/skills/cad-drawing-to-model/SKILL.md) | 技能 | 从多视图、剖视与控制尺寸重建，再用实际 CAD 视图逐项核对。上游示例采用 build123d。 |
| [BaratiLab Sketch to CAD](https://github.com/BaratiLab/mechanical-engineering-skills/blob/119b1a946e2ea43784f5d045057b59757a1a7dd1/skills/sketch-to-cad/SKILL.md) | 技能 | 区分视图、标定实尺度、记录尺寸置信度。 |
| [FreeCAD Sketch from Image](https://github.com/ghbalf/freecad-ai/blob/41f03d7af3f4aec932d70d36fc8f1a99ae2ad25e/skills/sketch-from-image/SKILL.md) | 技能 | 参考已知尺度校准和草图几何识别。真实尺寸和图纸标注仍需按各附件独立核对。 |

## CMF 与外观表达

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [MaterialX PBR Specification](https://github.com/AcademySoftwareFoundation/MaterialX/blob/48106ed259bf1b905ed284f03a073f8be61a8734/documents/Specification/MaterialX.PBRSpec.md) | 规范源码 | 用于核对金属、粗糙度、涂层与各向异性的渲染参数。 |
| [Khronos glTF Transmission](https://github.com/KhronosGroup/glTF/blob/da88a3bbbe168cc728eddf71fa5e1915cc2c0629/extensions/2.0/Khronos/KHR_materials_transmission/README.md) | 规范源码 | 用于核对镜片或屏幕盖板的透射材质在交换时的语义。 |

## 制造工艺与装配

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [AgentCAD Skills](https://github.com/n3r/AgentCAD/blob/4b00aa503776eef9404bea9e489f3a244f423d3c/docs/skills.md) | 技能集 | 壳体、筋柱、拔模、卡扣、配合和装配基准。其示例使用 build123d / OCCT。 |
| [text-to-cad CAD Skill](https://github.com/earthtojake/text-to-cad/blob/b61fb3a974737e27d7b87a2b518a846d11861bc9/skills/cad/SKILL.md) | 技能 | 从工艺约束派生几何与可复查证据，按用途输出 STEP 等交换件。 |
| [FreeCAD DFM Workbench](https://github.com/ryankembrey/FreeCAD-DFM-Workbench/blob/9de829aed2dfb6ba4b4b6f41bf462c4ac8173060/README.md) | 工作台 | 用于建立不同工艺的检查项。原自动检查在 FreeCAD 中执行。 |
| [AgentCADCAM](https://github.com/jeremylongworth-source/AgentCADCAM/blob/2fd5f918dede5802716aa7965ec21dc8149d578c/README.md) | 技能集 | 用工艺、装夹和输出证据组织制造前评审及交接。 |
| [BaratiLab DFM Review](https://github.com/BaratiLab/mechanical-engineering-skills/blob/119b1a946e2ea43784f5d045057b59757a1a7dd1/skills/dfm-review/SKILL.md) | 技能 | 用工艺和材料定义注塑复核项，将可测问题与供应商确认事项对应起来。 |
| [BaratiLab Tolerance Stack-up](https://github.com/BaratiLab/mechanical-engineering-skills/blob/119b1a946e2ea43784f5d045057b59757a1a7dd1/skills/tolerance-stackup/SKILL.md) · [Drawing GD&T Review](https://github.com/BaratiLab/mechanical-engineering-skills/blob/119b1a946e2ea43784f5d045057b59757a1a7dd1/skills/drawing-gdt-review/SKILL.md) | 技能 | 参考尺寸链方向、最差范围、统计假设与图纸基准核对。 |
| [CAD Design Review](https://github.com/RamunasSab/cad-design-review/blob/78f650ddf84f05672dbba5e05e1c42e05365f7bd/SKILL.md) | 技能 | 区分尺寸、装配路径、功能检验和供应商输入所需的证据。 |
| [McNeel Draft Angle Curves](https://github.com/mcneel/rhino-developer-samples/blob/441d7301d3c9fa55d94e2c244d93f43d48b2c708/rhinopython/SampleDraftAngleCurves.py) | 官方代码样例 | 参考在指定拉拔方向上绘制拔模等值线。 |

## NURBS 曲面、连续性与渐消

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [CADacombs Curve Fair](https://github.com/CADacombs/rhinopython/blob/4e672082ec9c4227de286581414298d8ff86e091/spb_Crv_Fair.py) | Rhino 脚本 | 参考曲线光顺时的偏差限制和交互流程。 |
| [CADacombs MatchSrf](https://github.com/CADacombs/rhinopython/blob/4e672082ec9c4227de286581414298d8ff86e091/spb_MatchSrf.py) | Rhino 脚本 | 参考曲面边缘匹配的实现。测试时先核对使用环境和目标连续性。 |
| [CADacombs Edge Continuity](https://github.com/CADacombs/rhinopython/blob/4e672082ec9c4227de286581414298d8ff86e091/xBrep_EdgeContinuity_Interior_All.py) | Rhino 脚本 | 参考如何逐条复核已拼合模型内部的曲面接缝。 |
| [McNeel Surface Curvature](https://github.com/mcneel/rhino-developer-samples/blob/441d7301d3c9fa55d94e2c244d93f43d48b2c708/rhinocommon/snippets/cs/calculate-surface-curvature.cs) | 官方代码样例 | 读取指定曲面位置的主曲率与主方向，为渐消端量测提供基础。 |
| [CurvesWB](https://github.com/tomate44/CurvesWB/blob/d55914005cd06e41d71b76fec5c9cf17dd6c8e9c/README.md) | 工作台 | FreeCAD 中的曲线及自由曲面工具，参考构面策略与控制网络。 |
| [FreeCAD Gordon Surface](https://github.com/FreeCAD/FreeCAD-documentation/blob/0499378a238ce4c77c643b9cc4a03d0947381e45/wiki/Curves_GordonSurface.md) | 官方项目文档 | 核对横纵轨线网络、相交关系与选择顺序。 |
| [occ_gordon](https://github.com/rainman110/occ_gordon/blob/b9520328f46aa76559e61471050734ab41d984e4/README.md) | 几何库 | 供研究曲线网络插值与公差处理。实现基于 OCCT。 |
| [McNeel RhinoCommon Boolean Difference](https://github.com/mcneel/rhino-developer-samples/blob/441d7301d3c9fa55d94e2c244d93f43d48b2c708/rhinocommon/cs/SampleCsCommands/SampleCsBooleanDifference.cs) | 官方代码样例 | 参考贯穿切削体和文档公差。使用代码前核对本机 Rhino 版本。 |

## Rhino 执行、文件与验收

| 来源 | 类型 | 在本库中的用途 |
| --- | --- | --- |
| [RhinoMCP](https://github.com/jingcheng-chen/rhinomcp/blob/3c192bd8c800360f9fbce70d921d9d94bc7dc77f/README.md) | Rhino MCP 项目 | 发现当前可用工具，执行实际建模并读取文档状态。 |
| [rhino3dm](https://github.com/mcneel/rhino3dm/blob/cc0818a837b6255398e8117927223a41da6db530/README.md) | 几何读写库 | 用于原生模型的文件和对象复读，复杂操作的验收使用对应几何内核。 |

## Rhino 官方命令与接口

- 变半径的曲面过渡及截面约束。 [VariableBlendSrf](https://docs.mcneel.com/rhino/8/help/en-us/commands/variableblendsrf.htm)
- 接缝连续性和高光诊断。 [EdgeContinuity](https://docs.mcneel.com/rhino/8/help/en-us/commands/edgecontinuity.htm) · [Zebra](https://docs.mcneel.com/rhino/8/help/en-us/commands/zebra.htm) · [RhinoCommon Brep API](https://developer.rhino3d.com/api/rhinocommon/type/rhino.geometry.brep/)
- 设置实际拉拔方向并复核分析网格。 [DraftAngleAnalysis](https://docs.mcneel.com/rhino/8/help/en-us/commands/draftangleanalysis.htm)
