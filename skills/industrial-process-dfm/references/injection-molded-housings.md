# 注塑壳体专项复核

1. **先定开模和零件归属。** 在模型中标出动模与定模拔模方向、主分型和止口所在件。侧孔、卡扣、反台阶和后装饰件逐个判断能否沿主方向释放。若需要侧抽或嵌件，标出运动方向与退出包络，记录分型变化对外观线的影响。
2. **在真实拔模方向上测。** 用 `DraftAngleAnalysis` 为每个模具方向单独设置拉拔矢量，并以实际表面法向和供应商要求解释色带。沿位移方向做剖面检查局部倒扣和遮挡，覆盖深筋、屏幕口、渐消凹面和分型末端。外部纹理、内抛光和薄钢位分别核对。
3. **沿剖面定位厚度问题。** 同时量凹面背后的薄壁和柱根、筋根、转角的厚料堆积。可优先改变内壁、掏空厚区或把筋与柱的连接移至非外观区。说明测量是局部法向、指定截面还是最短距离，按同一口径复测。
4. **留出制造空间。** 在可见面、密封面和定位面标出浇口、顶针、排气、镶件痕迹可能冲突的区域。模具供应商确定最终方案之前，记录工艺假设和需要确认的区域。卡扣另外检查自由状态、装入变形、实际扣合量和拆卸操作空间。
5. **回查装配方向和分缝。** 复核修改后的机芯包络、座肩深度、带涂层的成品间隙、极限位置和紧固工具路线。记录最薄点、拔模方向、倒扣位置和需要供应商确认的具体要求。

## 参考

- Rhino 拔模分析方向和网格精度设置。 [McNeel DraftAngleAnalysis](https://docs.mcneel.com/rhino/8/help/en-us/commands/draftangleanalysis.htm) · [McNeel 拔模等值线代码示例](https://github.com/mcneel/rhino-developer-samples/blob/441d7301d3c9fa55d94e2c244d93f43d48b2c708/rhinopython/SampleDraftAngleCurves.py)
- 从工艺约束定位设计检查项和证据缺口。 [BaratiLab DFM Review](https://github.com/BaratiLab/mechanical-engineering-skills/blob/119b1a946e2ea43784f5d045057b59757a1a7dd1/skills/dfm-review/SKILL.md) · [CAD Design Review](https://github.com/RamunasSab/cad-design-review/blob/78f650ddf84f05672dbba5e05e1c42e05365f7bd/SKILL.md)
