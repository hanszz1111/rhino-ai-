---
name: rhino-trim-and-patch
description: 修复或重建 Rhino 产品曲面的切割、补面与断口。用于 Trim、Split、Untrim、ExtendSrf、EdgeSrf、NetworkSrf、Patch 选择，或诊断补面与布尔后裸边。
---

# Rhino 切割与补面

先判断是裁剪边丢失、底层面质量有问题，还是确实需要新造型。保留可用母面及交线，再确定补面的边界职责。

## 切割

1. 在副本上用 Intersect 检查相交范围和方向，优先形成清楚且连续的空间交线。封闭件用实体切削时，从两个侧面或剖面确认切削体完全穿过目标余量，并排除近相切、共面和零厚度交叉。
2. 用 Split 先保留切割两侧，确认保留区和曲线方向后再去除边料。未成功分割时检查边界环是否闭合、是否存在重复交段、短边、孤立小片或翻面。
3. 需要恢复母面时优先用保留的副本或可恢复的 Untrim，再视情况用 ExtendSrf 延长到可重新相交。近相切区可改变切削体的穿越角度或先分区。调整公差前先定位是构造间隙、投影误差还是修剪拓扑。

使用 RhinoMCP 时先核对当前版本对布尔预演与保留源对象的支持。预演成功后检查结果是否切除了期望区域及剩余壳厚。对空交集或失败返回，先在两处代表剖面核对真实相交区和端面接触，再选择延长、定位或分段切削。

## 补面

| 缺口形态 | 首选 |
|---|---|
| 平面闭合环 | PlanarSrf，或对实体的平面孔用 Cap |
| 两侧之间的狭长连续带 | BlendSrf，或有稳定双轨时用 Sweep2 构底后匹配 |
| 2–4 条界线明确的非平面开口 | EdgeSrf 建立边界基面，再按边的要求做匹配。三边面可能有奇点，应安置在非关键区 |
| 两向曲线网格 | NetworkSrf。每个方向内部曲线彼此不交，两方向相互跨越。按需设置边界匹配并实测 |
| 多边孔、扫描参考或不规则缺口 | 先尝试拆成可控的四边片。Patch 可作为拟合起点，复测边界距离和切向，确认后再裁剪与连接 |

1. 用实际 Brep 边或可靠的交线定位补面。需做 G1 或 G2 的自由边保留可编辑的自然边。MatchSrf 可以改未修剪边并匹配到目标裁剪边。
2. 先接关键光顺边，再处理次要角区。多个匹配冲突时，在角区增加专用补面或重分片，避免反复移动已匹配的主面。
3. 用 ShowEdges 定位裸边、非流形边和局部短边。Join 建立拓扑连接，边界配合与光顺另用距离、切向和曲率检查。预期闭合时复核有效性、实体闭合和正体积。交付文件可重开后重复关键检查。

## 参考

- 从已有边或交叉曲线建面。 [EdgeSrf](https://docs.mcneel.com/rhino/8/help/en-us/commands/edgesrf.htm) · [NetworkSrf](https://docs.mcneel.com/rhino/8mac/help/en-us/commands/networksrf.htm) · [Patch](https://docs.mcneel.com/rhino/8/help/en-us/commands/patch.htm)
- Rhino 8 的切削体和差集示例。 [McNeel RhinoCommon 样例](https://github.com/mcneel/rhino-developer-samples/blob/8/rhinocommon/cs/SampleCsCommands/SampleCsBooleanDifference.cs)
- 受损边界和连续性。 [ExtendSrf](https://docs.mcneel.com/rhino/8mac/help/en-us/commands/extendsrf.htm) · [MatchSrf](https://docs.mcneel.com/rhino/8/help/en-us/commands/matchsrf.htm) · [ShowEdges](https://docs.mcneel.com/rhino/8/help/en-us/commands/showedges.htm)
