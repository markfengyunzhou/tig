## 简单安装
   github上找链接下载rpm包
```   
yum install xxx
```

## 源码安装
   * install go
   * install dep
   * go get -d github.com/influxdata/telegraf
   * cd "$HOME/go/src/github.com/influxdata/telegraf"
   * https_proxy="xxx.xxx.xxx.xxx:xxx" make (代理)

