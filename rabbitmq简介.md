# 主流消息中间件介绍

## 主流消息中间件介绍-ActiveMQ

- ActiveMQ是Apache出品，能力强劲的开源消息总线，并且它一个完全支持JMS规范的消息中间件
- 其丰富的API、多种集群构建模式使得他成为业界老牌中间件，在中小型企业中应用广泛！
- 现在用的比较少，相比现在的流行MQ性能一般，传统行业比较常用，高并发大数据力不从心。
- MQ衡量指标：服务性能、数据存储、集群架构

集群架构

Master-Slave模式：高可用服务，主备模式

NetWork：分布式、两种主备模式

       
      
![架构](https://raw.githubusercontent.com/GodNoBug/MQ/master/img/Activemq.jpg)

## 主流消息中间件介绍-KAFKA

Kafka是LinkedIn开源的分布式发布-订阅消息系统，目前归属于Apache顶级项目。Kafka主要特点是基于Pull的模式来处理消息消费，**追求高吞吐量**，一开始的目的就是用于日志收集和传输。0.8版本<u>开始支持复制，不支持事务，对消息的重复、丢失、错误没有严格要求</u>，适合产生大量数据的互联网服务的数据收集业务。性能是很好的

![KAFKA](https://raw.githubusercontent.com/GodNoBug/MQ/master/img/kafuka.jpg)

## 主流消息中间件介绍-RocketMQ

RocketMQ是阿里开源的消息中间件，目前也已经孵化为Apache顶级项目，它是纯Java开发，具有高吞吐量、高可用性、适合大规模分布式系统应用的特点。RocketMQ思路起源于Kafka，它对消息的可靠传输及事务做了优化，目前在阿里集团被广泛应用于交易、充值、流计算、消息推送、日志流式处理、binglog分发等场景。<u>消息顺序性</u>

![](https://raw.githubusercontent.com/GodNoBug/MQ/master/img/rocketMQ.jpg)

- ActiveMQ不适合高并发，传统行业可以考虑
- Kafka主要高性能，不满足消息的可靠性
- RicketMQ高性能，满足消息的可靠性，分布式事务，水平扩展，上一级别的消息堆积，主从自由切换，但是商业版，收费有些功能不对外开放

## 主流消息中间件介绍-RabbitMQ

RabbitMQ是使用Erlang语言开发的开源消息队列系统，基于AMQP协议来实现。AMQP的主要特征是面向消息、队列、路由（包括点对点和发布/订阅）、可靠性、安全。AMQP协议更多用在企业系统内，对数据一致性、稳定性和可靠性要求很高的场景，对性能和吞吐量的要求还在其次。

![](https://raw.githubusercontent.com/GodNoBug/MQ/master/img/RabbitMQ.jpg)

	

# 关于中间件选型：

待续
