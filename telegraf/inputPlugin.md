## add input Plugin

# clickhouse监控

* github.com/ClickHouse-Ninja/telegraf 有添加clickhouse input plugin ，尚未merge到influxdata/telegraf，下载github.com/ClickHouse-Ninja/telegraf，从源码安装
```
  go get -d github.com/ClickHouse-Ninja/telegraf
  
```
* 复制github.com/ClickHouse-Ninja/telegraf 到github.com/influxdata/telegraf  
```
 cp -r $HOME/go/src/github.com/ClickHouse-Ninja/telegraf $HOME/go/src/github.com/influxdata/ 
```
* 从源码编译
```
cd "$HOME/go/src/github.com/influxdata/telegraf"
https_proxy="xxx.xxx.xxx.xxx:xxx" make (代理)
```
