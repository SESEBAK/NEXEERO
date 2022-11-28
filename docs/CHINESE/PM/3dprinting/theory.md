<br>
 <img style="float: center;" width=700 src="IMAGE/3d.png">

# 第一步 – 创建
3D打印首先是创建我们要打印的对象的蓝图斜线三维数字文件。创建数字模型的最常见方法是使用计算机辅助设计 - CAD。但是，有大量专业和入门级软件可以生成适合 3D 打印的文件。

- 设计：您可以使用 Blender、SketchUp、AutoCad、SolidWorks、Maya、PhotoShop、ThinkerCad 等 3D 建模软件来创建您自己的设计。我们将 Fusion360 用于该项目中的所有设计。
- 扫描：创建三维数字文件的另一种方法是通过 3D 扫描。 3D 扫描是一种与 3D 打印密切相关的技术，它分析现实世界的物体并立即创建数字复制品。 3D 扫描广泛用于行业专业人士的逆向工程任务。将现有对象数字化后，我们还可以选择在打印前对其进行修改。此过程需要 3D 扫描仪。
- 下载：如果您没有耐心，只想继续打印一些东西，您可以访问 Thingivers、YouMagine、CrabCad 和 MyMinifactory Shapeways 等网站下载或购买其他用户建模的文件。在大多数情况下，这些文件都可以进行 3d 打印！

最后，3D 文件在发送到打印机之前必须满足几个设计要求。在为增材制造（3D 打印）进行设计时，我们需要牢记我们是为现实世界设计的。诸如适当的比例尺寸、最小壁厚、歧管/水密性等等，仅举几例，我们将在稍后进行更深入的研究。

[链接到免费设计软件，准备打印文件和切片引擎](http://my3dconcepts.com/explore/design-scan-download/)


# 第二步——STL
完成 CAD 设计后，就可以将其发送给打印机了。首先，我们需要将其转换成合适的文件格式。最常见的 3D 打印文件格式称为 STL，代表 StereoLithography，并以有史以来第一个 3D 打印过程命名。 STL还有其他几种含义，例如“标准三角形语言”和“标准镶嵌语言”。这里要记住的重要一点是.STL 是可用的文件扩展名。

此文件格式包括三角网格（多边形），即描述三维对象布局/表面的数据。 STL 的替代品是 .OBJ 和 .3MF。请记住，所有这些文件格式都不包含颜色信息。对于全彩 3D 打印，您需要使用 .X3D、.WRL、.DAE、.PLY 等文件格式

这里需要注意的是，并非每个 STL 或 OBJ 文件默认都是可 3D 打印的。文件格式必须满足某些标准，如最大多边形数、水密性、适当的物理尺寸、最小壁厚等。（在此处阅读更多信息。）简而言之，它们必须在设计时考虑到 3D 打印！
切片 – CAM

<br>
 <img style="float: center;" width=700 src="IMAGE/stl.png">

# 第三步——切片
这是将 3D 文件转换为 3D 打印机要遵循的说明的过程。是的，这就是有趣的部分，您需要一个特殊的软件才能做到这一点！基本上，切片是将 3D 模型划分或切碎成数百或数千个水平层，一步一步地告诉机器确切要做什么。

使用的软件是 [Flashforge 3D Printer](https://www.flashforge.com/download-center)

<br>
 <img style="float: center;" width=700 src="IMAGE/slice.png">


文件被切片后，会生成一种新的文件格式，称为 G 代码，文件扩展名为 .gcode。 G代码是使用最广泛的数字代码编程语言，主要用于计算机辅助制造，以控制3D打印机和CNC（计算机数字控制）等自动化机床。简而言之，G 代码是机器的语言，也是我们用来与之交流的语言！

如果您拥有 3D 打印机，则必须自己动手。您可以调整很多设置以获得打印机的最佳效果。好消息是——根本不需要编码 😉

如果您使用的是 3D 打印服务提供商，则不必担心切片问题。为什么？因为提供者会为您做这件事。您需要做的就是上传正确的文件格式并等待 3D 打印过程完成。
<br>
 <img style="float: center;" width=700 src="IMAGE/send.png">

# 第四步——打印

<br>
 <img style="float: center;" width=400 src="IMAGE/1step.jpg">

<br>
 <img style="float: center;" width=400 src="IMAGE/levels.jpg">

<br>
 <img style="float: center;" width=400 src="IMAGE/4step.png">

<br>
 <img style="float: center;" width=400 src="IMAGE/5step.png">


印刷机由许多移动和复杂的部件组成，它们需要正确的维护和校准才能打印出成功的印刷品。大多数 3D 打印机在打印开始后不需要进行监控。机器会自动执行 G 代码指令，所以只要没有软件错误或机器没有用完原材料，打印过程中就不会出现问题。

# 第五步 – 删除
从打印机中取出成品部件会因 3D 打印技术的不同而有所不同。在某些情况下，例如台式机，它就像将打印件与构建平台分开一样简单。对于一些工业级 3D 打印机来说，部件的拆卸是一个技术过程，需要在受控环境中使用专业技能和专用设备。

<br>
 <img style="float: center;" width=400 src="IMAGE/postp.png">


# REFERENCES
1. [Nexmaker](https://www.nexmaker.com/doc/3_3dprinter/1.3Dprintingbackground.html)
2. [3D CONCEPTS](http://my3dconcepts.com/explore/how-3d-printing-works/)