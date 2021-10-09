---
title: 提高低面数模型视觉质量
---

::: right
Blender Version 2.93.5 / [最强侦察兵布洛特亨德尔动画工程](https://www.bilibili.com/video/BV1aq4y1V7W3)
:::

---

这篇指南从模型面数和实体化层面优化模型，在视觉上会比直接使用低面模型更有冲击。

## 范例

这是从 Apex Legends 中提取的渡鸦模型，面数十分低，精细度也不高。

只需要简单的添加几个修改器，它就会更加栩栩如生。

![](https://pic.imgdb.cn/item/6161c5142ab3f51d9170420c.png)

## 实体化修改器

在修改器面板添加 Solidify（实体化）修改器，并根据模型大小添加一定的厚度。

![](https://pic.imgdb.cn/item/6161c2fe2ab3f51d916c2cd3.png)

## 表面细分修改器

接着再添加 Subdivision（表面细分）修改器，给它增加面数并平滑结构。
::: tip 提示
表面细分修改器需要放在实体化修改器后面，以避免产生奇怪的暗角。
:::

![](https://pic.imgdb.cn/item/6161cd2d2ab3f51d91802a55.png)

## 额外

对于那些有棱角的模型在使用表面细分后会丢失掉部分曲折细节，你可以添加一个 Bevel（倒角）修改器在 Subdivision（表面细分）修改器之前以补全细节。

### 没有 Bevel（倒角）修改器

![](https://pic.imgdb.cn/item/6161cf162ab3f51d91837ef7.jpg)

### 添加 Bevel（倒角）修改器

![](https://pic.imgdb.cn/item/6161cf692ab3f51d918407b0.jpg)

## 温馨提示

- 不要忘记关掉视图显示（显示屏图标），不然卡崩 Blender 不要怪我。

![](https://pic.imgdb.cn/item/6161d0782ab3f51d9185b5be.jpg)

- 如果你觉得一直开着这些修改器会导致渲染时间大大延长，可以尝试给渲染应用（相机图标）打上关键帧，在需要高质量显示的时候再使用修改器效果。

![](https://pic.imgdb.cn/item/6161d08b2ab3f51d9185d2eb.jpg)