# 香草着色器入门教程！  
- [引言](#引言)
- [着色器](#着色器)
    - [什么是着色器](#什么是着色器)
    - [渲染原理](#渲染原理)
- [后处理着色器](#后处理着色器)
## 引言  
Minecraft 使用各式各样的着色器来渲染在屏幕上所看到的一切。通过在资源包中修改这些着色器，可以实现画面后处理、地图制作所需要的花哨特效或者许许多多新的创意，以使 Minecraft 更加高度自定义化和绚丽多彩。  

## 着色器
### 什么是着色器
「着色器」 ([Shader](https://en.wikipedia.org/wiki/Shader)) 是用于后期处理、特效或者图形渲染的一种程序。  
[OpenGL](https://en.wikipedia.org/wiki/OpenGL) 即「开放图形库」，是一套用于渲染图形的编程接口。Minecraft 使用 OpenGL 来渲染画面。  
在 Minecraft 中，着色器一般指 OpenGL 所使用的着色器。  
着色器在 Minecraft 中大体上可以分为两种：「后处理着色器」与「核心着色器」。  
「后处理着色器」正如其名，会对渲染完毕的画面进行后期处理。  
「核心着色器」是于 21w10a 被加入的新着色器类型，使得用户可以进一步自定义该如何渲染游戏的每个部分。  
### 渲染原理  
一般来说，渲染屏幕上的图形需要分为以下几步。  
1. 顶点着色器 (Vertex Shader)  
顶点着色器以图形的每个顶点坐标和一些用来变换位置的矩阵等作为输入，并输出变换后的顶点坐标以及一些后续流程所需要的额外的数据 (如顶点颜色)。后面会更详细地讨论它具体能做些什么。
2. 几何着色器、裁切与光栅化  
经顶点着色器变换后的顶点会装配成图元，输入几何着色器，裁切掉超出可视范围的部分，并且把图形变得像素化，以供后续使用。该部分在 Minecraft 中不可编辑 (但以普遍性理论而言，一般没有编辑该过程的需要)。

## 后处理着色器

本文采用[知识共享署名-非商业性使用 4.0 国际许可协议](http://creativecommons.org/licenses/by-nc/4.0/)进行许可。