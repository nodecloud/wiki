<!-- TITLE: Koa Prom -->
<!-- SUBTITLE: Koa Prom 中间件文档 -->

# Koa Prom
使用这个中间件会创建一个 /metrics API 供 [prometheus](https://prometheus.io) 监控系统调用，监控服务的运行情况。

## 如何使用

``` javascript
import Koa from 'koa';
import KoaProm from 'koa-prom';

const app = new Koa();

app.use(KoaProm({url: '/metrics', register: register}));
```

## API

1. options.url
自定义路由地址，默认为 /metrics。

2. options.register
详细配置请查看 [prom-client](https://github.com/siimon/prom-client)。