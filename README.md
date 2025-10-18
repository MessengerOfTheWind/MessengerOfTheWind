## 基 本 信 息
---------------------
联系方式：+68 18379883767 | breeze945@163.com             &emsp;&emsp;基本信息：2002-5 | 江西赣州 |共青团员   

## 教 育 经 历
---------------------
- **江西理⼯⼤学**                   **软件⼯程**                   **2020.09 - 2024.06** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; **西南交通大学**                   **计算机技术**                 **2024.09 - 2027.06**<br>
- **英语能⼒**：CET-4 (480) &emsp;&emsp;&emsp;&emsp;CET-6 (430)<br>

## 荣 誉 奖 项
---------------------
**奖学⾦**：本科生国家奖学金，本科一等奖学金*7,硕士一等奖学金*1正⼤鹏安奖学⾦(2/540)、豪鹏科技奖学⾦(2/540) 、⼀等奖学⾦*5（2/80）、国家励志奖学⾦

**荣誉称号**：优秀团员、五好学⽣、五好学⽣标兵、社团优秀会⻓、社团杰出贡献者、社团先进个⼈

**获奖经历**：

- 2023年7⽉ 中国⼤学⽣计算机设计⼤赛软件管理系统赛道国⼆
- 2023年7⽉ 第九届互联⽹＋省级银奖

**项目科研：**
- 《Towards Latency Differential Optimization in Deploying URLLC Service Function Chains》 TSC(CCFA期刊) **学生一作**
- 《Towards Latency QoE Optimization of Deploying URLLC In-Networrk Computing Services in Heterogeneous Computing First Networks》 TNSE(SCI 2区) **学生一作**
  
## 项 ⽬ 经 历
---------------------
**Wifi室内定位系统** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**项⽬负责⼈**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**2022.10 - 2023.03**

- **项⽬概述**：本项目通过采集wifi指纹并训练模型，通过模型精准定位出当前人员所处的室内定位，并对室内人员的定位信息进行管理，在大屏2D平面上进行展示

- **主要⼯作**：<br>
**搭建大屏数据链路**：服务端通过服务器发送事件（SSE）持续推送人员位置信息，客户端订阅并以 ECharts 实时展示全体人员位置。为承载高频更新，引入 Redis 作为位置数据的内存缓存与最新状态存储；同时配置定时任务，将 Redis 中的数据按批写入 MySQL，实现数据留痕与后续统计/报表支持。<br>
**鉴权与权限**：采用 JWT+ RBAC 模式；SSE 端点在握手时校验令牌并绑定用户身份与可见范围，按用户/部门进行数据级过滤；SSE 断线后自动重连，遇到 401 触发 短期令牌续签；<br>
**完成定位算法全链路**：采集训练样本，基于主成分分析（PCA）—数据增强—卷积神经网络（CNN）完成模型训练；将模型部署为后端推理接口；前端提交 RSSI 指纹图 的 POST 请求，后端返回人员坐标并写入 Redis，驱动大屏实时刷新展示。<br>
**系统部署**：以 Nginx 统一入口，承担静态资源托管与反向代理，按路由将请求转发至后端服务；后端应用打包为可执行 JAR 并制作镜像，使用 Docker Compose 定义服务、网络与卷，支持一键部署/更新/回滚及环境变量配置。<br>
- **项目成果**：《基于PAC的轻量化CNN室内定位模型》，一项软著，一项发明专利
<br>
<br>

**桂林理⼯⼤学奖福⾦系统** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;  **项⽬负责⼈** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp; **2023.03 - 2023.05**

- **项⽬概述**：本项⽬实现了财务⼈员对奖福⾦信息的录⼊，部⻔⼈员能够对奖福⾦信息进⾏测算，实现部⻔⼈员权限的动态控制，能够依据需求修改⽤⼾权限<br>

- **主要⼯作**：<br>
**功能实现**：基于**若依（RuoYi）**框架快速搭建业务模块，完成奖福金信息的增删改查与测算流程；引入基于角色的访问控制（RBAC），将权限细化到菜单/按钮/接口级。对测算功能进行优化，让其测算过程流畅，当输入奖福金数据时，能够迅速测算出相应的数据，有点类似网页的输入搜索<br>
**留痕与归档**：前端集成 web-print-pdf，支持一键生成 PDF 并打印，形成每次测算结果的纸质与电子留存。<br>
**优化奖福金测算体验**：实现“输入即算”流式交互，前端 防抖 + 在途请求取消 + 本地缓存，结果毫秒级回填表单；监听任一输入变更即临时禁用提交，待测算完成后自动解锁，确保“所见即所提”的一致性。<br>
**系统运维**：部署于校内内网 Windows 服务器；将后端 JAR、Nginx、Redis 注册为 Windows 服务，实现一键启停；编写批处理/脚本实现数据定时备份与归档，降低服务器故障导致的数据丢失风险。<br>

- **项⽬成果**：与桂⼯财务签署合作协议、已经上线运营，并进行多次维护工作<br>




## 个 人 技 能
---------------------
- 熟悉git操作，gitee和github仓库个人应用主页：[https://gitee.com/MessengerOfTheWind](https://gitee.com/huang-kai-hhh)&nbsp;&nbsp;[https://github.com/MessengerOfTheWind](https://github.com/MessengerOfTheWind)

- 熟悉python、C++、Java等编程语⾔，具备⾯向对象编程能⼒，能够运⽤⼯具实现基础算法以及基本开发

- 掌握Vue、SpringBoot、Mybatis、MybatisPlus等企业级开发语⾔，具有良好阅读国外技术⽂档能⼒

- 熟悉linux操作,熟练运⽤服务器进⾏linux操控，熟练使⽤Xshell⼯具等远程⼯具
