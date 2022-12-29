# Navfn Planner

这个仓库主要用于学习ros2中实现的A*算法和Dijkstra，主要改动是添加了一些代码注释来便于阅读和理解代码，你可以在[这里](https://github.com/hanlin-cheng/slam-study-note/blob/master/slam_theory/%E8%B7%AF%E5%BE%84%E8%A7%84%E5%88%92%E4%B9%8BA-star%E7%AE%97%E6%B3%95.md)找到A-star的原理介绍，并且在[这里](https://github.com/hanlin-cheng/A-Star-algorithm)找到一个利用c++实现的简易A *算法。

### **概述**

- 相关源代码位于[Github网站](https://github.com/ros-planning/navigation2/tree/main/nav2_navfn_planner)上。
- NavFn规划器插件实现了波前Dijkstra或A*扩展规划器。
- 是为该类型选择的相应规划器插件ID。
- 在官方[配置指南](https://navigation.ros.org/configuration/packages/configuring-navfn.html)页了解其参数配置

### **参数**

- .tolerance参数：

```
数据类型：double
默认值：0.5
描述：用于设置请求的目标位姿与路径终点之间的容许误差，单位为m。
```

- .use_astar参数：

```
数据类型：bool
默认值：False
描述：用于设置是否使用A*算法。如果为False，则会使用Dijkstra扩展算法（*注：这两者均为路径规划算法，其区别可以参阅知乎文章“路径规划算法(一)：Dijkstra和A*”）。
```

- .allow_unknown参数：

```
数据类型：bool
默认值：True
描述：用于设置是否允许在未知空间中进行路径规划。
```

> 醉后不知天在水，满船清梦压星河。