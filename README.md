# swarm-UAVs
## 项目简介：
以生物集群行为理论为基础，开发适用于多架无人机的自主飞行算法和框架，实现真实无人机在无GPS、无全局信息、无中央控制情况下完成特定任务。
## 研究内容：
- 1.基于生物启发，建立可适用于实际无人机系统的集群模型，实现仿真，并建立指标体系对结果进行分析。
- 2.研究单个无人机的自主飞行控制技术，包括：
  - （1）无GPS情况下，无人机通过视觉SLAM或光流法等技术实现自主定位；
  - （2）无人机通过视觉、红外线或无线通讯感知周围环境，识别地形、障碍物、其他无人机、目标物；
  - （3）路径跟踪技术，无人机能够精确按照规划的路径飞行。
- 3.搭建集群无人机硬件和软件平台，实现真实无人机集群完成特定任务，如有序穿越门框、向目的地投掷物体等。
## 研究方案：
- 仿真：多主体建模，python，用学院服务器。需要考虑噪声、风速、故障、通信延迟等实际因素。
- 自主定位技术：SLAM参考
- 视觉识别技术：深度学习或者opencv提供的视觉库
- 路径跟踪：
- 无人机硬件平台：
[大疆M100](https://www.dji.com/cn/matrice100?site=brandsite&from=nav) + [manifold2](https://www.dji.com/cn/manifold-2?site=brandsite&from=nav)(manifold2是manifold第二代，基本能兼容)
[大疆M600 Pro](https://www.dji.com/cn/matrice600-pro?site=brandsite&from=nav) + TX2
[Guidance](https://www.dji.com/cn/guidance?site=brandsite&from=nav)
- 无人机软件平台：
[大疆官方mobile SDK教程](https://developer.dji.com/cn/mobile-sdk/documentation/introduction/index.html)
[大疆官方onboard SDK教程](https://developer.dji.com/cn/onboard-sdk/documentation/quick-start/index.html)
[大疆官方mobile sdk源码](https://github.com/dji-sdk/Mobile-SDK-Android)
[大疆官方onboard sdk源码](https://github.com/dji-sdk/Onboard-SDK)




