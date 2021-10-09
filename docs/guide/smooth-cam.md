---
title: 让摄像机丝滑般运动
---
::: right
Blender Version 2.93.5 / [最强侦察兵布洛特亨德尔动画工程](https://www.bilibili.com/video/BV1aq4y1V7W3)
:::

---

这篇指南基于 Youtube 视频 ["Tutorial: Quick Smooth Camera Movements in Blender"](https://youtu.be/a7qyW1G350g)

如果你需要更完整的操作指导，可以点击上方标题前往观看。

## 范例

这几秒取自于潜行的一个动画。
这里面的镜头移动关键帧都处于 Blender 自动钳制状态，所以过于密集的关键帧下会显得抽拉感拉满。

<div style="position: relative; padding: 30% 45%;">
<video src="https://assets.007.rip/video/blender-smooth-cam-1.mp4" controls="controls" style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;">
Your browser does not support the video tag.
</video>
</div>

### 取样关键帧

找到你需要平滑的摄像机关键帧，并选中它们。

![](https://pic.imgdb.cn/item/615ffbff2ab3f51d91b1df2a.png)

将鼠标停放在 Dope Sheet（动画摄影表）上，然后使用快捷键 `Ctrl + Tab` 切换到 Graph Editor（曲线编辑器），然后按 `.` 键将可视区域范围设定到选定关键帧上。

![](https://pic.imgdb.cn/item/615ffcdc2ab3f51d91b3029a.png)

在 Key（关键帧）里找到 Smaple Keyframes（取样关键帧），你也可以使用 `Shift + Alt + O` 快捷键，

![](https://pic.imgdb.cn/item/615ffd042ab3f51d91b33778.png)

回看到曲线编辑器，所有被选中的关键帧之间会自动补全，此时你再用 `Ctrl + Tab` 切换回 Dope Sheet（动画摄影表）后，你会发现这些自动补全的关键帧是以蓝色标记的。

![](https://pic.imgdb.cn/item/615ffd812ab3f51d91b3ec70.png)

![](https://pic.imgdb.cn/item/615ffd732ab3f51d91b3db6f.png)

## 平滑关键帧

当你完成上面的内容后，在 Graph Editor（曲线编辑器）中的 Key（关键帧）里找到 Smooth Keys（平滑关键帧），我更推荐使用`Alt + O`快捷键，因为只按一次是不够的，建议按 30 次起步。

当你按到足够多的次数后，关键帧就会足够平滑。

![](https://pic.imgdb.cn/item/615ffeb22ab3f51d91b56ced.png)

### 最终效果

<div style="position: relative; padding: 30% 45%;">
<video src="https://assets.007.rip/video/blender-smooth-cam-2.mp4" controls="controls" style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;">
Your browser does not support the video tag.
</video>
</div>