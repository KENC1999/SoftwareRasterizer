# 软件光栅化渲染器

​	参考[tinyrenderer](https://github.com/ssloy/tinyrenderer/wiki)教程实现了一个简易的软件光栅化渲染器，实现功能包括：

1、Gouraud着色；

2、Blinn-Phong着色；

3、纹理贴图及法线贴图；

4、背面剔除及深度缓存；

5、交互式相机和渲染器，可旋转拉伸镜头并选择渲染参数。

---

使用的第三方库如下：

1、[tinyrenderer](https://github.com/ssloy/tinyrenderer/wiki)提供的model.h，用于读取模型文件；

2、[Eigen3](http://eigen.tuxfamily.org/index.php?title=Main_Page)，用于矩阵计算；

3、[EasyX](https://easyx.cn/)，用于绘制模型并实现交互功能。

编程语言为C++，代码在VS2017中选择Release x64模式编译。

---

​		若要运行程序，请将模型文件放在程序同目录下名称为“obj”的文件夹中，输入文件名即可（注意不要添加后缀，例如直接输入“african_head”）。

​		操作指南：

​		旋转视角——左键、CTRL+左键、右键、CTRL+右键

​		缩放——滑动鼠标中键

​		启用/关闭纹理——SHIFT+左键

​		启用/关闭法线贴图——SHIFT+右键

​		切换着色模式——按下鼠标中键

​		退出——CTRL+SHIFT+按下鼠标中键

演示效果如下：

<img src="C:\Users\22245\AppData\Roaming\Typora\typora-user-images\image-20200730235611642.png" alt="image-20200730235611642" style="zoom:33%;" /><img src="C:\Users\22245\AppData\Roaming\Typora\typora-user-images\image-20200730235538917.png" alt="image-20200730235538917" style="zoom: 33%;" />



<img src="C:\Users\22245\AppData\Roaming\Typora\typora-user-images\image-20200730235734318.png" alt="image-20200730235734318" style="zoom:33%;" /><img src="C:\Users\22245\AppData\Roaming\Typora\typora-user-images\image-20200730235810406.png" alt="image-20200730235810406" style="zoom:33%;" />

---

已知问题:

​		目前每次运行只能加载一个模型，且暂未实现阴影映射和环境光遮蔽，没有进行并行优化。计划把Path Tracing的渲染器写了再回来做。
