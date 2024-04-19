---
title: 'go2 控制器方案'
date: 2024-04-10
draft: true
tags: ["robot", "overview"]
keywords: 
- 
categories: 
- 
description: ""
weight: 10
slug: ""
draft: true # 是否为草稿
comments: true
reward: false # 打赏
mermaid: false #是否开启mermaid
showToc: true # 显示目录
TocOpen: true # 自动展开目录
hidemeta: false # 是否隐藏文章的元信息，如发布日期、作者等
disableShare: true # 底部不显示分享栏
showbreadcrumbs: true #顶部显示路径
cover:
    image: "" #图片路径例如：posts/tech/123/123.png
    caption: "" #图片底部描述
    alt: ""
    relative: false
---

### go2 高层运动

订阅：`/sportmodestate` ，类型为 `unitree_go::msg::SportModeState`

发布：`api/sport/request`，类型为 `unitree_api::msg::Request`



> **unitree_go::msg::SportModeState**
>
> ```cpp
> TimeSpec stamp(); 
> uint32_t errorCode(); //错误代码
> IMU imuState(); //IMU状态
> uint8_t mode(); //运动模式
> /*
> 运动模式
> 0. idle, default stand
> 1. balanceStand
> 2. pose
> 3. locomotion
> 4. reserve
> 5. lieDown
> 6. jointLock
> 7. damping
> 8. recoveryStand
> 9. reserve
> 10. sit
> 11. frontFlip
> 12. frontJump
> 13. frontPounc
> */
> 
> float progress(); //是否动作执行状态：0. dance false; 1. dance true
> uint8_t gaitType(); //步态类型
> /*
> 步态类型
> 0.idle  
> 1.trot  
> 2.run  
> 3.climb stair  
> 4.forwardDownStair   
> 9.adjust
> */
> 
> float footRaiseHeight(); //抬腿高度
> std::array<float, 3> position(); //三维位置
> float bodyHeight(); //机体高度
> std::array<float, 3> velocity(); //三维速度
> float yawSpeed(); //偏航速度
> std::array<float, 4> rangeObstacle(); //障碍物距离
> std::array<int16_t, 4> footForce(); //四个足端力
> std::array<float, 12> footPositionBody(); //足端相对于机体的位置
> std::array<float, 12> footSpeedBody(); //足端相对与机体的速度
> std::array<PathPoint, 10>  pathPoints(); //当前跟踪的路径点
> ```
>
>  
>
> **unitree_api::msg::Request**
>
> ``` bash
> RequestHeader header
> string parameter
> uint8[] binary
> ```
>
> 

对  unitree_api::msg::Request 中的 string parameter 参数进行解析：

消息案例：

``` json
Parameter: [ {
    "t_from_start": 0.0, "vx":0.38878634572029114, "vy":0.0, "vyaw":0.0, "x":0.3143965005874634, "y":0.0, "yaw":0.0
}

,
{
"t_from_start": 0.20000000298023224, "vx":0.35545676946640015, "vy":0.0, "vyaw":0.0, "x":0.3516397178173065, "y":0.0, "yaw":0.0
}

,
{
"t_from_start": 0.4000000059604645, "vx":0.31857556104660034, "vy":0.0, "vyaw":0.0, "x":0.3853694498538971, "y":0.0, "yaw":0.0
}
            
.......
            
]

```

消息含义解释：

- `"t_from_start"`: 从路径开始到达此点所需的时间。
- `"vx"`: 在此点的x方向上的期望速度。
- `"vy"`: 在此点的y方向上的期望速度。
- `"vyaw"`: 在此点的期望偏航速度。
- `"x"`: 此点的x坐标。
- `"y"`: 此点的y坐标。
- `"yaw"`: 此点的偏航角。
