# canal监控指标

## 介绍

参考grafana看板

https://raw.githubusercontent.com/alibaba/canal/master/deployer/src/main/resources/metrics/Canal_instances_tmpl.json


## 监控指标

- canal 基础 （cpu、内存、存活节点、jmx、gc）
- 网络带宽
- Canal server与master延时；store 的put, get, ack操作对应的延时。
- sink线程blocking占比；dump线程blocking占比(仅parallel mode)。
- Canal instance 处理binlog的TPS，以MySQL transaction为单位计算。
- 分别对应store的put, get, ack操作针对数据表变更行的TPS
- Canal client请求server的请求数统计，结果按请求类型分类(比如get/ack/sub/rollback等)。
- Canal client请求server的响应时间统计。
- Canal client请求server返回空结果的统计。
- Canal instance ringbuffer中堆积的events数量。
- Canal instance ringbuffer中堆积的events内存使用量。
- client发送请求的QPS，按GET与CLIENTACK分类统计

## 指标讲解 与 运维对接

## 实现

## 参考

- https://blog.csdn.net/heaven_monkey/article/details/105664503
- https://www.cnblogs.com/dalianpai/p/14022235.html
- https://www.cnblogs.com/zh94/p/13937530.html