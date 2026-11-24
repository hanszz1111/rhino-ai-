---
name: rhino-nurbs-fairing
description: 在 Rhino 中改善工业外观 NURBS 曲线和曲面的面内光顺，控制高光、曲率峰值和曲面偏差。适用于重建截面、Loft、Sweep、NetworkSrf、局部补片、保留轮廓的改款和反射斑马纹诊断。
---

# Rhino NURBS 曲线与曲面光顺

## 诊断范围

- 从相同相机与反射方向出发，区分轮廓波纹、面内反射波动、面际切线或曲率跳变、网格显示误差。改变显示网格精度或反射方向复核显示问题。
- 锁定分件线、安装面、关键截面、端口及需保持的最大包络。可用位移预算由设计约束决定。记录原轮廓、代表剖面和高光。
- 区分 NURBS 母面、裁剪边和独立参考曲线。比较用的裁剪边或轮廓应来自当前模型，检查线需与实际几何重新对照。

## 选面与调整

| 情况 | 建模方法 |
| --- | --- |
| 同一方向由稳定截面主导 | 用 Loft，先统一曲线方向、闭环缝点和截面对应。检查过密截面是否引入局部波纹。 |
| 一条路径或两条边界决定形体 | 用 Sweep1 或 Sweep2，预演转弯处的截面朝向、轨道距离和扫掠扭转。 |
| 横纵两组轨线都承担造型约束 | 用 NetworkSrf 或 Gordon 型曲面。核对交点顺序和相交误差，在轨线偏差和面内光顺之间选择。 |
| 只有边缘或高光局部异常 | 找到问题方向后移动少量控制点，或在可编辑的自然边重匹配。必要时分出独立角块，保住远端基准。 |

曲线或截面重建时，先试较少的跨段数，再按受约束的位置增加控制。每轮对比匹配前后的最大偏差、端点切向和曲率梳。用同一组截面复查峰值、意外反曲与平直段。调整过渡面时留一份修剪前母面和控制轨线。

## 验收

- 用固定相机斑马纹和不同方向的剖面检查面内高光。重点核对渐消端、最窄处、角部和切孔后的可见边。
- 对接缝量位置误差、法向夹角，并在共同切平面内对比方向性法曲率。把软件公差、用途要求与实测结果写清。拓扑闭合、视觉光顺和连续性测量分别记录。
- 对冻结的轮廓、外包络和装配面做回归检查。只测过部分剖面时，说明采样位置和范围。

## 参考

- Rhino 曲面匹配脚本的作者实现。 [CADacombs Rhinopython](https://github.com/CADacombs/rhinopython)
- 基于曲线网络的实现思路。 [CurvesWB](https://github.com/tomate44/CurvesWB) · [occ_gordon](https://github.com/rainman110/occ_gordon)
- RhinoCommon 的原生曲面工具和样例。 [McNeel Rhino Developer Samples](https://github.com/mcneel/rhino-developer-samples) · [McNeel Brep API](https://developer.rhino3d.com/api/rhinocommon/type/rhino.geometry.brep/)
