# 文件目录说明
- frontend 是前端
- backend 是后端
- utils 是工具
- notes 是笔记
有啥需要的随便加

### 编译说明：

```c++
cd BA_schur  \\ 进入文件夹
mkdir build   
cd build
cmake ..
make -j4    
```

### 开发记录
```c++
1. ubuntu 16.04 列清楚数据和整个架构

```

| camera pose | points| 
|---|---| 
|  frame 类型，3 个 pose|特征点，数目是20|
|元素包括Rwc qwc twc,featurePerId|Pw,都被3帧frame观测到| 
|featurePerId Pw经过平移和旋转投影到归一化平面上Pc||
 


| problem  | problem|vertexCams_vec|allPoints|
|---|---|---|---|
|AddVertex : pose 和逆深度|AddEdge: pose和逆深度|pose的7个量|逆深度|
|顶点：优化的变量 pose和观测值Pc|边：重投影误差项|四元素和平移量|Pc的倒数|
