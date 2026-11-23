---
name: rhino-model-validation
description: 验收 Rhino 工业产品和交付 .3dm，检查有效性、闭合、裸边、G1/G2、剖面间隙、指定零件干涉、命名视图和存盘重读。适用于模型审查与返工后的回归检查。
---

# Rhino 模型验收

先明确交付范围、开放面是否符合设计、角色与版本。按几何、光顺、配合和存盘分别验证，并留下实际值、采样区间和结果。

## 验收顺序

1. **基线。** 记录文档单位与公差、目标对象、部件名、应保留的母面、包络和命名视图。针对每项配合列出对象对、允许接触状态和指标阈值。
2. **几何。** 用 Check 或 IsValid 检查有效性。对必须闭合的零件再检查 IsSolid、裸边与非流形边。如果需要体积，先验明闭合性。记录开放曲面、装饰网格与实物实体各自的数量。
3. **光顺。** 在跨接缝对应位置测边界距离、法向夹角和方向性法曲率。G2 按约定采样，不同单位指标单独保存。用曲率图、Zebra 或反射预览检查面内波纹和拔尖，并定位到截面。
4. **配合。** 在剖面测入位方向的间隙、槽底和剩余壁厚。做零件对的静态交集检查。看起来接触且求解返回失败时，检查操作数、接触平面和截面，再决定是否存在干涉。要求可装入时，单独检查插入路径。
5. **重读交付文件。** 用 File3dm.Read 或 rhino3dm 核验实际文件的有效性、对象计数、命名视图、单位和检查图层可见性。曲率和实体交集需要的 Rhino 原生运算另由 Rhino 或 RhinoCommon 执行。

## 记录与排错

- 每项给出对象名、测量位置和结论。区分通过、未通过和无法判定。样本检查用采样区域描述，精确接触和几何重叠分别写明。
- 检查图层、辅助曲线及命名视图要用保存后的状态核对；应用中显示正确仍需确认文件重开后的显示。
- 结果不同时先核对读取的版本、单位和物体名称，再重跑当前阶段。工具不支持的几何运算可用 RhinoCommon，离线文件读回适合验证数据结构与有效性。

## 参考

- 用工具元数据、几何测量与文件读回对照。 [RhinoMCP 建模指南](https://github.com/jingcheng-chen/rhinomcp/blob/main/cc-plugin/agents/rhino-modeler.md) · [McNeel 3DM 库](https://github.com/mcneel/rhino3dm)
- Rhino 裸边、非流形边和高光检查。 [ShowEdges](https://docs.mcneel.com/rhino/8/help/en-us/commands/showedges.htm) · [Zebra](https://docs.mcneel.com/rhino/8/help/en-us/commands/zebra.htm)
