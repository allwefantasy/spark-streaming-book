## Spark Streaming 流式计算  大纲

以一个实例在不断被提出新需求的情况下进行重构，期间介绍Spark Streaming的知识体系，涵盖从开发，测试，打包，发布，监控，性能优化等多个环节。并且对特定知识点融合实际项目经验，深入源码进行阐述原理解答疑问。

1. 架构和组件介绍
1. 编写第一个spark streaming程序
   > - 利用maven构建一个spark steaming程序，消费Kafka(同时也提供一个虚拟的数据源，避免依赖Kafka),并且存储到HDFS上来介绍下如何构建/打包/发布一个streaming程序。包括stanalone/cluster模式

1. 数据源
   > - spark streaming 原生支持的数据源
   >    1.socket file actor
   >    2.kafka flume mqtt（kakfa作为重点，分别阐述kafka两种数据输入的不同）
   > - 如何从InputDStream实现自己的数据源
   > - 利用spark streaming提供的high level api（receiver方式）来接入自己的数据源

1. 处理和输出
   > - 什么是Dstream（主要分为两类）
   > - DStream 常见的操作   
   >    1.transformations on DStream(具体再细分)
   >    2.output Operations on Dtream
   >
   > - accumulators 和 broadcast variables
   > - Spark Streaming 周期调度原理

1. 数据持久化
   > - 持久化到HDFS
   > - 持久化到ES
   > - 持久化到Redis
   
1. 构建单元测试
   > - 编写自己的InputDStream
   > - 使用ManualClock玩转周期调度
   > - 编写自己的ForeachDStream
   > - 使用maven来区分debug,dev,online 三种模式
   
7. 性能调优
   > - 实时性的选择
   > - shuffle调优
   > - gc 优化
   > - 资源的分配原则

参考文献
