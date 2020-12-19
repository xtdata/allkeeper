# allkeeper

## 简介

`all` `keepeer` 

寓意所有的管理员；

包括但不限于大数据相关组件所有的管理 主要实现对各个组件的运维和监控；

这是一个`文档`类的项目，以文档的形式呈现主要讲解对各组件的运维、监控；

本文档中的操作主要使用`prometheus`+`grafana`实现，后续可能会更新其他老牌监控；

## 目录结构

```
/
├── README.md            项目介绍
├── md-format-mac        对非空目录自动覆盖生成README.md文件并索引当前文件和目录，自动跳过空目录
├── md-format-mac.exe    对非空目录自动覆盖生成README.md文件并索引当前文件和目录，自动跳过空目录
├── 监控相关              监控生态系统 与 监控指标 相关文档
│   ├── 监控指标
│   └── prometheus生态
└── 运维相关              组件运维的相关文档，运维程序、安装部署等
    ├── hbase
    ├── spark
    ├── zookeeper
    ├── hadoop
    ├── hive
    └── presto
```

## 目录导航

- [监控相关](./监控相关/README.md)  
  - [监控指标](./监控相关/README.md)  
  - [prometheus生态](./prometheus生态/README.md)  
- [运维相关](./运维相关/README.md)  
  - [hadoop](./运维相关/hadoop/README.md)  
  - [zookeeper](./运维相关/zookeeper/README.md)  
  - [spark](./运维相关/spark/README.md)  
  - [hbase](./运维相关/hbase/README.md)  
  - [hive](./运维相关/hive/README.md)  
  - [presto](./运维相关/presto/README.md)  



## 注意事项

- [整体文档规范](./其他/整体文档规范.md)
- [PR流程](./其他/PR流程.md)
- [监控类文档规范](./其他/监控类文档规范.md)
- [运维类文档规范](./其他/运维类文档规范.md)





