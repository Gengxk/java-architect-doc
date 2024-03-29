# 架构师技术目录

   > 提升性能，开发稳定高效的中间件，解决疑难问题(绝大部门人解决不了那种)，开源库替换验证，设计开发通用的基础组件和高级代码，
    重构架构和设计(向着高内聚低耦合的目标)
      
>  其实关于架构师的工作也并非那么的固定，根据公司的情况不一样，架构师所做的工作与架构师所处的地位也是不尽相同，在有一些小的公司，架构师仍旧是在一线编码，他们除了编码，他们还是需要解决疑难问题，只要是技术上问题，普通开发人员解决不了的他们就得上，不会把程序员的工作与架构师的工作分得那么清楚，当然，有这样经历的架构师技术能力也是很强的，都是得意于这种艰苦环境塑造出来的，大一点公司，架构师的工作就可能相对规范一点，主要参与系统的架构调整及规划，一些技术选型的都需要他们去做，另外，有的公司架构师的职位就和CTO差不多了，关于技术上事情，他们是比较有权威的，当然，这也与个人的一些特点有关，职位高再加上能张罗一些事情，爱出头，擅于扛事，所处的地位自然也会比现有的职能还要高。

***
#### 1. 基础

    进程是操作系统层的，能起到数据隔离的作用，线程调度是cpu完成的。
    
- cpu缓存技术(MESI)

- jvm(Hotspot)
  - jmm
  - 故障调优


- 多线程
      
  - 并行

  - 并发

***
#### 2. 架构技术（微服务）

    分布式特性：CAP（一致性，可用性，分区容错性，分布式中间件都是基于这些特性开发的）

- 分布式事物 2PC/CAP
  - 2PC（强一ng致导致有性能问题）
 
  
- CP/AP（分布式必须实现分区容错性，所以剩下的只能在一致性和可用性之间选择）  
  - BASE基本可用（基本可用，softstate（中间状态），
  最终一致性（一段时间后达到一致性 -> 衰减重试 —> 失败（自动对账或人工处理）


- zookeeper(CP)
  - 数据结构：类似linux文件目录结构，分持久节点和临时节点，
在持久节点下可创建子节点
  - 应用场景：利用watcher特性实现分布式锁（节点抢占）和服务注册

- spring cloud
  - eureka(AP) 服务发现
  - Config 配置中心
  - ribbon 负载均衡
  - feign  restful客户端
  - hystrix 熔断器
  - zuul   网关
  - gateway 网关
  - sleuth 调用连追踪
  - vault  加密管理
  - springboot cli  命令行工具
  - stream 消息驱动
  - bus     消息总线
  - task    任务批处理

- DDD（uml领域建模）
  - 领域模型设计是需求分析的关键步骤。它帮助用户及需求分析人员建立业务概念，确定用户业务的问题域，系统涉及的业务范围等等。

- 安全性
  - API增加身份验证，防止恶意调用，反爬虫

***
#### 3. 规范/部署/发布

- TDD (测试后驱动开发)

- CI/CD

***
#### 4.技术

- 技术栈
  - springboot（webflux）
  - springcloud
  - kafka
  - redis
  - nginx
  - zookepeer
  - disrupotr
  - docker
  - k8s
  
   
