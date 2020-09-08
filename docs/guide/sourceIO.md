---
title: 与Source资产交互(SourceIO)
---
::: right
Blender Version 2.90.0 / SourceIO Version 3.7.0
:::

---

这篇指南将会告诉你如何通过插件 SourceIO 在 Blender 中使用 Source引擎 的资产。

这篇指南可能会有多次的重组或合并，详细我会在本文最后留下每次更新时间和摘要。

## 准备

Source IO 是 [REDxEYE](https://github.com/REDxEYE) 写的一个插件。

你可以通过 [Github](https://github.com/REDxEYE/SourceIO/releases) 或者 [蓝奏云](https://wwa.lanzous.com/i56F2gghfsh) 下载。**请注意，版本的不同可能会导致无法实现本文的操作。**

将插件安装好后，你会在导入和导出选项中找到新的格式支持，如 `.mdl` `.vtf` 等。

## 导入资产

### MDL&VTF

`.mdl` 是 Source引擎 专有模型格式的扩展。它定义了模型的结构以及动画、材质、网格和LOD等信息。但是，它不完全包含模型所需的所有信息。额外的数据存储在PHY, ANI, VTX和VVD文件中。

SourceIO 会自动寻找 `.mdl` 所需要的额外信息，并直接导入到 Blender 中，省去了解包 `.mdl` 的功夫，同时还允许你将对应的 `.vtf` 一起导入。

---

#### 导入MDL

首先你需要将你要导入进 Blender 的模型解压放在 Source Filmmaker 的 usermod 里，然后在 Blender 中选择导入 `.mdl` ，并选择 `Import texture ` ，等待 Blender 处理，你所需要的模型就会直接载入进 Blender 了，并且含有对应的材质和贴图，如果你发现了没有导入糙度贴图、高光贴图和丢失透明通道的问题，别急，看下去。

![](https://pic.downk.cc/item/5f577c02160a154a67acdcbd.jpg)

![](https://pic.downk.cc/item/5f577c88160a154a67ad01f7.jpg)

---

#### 导入VTF

如果你没有 Source Filmmaker ，你依旧可以使用 SourceIO 直接打开 `.mdl` 但是，相应的贴图将不会自动导入，你需要手动导入，这个流程也适合上步骤没有导入糙度、高光等贴图和丢失透明通道的读者。

很简单的，导入 `.vtf` 找到你需要额外导入和导入丢失通道的贴图后，**点击掉**右边的 `Load alpha into separate image` ，之后你就得到了正常的带有透明通道的贴图。

![](https://pic.downk.cc/item/5f577db9160a154a67ad54bc.jpg)

---

临时结语，开始愉快的使用 Source引擎 的模型资产吧。