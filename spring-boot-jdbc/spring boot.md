##  spring boot





### 数据库JDBC



#### 数据源 

含义： 数据源定义的是**连接到实际数据库的一条路径**而已，数据源中并无真正的数据，它仅仅记录的是你连接到哪个数据库，以及如何连接的，如odbc数据源。也就是说**数据源仅仅是数据库的连接名称**，一个数据库可以有多个数据源连接。

> https://my.oschina.net/hokkaido/blog/85366 

分类

* 嵌入式数据源  ？？
* 通用性数据源 ？？
* 分布式数据源 ？？



### 事务

 从**服务的实现角度**：  Java事务类型有三种：JDBC事务、JTA(Java Transaction API)事务、容器事务。

从**事务的管理角度**：  Java中用到的事务分为本地事务和全局事务

 ![transaction](transaction.png)

事务的原理：

本地事务&分布式事务的使用场景：

​	分布式事务的场景： 转账业务（跨数据库）； 本地事务无法实现一致性

由于JDBC无法实现分布式事务，而如今的分布式场景越来越多，所以，JTA事务就应运而生。	

为了保证分布式事务一致性， 现阶段有 二阶段提交(Two-phaseCommit) 和三阶段提交(Two-phaseCommit)  以及 paxos 算法

其中 2pc 和3pc都无法解决分布式一致性的问题。 



关于事务的理解：

http://www.hollischuang.com/archives/1678

http://www.hollischuang.com/archives/681

### JDBC

JDBC（JSR-221）：

介绍JDBC 核心接口，数据源、数据库连接、执行语句、事务等核心API的使用方法