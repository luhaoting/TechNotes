> 来源：https://doocs.gitee.io/advanced-java/#/./docs/high-availability/hystrix-introduction

# 01 | 基于Hystrix实现高可用

## 1.1 Hystrix 介绍

**Hystrix 是什么？**

Hystrix 可以让我们在分布式系统中对服务间的调用进行控制，加入一些调用延迟或者依赖故障的容错机制。

Hystrix 通过将依赖服务进行资源隔离，进而阻止某个依赖服务出现故障时在整个系统所有的依赖服务调用中进行蔓延；同时 Hystrix 还提供故障时的 fallback 降级机制。

总而言之，Hystrix 通过这些方法帮助我们提升分布式系统的可用性和稳定性。

**Hystrix 的设计原则**

- 对依赖服务调用时出现的调用延迟和调用失败进行**控制和容错保护**。
- 在复杂的分布式系统中，阻止某一个依赖服务的故障在整个系统中蔓延。比如某一个服务故障了，导致其它服务也跟着故障。
- 提供 `fail-fast`（快速失败）和快速恢复的支持。
- 提供 fallback 优雅降级的支持。
- 支持近实时的监控、报警以及运维操作。

**Hystrix 更加细节的设计原则**

- 阻止任何一个依赖服务耗尽所有的资源，比如 tomcat 中的所有线程资源。
- 避免请求排队和积压，采用限流和 `fail fast` 来控制故障。
- 提供 fallback 降级机制来应对故障。
- 使用资源隔离技术，比如 `bulkhead`（舱壁隔离技术）、`swimlane`（泳道技术）、`circuit breaker`（断路技术）来限制任何一个依赖服务的故障的影响。
- 通过近实时的统计/监控/报警功能，来提高故障发现的速度。
- 通过近实时的属性和配置**热修改**功能，来提高故障处理和恢复的速度。
- 保护依赖服务调用的所有故障情况，而不仅仅只是网络故障情况。

## 1.2 电商网站详情页系统架构



## 1.3 Hystrix 线程池技术实现资源隔离

## 1.4 Hystrix 信号量机制实现资源隔离

## 1.5 Hystrix 隔离策略细粒度控制

## 1.6 深入Hystrix执行时内部原理

## 1.7 基于request cache请求缓存技术优化批量商品数据查询接口

## 1.8 基于本地缓存的fallback降级机制

## 1.9 深入Hystrix断路器执行原理

## 1.10 深入Hystrix线程池隔离与接口限流

## 1.11 基于timeout机制为服务接口调用超时提供安全保护

# 02 | 如何设计一个高可用系统？



# 03 | 如何实现限流？



# 04 | 熔断

## 问题01：如何进行熔断？



## 问题02：熔断框架都有哪些？具体实现原理是什么？



## 问题03：熔断框架选用Sentinel还是Hystrix?



# 05 | 如何进行降级？



