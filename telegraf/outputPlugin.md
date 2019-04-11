# add output plugin

## output to clickhouse

需要手动创建表和库

* 下载telegraf源码
```
go get -d github.com/influxdata/telegraf
```
* 下载https://github.com/r3nic1e/telegraf-clickhouse-plugin/blob/master/clickhouse_client.go 

* 移动clickhouse_client.go 到telegraf/plugins/outputs/目录下
```
mkdir telegraf/plugins/outputs/clickhouse
mv clickhouse_client.go clickhouse.go
mv clickhouse.go telegraf/plugins/outputs/clickhouse/
vi clickhouse.go 
修改package clickhouse
```
* 配置
```
[[outputs.clickhouse]]
    # URL to connect
    url = "http://localhost:8123"
    # Database to use
    database = "telegraf"
    # # SQLs to create tables
    #create_sql = ["CREATE TABLE IF NOT EXISTS blablabla"]
    # # Time shift for timezone
    # time_shift = -3600`
```

