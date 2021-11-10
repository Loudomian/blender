---
title: DAZ Studio
---

::: right
DAZ Studio Version 4.15 / Blender Version 2.93.5
:::

有谁会不喜欢 DAZ 这个丰富的资产库呢？
合理利用里面的资产可以让我们更快实现想要的效果。

本片指南会手把手教你如何安装 DAZ Studio 跟 Blender 交互的插件。

需要值得注意的是，我并不推荐使用官方所提供的插件，那个插件原本也是社区制作的，后来被官方采纳了，那个插件比较封闭，很多效果都无法实现。

## 下载

我们需要下载的插件由 Diffeomorphic 制作。

[[ 官方网站 ]](http://diffeomorphic.blogspot.com/)  [[ 最新下载地址 ]](https://bitbucket.org/Diffeomorphic/import_daz/downloads/)

作者还提供了一个稳定版地址，你可以去对应页面找到下载地址，我个人比较推荐下载 Bitbucket 仓库的最新版。

![](https://pic.imgdb.cn/item/618a94202ab3f51d91985e1a.jpg)

## 安装

你需要给 Blender 和 DAZ Studio 分别安装上对应的插件。

### Blender

下载好压缩包后，不需要解压，直接通过 Blender 内的插件安装进行安装即可，然后启用插件，但不要关闭 Blender。

![](https://pic.imgdb.cn/item/618a96122ab3f51d91991f2f.jpg)

![](https://pic.imgdb.cn/item/618a966c2ab3f51d91993e99.jpg)

### DAZ Studio

解压压缩包，你可以看到一个叫做 to_daz_studio 的文件夹，里面有一个 Scripts 的文件夹，复制 Scripts 文件夹，粘贴到你的 DAZ 资产库里覆盖。

![](https://pic.imgdb.cn/item/618a96902ab3f51d91994cda.jpg)

![](https://pic.imgdb.cn/item/618a96d42ab3f51d91996b40.jpg)

## 配置插件

安装好插件后并不意味着可以直接使用，请跟随下方操作配置插件。

### DAZ Studio

#### 第一步

启动 DAZ Studio，找到 Scripts 目录下的 Diffeomorphic 文件夹，你会看到5个选项。

![](https://pic.imgdb.cn/item/618a976a2ab3f51d9199a2ff.jpg)

点击 Setup Menus 选项，它会自动在 File 栏目下设置2个输出方式，一个是 Export To Blender，一个是Export HD To Blender，两者区别是一个是正常版本，一个是细分后版本，且不含骨骼，正常情况下使用 Export To Blender 即可。

![](https://pic.imgdb.cn/item/618a97c72ab3f51d9199c357.jpg)

#### 第二步

点击 Save Root Paths 选项，这个选项的作用是输出一个 json 文件告诉 Blender 我们的 DAZ 资产库在哪个地方，这样就不需要我们手动寻找了。

![](https://pic.imgdb.cn/item/618a98e32ab3f51d919a2407.jpg)

### Blender

回到 Blender 里，在右侧面板找到 DAZ Importer 栏目，点击 Global Settings 进入设置界面。

点击左下角的 Load Root Paths 后，找到你刚才在 DAZ Studio 输出的 json 文件并导入，插件会自动处理路径。

![](https://pic.imgdb.cn/item/618a993c2ab3f51d919af0ea.jpg)

![](https://pic.imgdb.cn/item/618a99a82ab3f51d919b7bc6.jpg)

接着，修改第三和第四栏目的参数，你可以参考上图我的设定。

## 使用资产

### 从 DAZ Studio 中导出
首先，你需要在 DAZ Studio 里载入你需要导出的资产，可以是场景、角色或者是衣服，在这里我载入了一个奎爷和他的衣服。

::: tip 提示
你在 DAZ Studio 中的 Morph 修改也可以被正常导出，但 DAZ 的布料自动贴合角色则无法保留。
:::

![](https://pic.imgdb.cn/item/618a9c922ab3f51d919cf9a5.jpg)

接着，去 File 中保存工程，这里我新建了一个 Kratos 文件夹，并将工程命名为 1.duf。

![](https://pic.imgdb.cn/item/618a9d5d2ab3f51d919d6c0d.jpg)

然后，再去 File 中点击 Export To Blender 输出 1.dbz 到 Kratos 文件夹。

::: warning 注意
duf 和 dbz 必须存放在同一目录下，并且一定要相同命名，否则插件无法正常寻找资产并导入。
:::

最后文件夹里看起来是这样的。

![](https://pic.imgdb.cn/item/618a9dda2ab3f51d919da8c4.jpg)

### 在 Blender 中导入

在 Blender 导出选项中，你可以选择 DAZ 或者是 Easy DAZ，两者的区别则是你不需要手动在面板中合并骨骼，导入修正或是表情 Morph 这类重复性操作。

但为了更大的修改空间以演示功能，我在这里使用基础的 DAZ 导入，需要注意的是，你只能选择 duf 文件导入，选择 dbz 是无法导入的。

![](https://pic.imgdb.cn/item/618aa6972ab3f51d91a1a8e9.jpg)

等待片刻，DAZ Studio 工程中所有资产都会载入。

![](https://pic.imgdb.cn/item/618aa7022ab3f51d91a1d1ac.jpg)

## 面板功能

由于我平时用的高级功能较少，在这里我只会讲一些比较基础的操作，更多的玩法请前往 [[ 官方网站 ]](http://diffeomorphic.blogspot.com/)
了解。

::: warning 注意
所有操作必须依照面板排序由上到下逐步进行，正常情况下反向操作会导致功能无法正常使用的问题。
:::

### 合并骨骼

::: tip 提示
这个功能可以用在任何重复命名的骨骼上。
:::

在正常导入后，你会发现所有物体都是有自己的独立骨骼控制，好比身体有一套骨骼，睫毛有一套骨骼，衣服每一个部分都有一套骨骼。

![](https://pic.imgdb.cn/item/618aaa3b2ab3f51d91a2dd57.jpg)

这时你可以通过 Merge Rigs 按钮合并骨骼。

选择所有子骨骼后最后选择身体的主骨骼，然后点击 Merge Rigs，弹出的面板选择默认，点击 OK 后，相同命名的骨骼会合并为到一起。

![](https://pic.imgdb.cn/item/618aaa722ab3f51d91a2f353.jpg)

![](https://pic.imgdb.cn/item/618aaada2ab3f51d91a31167.jpg)

### 导入JCM

JCM 全称 Joint Controlled Morphs，中文译作联合控制形变，你可以理解成用来自动修正骨骼变形的 Shapekey。

::: warning 注意
需要知道的是，JCM 并非是全能的存在，它仍会在一些特定的动作下产生奇怪的负面影响，你随时可以手动修正或临时停用掉。
:::

是 Morphs 栏目的一员，你可以通过点击进对应栏目里的按钮预览相应会载入的 Morphs，如果你仍有较大疑惑，请在评论区留言。

正常情况下会全部选中，点击 OK 后等待片刻，选中的 Morphs 将会被自动绑定上骨骼驱动器。

![](https://pic.imgdb.cn/item/618aac3d2ab3f51d91a38ab0.jpg)

#### 对比

![有JCM](https://pic.imgdb.cn/item/618aacbb2ab3f51d91a3b669.jpg)

![无JCM](https://pic.imgdb.cn/item/618aacf32ab3f51d91a3cab3.jpg)

### 合并嫁接部分

Geografts，我翻译为嫁接模型，在 DAZ Studio 中一般用作添加 √8 或者是 PU33Y，以新的模型结构代替原有模型结构，我不敢给奎爷加这两玩意还发出来。

用法很简单，选中你希望合并的物体，再选中身体，去 Finishing 面板点击 Merge Geografts 即可。

插件会自动识别相同结构的部分，然后合并为一个物体。

::: warning 注意
如果无法正常合并，需要手动操作时，请记得修改 UV 贴图的名字，在大多数情况下 DAZ Studio 的模型 UV 命名是不一样的。
:::

![](https://pic.imgdb.cn/item/618ba5082ab3f51d91fe1721.jpg)

### 骨骼转换

插件提供一键转换为高级 Rig 的按钮，你可以去 Rigging 下点击 Create Rigify 以转换到 Rigify 骨骼。

![](https://pic.imgdb.cn/item/618ba6fb2ab3f51d91fed42a.jpg)

## 结语

目前上面总结的是我平时会使用的部分，如果你觉得我写的还不够详细或者有什么问题，欢迎评论区告诉我，我会找个时间展开讲讲。