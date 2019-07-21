# swarm-UAVs
## 项目简介：
以生物集群行为理论为基础，开发适用于多架无人机的自主飞行算法和框架，实现真实无人机在无GPS、无全局信息、无中央控制情况下完成特定任务。
## 研究内容：
- 1.基于生物启发，建立可适用于实际无人机系统的集群模型，实现仿真，并建立指标体系对结果进行分析。
- 2.研究单个无人机的自主飞行控制技术，包括：
  - （1）无GPS情况下，无人机通过视觉SLAM或光流法等技术实现自主定位；
  - （2）无人机通过视觉、红外线或无线通讯感知周围环境，计算距离，识别地形、障碍物、其他无人机、目标物；
  - （3）路径跟踪技术，无人机能够精确按照规划的路径飞行。
- 3.搭建集群无人机硬件和软件平台，实现真实无人机集群完成特定任务，如有序穿越门框、向目的地投掷物体等。
## 研究方案：
- 仿真：多主体建模，python，用学院服务器。需要考虑噪声、风速、故障、通信延迟等实际因素。
- 实际飞行：
  - 1.首先实现单个飞机的自主飞行，利用视觉识别目标，实时规划路径，保持与地面间的通讯，稳定抵达目的地；
  - 2.SLAM技术较为复杂，先在室内进行实验；参考[`slam简介`](https://www.cnblogs.com/gaoxiang12/p/3695962.html)[`高翔slam14讲`](https://github.com/gaoxiang12/slambook)
  - 3.单个无人机实现后，进行双机领导-跟随飞行，无人机之间实时通讯、互相识别、保持距离，稳定抵达目的地；
  - 4.4架以上无人机的集群飞行，利用集群优势更好的完成特定任务，与传统编队飞行算法比较。
- 无人机硬件平台： <br>
[`大疆M100`](https://www.dji.com/cn/matrice100?site=brandsite&from=nav) + [`manifold`](https://www.dji.com/cn/manifold) <br>
[`大疆M600 Pro`](https://www.dji.com/cn/matrice600-pro?site=brandsite&from=nav) + `TX2` <br>
[`Guidance`](https://www.dji.com/cn/guidance?site=brandsite&from=nav) <br>
`无线模块（还未选型）` <br>
自组装[`px4开源飞控`](https://px4.io/)
- 无人机软件平台： <br>
[`大疆官方onboard-sdk教程`](https://developer.dji.com/cn/onboard-sdk/documentation/introduction/homepage.html) <br>
[`大疆onboard-sdk源码`](https://github.com/dji-sdk/Onboard-SDK) <br>
[`大疆Assistant2调参软件`](https://www.dji.com/cn/downloads/softwares/assistant-dji-2-for-matrice) <br>
[`大疆下载中心`](https://www.dji.com/cn/downloads) <br>
[`一个用大疆M100做行人检测的demo`](https://github.com/fan0210/DJIM100-people-detect-track) <br>
[`PX4飞控固件`](https://github.com/PX4/Firmware)




