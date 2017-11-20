<!-- TITLE: Koa Consul -->
<!-- SUBTITLE: koa consul 中间件文档 -->

# Koa Consul

## 简介

使用这个中间件会创建一个 /health api 供 服务注册中心 consul 调用。

## 如何使用：

``` javascript
import Koa from 'koa';
import KoaConsul from 'koa-consul';

const app = new Koa();

const consulOptions = {
	url: '/health', 
	strategy: monitorData => {return true}
};

app.use(KoaConsul(consulOptions));
```

## API

1. options.url: string

可以通过 options.url 修改默认的 koa route。

2. options.strategy: function(data)

strategy 是一个回掉函数，参数是 node 的一些相关的 运行数据，

可以在回掉函数中写一些策略，如果 return true，则服务健康；如果 return false，则服务状态是 warn。