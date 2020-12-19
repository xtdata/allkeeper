# hadoop-集群更换硬件

hadoop集群更换硬件，主要涉及节点的下线与上线。

这里有个细节，节点是要完全下线，还是临时下线，操作会有点细微区别。

## 节点下线

需要进行如下修改，告诉hadoop集群，我需要排除哪些节点。

hdfs-site.xml 中 添加如下配置

```
<property>
  <name>dfs.hosts.exclude</name>
  <value>/opt/apps/hadoop-2.7.2/etc/hadoop/hdfs.excludes</value>
</property>
```

yarn-site.xml 中 添加如下配置

```
<property>
   <name>yarn.resourcemanager.nodes.exclude-path</name>
   <value>/opt/apps/hadoop-2.7.2/etc/hadoop/yarn.excludes</value>
</property>
```

然后在对应文件添加host即可。nn1、nn2都需要配置。

```
/opt/apps/hadoop-2.7.2/etc/hadoop/hdfs.excludes
/opt/apps/hadoop-2.7.2/etc/hadoop/yarn.excludes
```

然后在namenode节点中执行以下命令，进行刷新节点。

```
hdfs dfsadmin -refreshNodes
```

```
yarn rmadmin -refreshNodes
```

如果只是临时重启，或者更换设备硬件，时间比较短的操作。

在页面的datanode中看到有离开的datanode节点并且显示`Decomissioning`，即可直接关闭进行，然后重启机器即可。

如果是完全下线节点，需要等待数据迁移完成，比如下图，要等待所有的`Under replicated blocks`文件块完成，才可下线。 


## 节点上线

在刚才的2个配置文件中，把节点信息去掉，然后再执行

```
hdfs dfsadmin -refreshNodes
```

```
yarn rmadmin -refreshNodes
```

等待节点回到集群，即可。