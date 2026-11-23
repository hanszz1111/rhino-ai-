---
name: rhino-surface-to-plane
description: 设计和检验 Rhino 工业外观的曲面接平面及直线接曲线。适用于顶部平面、玻璃周边、端面到肩部、G1 或 G2 匹配及高光连续性。
---

# Rhino 曲面与平面衔接

以真实安装平面和截面为基准，决定平面要保留的有效区域。将机械分件、锐折和外观连续带分开处理。对可见的连续带，在平面一侧事先留出足以展开切向和曲率的宽度。

## 建构方法

1. 沿典型截面画出直线和过渡曲线，定位切点和曲率开始抬升的位置。曲线接直线时，G1 要求同切向，G2 再要求曲率向量在边界回到零。单段五次 Bézier 可用端点和相邻两个控制点沿目标切线排列，并保持端部导数非零。
2. 同时有平面与既有曲面时，优先保留两条可控的边界，在中间构建过渡带。用 BlendSrf 对两边分别选连续性。方向差大或边长比失衡时先重排对应点、增加少量关键截面或重新划分边界。
3. 曲面已经接近平面时，用 MatchSrf 调整可编辑的未修剪边，目标选平面侧。需要保护另一端时指定保留条件。若匹配产生远端变形、密集等参线或反折，回到边界和基底面调整。
4. 直接创建开放夹持的非有理 NURBS 面时，可让连接平面的前三排控制点位于目标平面，并保留边界的非退化参数化。由此使边界跨缝方向的一阶、二阶法向分量为零。该构造适用于接平面，接其他曲面需匹配对面的方向性曲率。

对多片面先校对 U/V 方向、对应端点和截面顺序。把转角和近奇点区单独加密采样。匹配后先量目标平面上的有效安装宽度，再复查过渡面远端与修剪后的边缘。

## 验证

- 在边缘对应位置测距离、切平面法向夹角，并按要求比较公共切平面内的方向性法曲率。平面侧各方向的法曲率为零。记录最大差和检查区间。
- 检查平面是否仍满足玻璃、开口和定位尺寸。用 Zebra 或反射、截面曲率图检查面内有无扭曲、曲率峰值或凹陷。看到反射线平滑是质量线索，确定几何要求仍需测量。
- 相切圆弧接平面时通常仍有曲率跳变。需要 G2 的重点肩部用曲率过渡带，并在合并与裁剪后复查选定边界。

## 参考

- 连续性与曲率的定义。 [McNeel 参数曲线与曲面](https://developer.rhino3d.com/en/guides/general/essential-mathematics/parametric-curves-surfaces/)
- 匹配边、保留另一端和独立两端曲率。 [MatchSrf](https://docs.mcneel.com/rhino/8/help/en-us/commands/matchsrf.htm) · [BlendSrf](https://docs.mcneel.com/rhino/8/help/en-us/commands/blendsrf.htm)
- 线接曲线和曲率检查。 [McNeel 曲线连续性](https://www.rhino3d.com/it/docs/guides/modeling/rhino-continuity-curves/) · [Zebra](https://docs.mcneel.com/rhino/8/help/en-us/commands/zebra.htm)
