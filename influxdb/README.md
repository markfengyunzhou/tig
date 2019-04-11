## 数据存储时效

* 默认不删除
```
show retention policies on telegraf;
```

```
name    duration shardGroupDuration replicaN default
----    -------- ------------------ -------- -------
autogen 0s       168h0m0s           1        true
```

* 修改为30\*24h
```
alter retention policy "autogen" on "telegraf" duration 720h replication 1 default;
```
```
show retention policies on telegraf;
```
```
name    duration shardGroupDuration replicaN default
----    -------- ------------------ -------- -------
autogen 720h0m0s 168h0m0s           1        true
```
