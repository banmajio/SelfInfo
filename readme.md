### 个人信息

基础信息：xxx	|	男	|	汉族	|	1997-01-08						    籍		  贯：山西	|	现居地：北京

联系方式：手机：176xxxx4399	|	邮箱：banmajio@163.com	  	应聘岗位：Java开发工程师

### 教育背景

2015.09	~	2019.06						南京信息工程大学滨江学院						计算机科学与技术						本科

荣誉/奖项：院三等奖学金（2015-2016）、院一等奖学金（2017-2018；2018-2019）、院三好学生（2017-2018；2018-2019）、院优秀毕业生（2018-2019）

---

### 擅长技能

- 熟练使用`SpringCloud`+`SpringBoot`架构进行项目搭建，业务开发。
- 熟练使用`MySQL`进行系统业务开发，有一定的SQL调优经验。
- 对`JVM`原理有初步的理解，有一定的JVM调优与内存溢出排查解决经验。
- 熟练使用`Redis`、`Nacos`、`Kafka`、`RabbitMQ`等中间件。
- 熟悉`Docker`、`Linux`等基础使用。

### 工作履历

**xxxx									Java研发工程师							2021.05	~	至今**

**xxxx					            Java研发工程师					    	2019.06	~	2021.05**

---

### 项目经验

#### 课下学习助手小程序&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;xxxx&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2022.4 ~ 至今

【项目描述】：该系统主要面向学员使用，包括学员作业、背单词小程序等模块。其中【背单词】小程序针对不同程度学员，设置强制学及自由学两种模式；并在背词后强制测试，检验背词效果，能够有效帮助学生及教学、服务老师了解学生背词情况。测试数据收集，能够为学生提供每日背词报告，教学服务角色可通过后台随时了解学生背词数据，有效减轻日常背词及阶段测试工作量，提升工作效率，并可对异常情况及时干预，最大程度帮助学生完成背词计划。

【项目架构】：项目采用分布式部署方案，使用SpringBoot微服务进行整体架构的基础构建。该项目使用Redis作为分布式缓存、以MySQL做数据持久化存储、以Kafka作为消息中间件处理消息订阅、以Nacos作为配置中心与服务注册发现中心。

【我的职责】：负责课下学习助手小程序【作业】模块、课下学习助手小程序【背单词】模块的补打卡功能、单词自主测试功能的设计与业务代码开发。

【设计技术】：SpringCloud	|	SpringBoot	|	MySQL	|	Redis	|	Kafka	|	Nacos	|	Redission

- 使用Redis存储学员背词或者测词过程中的进度、来减轻调用接口进行复杂的逻辑判断从而造成的耗时问题。
- 为了解决生成测试任务接口耗时导致用户多次点击造成的并发问题。采用自定义注解对需要防止重复提交的接口进行AOP拦截，通过Redission获取锁，来判断是否为重复提交的请求，从而解决并发问题。
- 使用Kafka订阅微信公众号的订阅与退订消息，对消息内容进行持久化存储，从而完成公众号对学员发送任务提醒消息。
- 使用lambda表达式对列表对象分组生成Map对象，优化业务代码中大量的for循环嵌套查询导致的接口响应耗时问题。

---

#### xxxx管理系统&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;xxxx&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2021.06 ~ 2022.06

【项目描述】：该系统作为xxxx部门教学服务管理综合平台，将教师在课下繁重的教学任务中产生的各种工作办理考核指标迁移到线上，让老师可以更加专注于线下的教学任务。

【项目架构】：基于开源的若依管理系统二次开发。项目采用分布式部署方案，分布式框架使用的是SpringCloud以实现项目的高并发和高可用，并配合使用SpringBoot微服务进行整体架构的基础构建。项目中使用的是Redis分布式缓存、数据存储以MySQL进行存储、异步消息中间件采用Kafka进行消息的订阅、使用Nacos中间件进行服务注册与发现、服务之间的远程调用使用OpenFeign等。

【我的职责】：负责问题学员、正模考反馈、作业批改统计等模块的功能设计与业务开发。以及慢查询优化，服务稳定性提升，系统维护，系统内存溢出系统崩溃问题的排查等。

【设计技术】：SpringCloud	|	SpringBoot	|	MySQL	|	Redis	|	Kafka	|	Nacos	|	OpenFeign

- 在正模考反馈需求中使用乐观锁解决多端操作、多用户操作造成的并发数据一致性问题。
- 通过配置JVM参数提升系统稳定性，并通过MAT、JProfiler等分析工具对dump文件进行分析排查，优化代码解决线上报表相关业务频繁造成系统内存溢出导致系统崩溃的问题。
- 通过Explain关键字对慢SQL优化调优，合理优化索引，从而提高接口响应速度，提升用户使用体验。

---

#### 监控安防视频流媒体服务&emsp;&emsp;&emsp;&emsp;&emsp;xxxx有限公司&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2019.09 ~ 2021.03

【项目描述】：作为增值服务，为其他项目提供监控视频的PC端/移动端直播与点播功能。根据不同项目需求，提供了萤石云接入、海康SDK二次开发、RTSP协议接入、GB28181协议接入四种版本的流媒体服务。

【项目架构】：基于SpringBoot搭建，采用Redis对设备信息进行存储，通过开源流媒体库JavaCV对视频流音频流进行转码封装，使用开源SRS流媒体服务平台进行码流分发推送。

【我的职责】：负责服务搭建，核心代码编写，视频流的转码与分发。

【设计技术】：SpringBoot	|	Redis	|	JavaCV	|	SRS	|	HTTP-FLV

- 使用开源JavaCV库对接不同协议的音视频数据，转码转封装为H5不依赖插件就可以直接播放的音视频流。
- 使用管道流PipedInputStream，PipedOutputStream处理不同线程内的音视频流数据传输。
- 使用Redis存储设备信息，以减少每次任务都要通过sdk接口查询设备信息造成的性能损耗。
- 使用线程池支持并发，对于每一路直播信号进行多线程处理。
- 服务开源至GitHub、Gitee等开源社区，累计获得800+ Star，广受好评。该服务在新疆采油一厂、中石化胜利测井公司等项目中稳定运行。





> 感谢您的阅读，期待与您公事！
