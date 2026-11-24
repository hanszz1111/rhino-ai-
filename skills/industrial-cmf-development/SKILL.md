---
name: industrial-cmf-development
description: 为实体产品制定颜色、材料与表面工艺方案，并用同视角渲染与材料样板核对。适用于珠光外壳、拉丝金属、喷涂、软胶、镜片、屏幕和跨零件的外观协调。
---

# 工业产品 CMF 开发

## 用零件和工艺定义外观

- 以零件、可见面和使用区为单位列出基材、着色方式、光泽、纹理方向、会磨损或接触的位置，以及要保持功能的区域。用统一的零件名称连接 CAD、渲染和工艺记录。
- 审查材质边界能否由真实分件、掩膜、印刷或其他可复现工序实现。对齐装配分缝，核对屏幕的黑边遮蔽、金属件的倒角高光、软胶的可视边和涂层覆盖后的配合。
- 比较模内质感与二次处理时，记录预期的外观层次、颜色均匀性、附着和耐磨需求，以及待供应商确认的表面规格与过程条件。在真实基材、曲率和装配缝上验证样板。

## 让渲染清楚表达设计

1. 先用中性材质和一致光源核对轮廓及反射，再比较颜色、粗糙度、金属感、涂层与纹理。对比时固定相机、投影、曝光和灯光。
2. 按零件职责设置材质。镀膜镜片关注透射和反射，黑色显示盖板区分丝印区、可视区和背板，拉丝方向沿真实加工走向。跨软件交换时确认目标渲染器支持所用参数。
3. 把渲染参数和量产规格分别写入记录。用实物样板或供应商可接受的颜色、光泽及纹理样件签认生产表现。尚未测得的性质注明待验证。
4. 输出 CMF 表、同视角对照和所需样板，标注变化和对应的 CAD 版本。

## 参考

- 参考图、外观语言与实体产品评审。 [Industrial Product Design with GB/T Handoff](https://github.com/beiming183-cloud/industrial-product-design-gbt)
- PBR 参数的跨渲染器含义。 [MaterialX PBR Specification](https://github.com/AcademySoftwareFoundation/MaterialX/blob/main/documents/Specification/MaterialX.PBRSpec.md)
- 光学透射材质的交换语义。 [Khronos glTF Transmission](https://github.com/KhronosGroup/glTF/blob/main/extensions/2.0/Khronos/KHR_materials_transmission/README.md)
