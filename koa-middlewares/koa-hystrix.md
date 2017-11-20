<!-- TITLE: Koa Hystrix -->
<!-- SUBTITLE: Koa Hystrix 中间件文档 -->

# Koa Hystrix
使用这个中间件会创建一个 /hystrix.stream API 供 hystrix dashboard 调用，可以查看服务当前熔断器的状态信息。

## 如何使用

``` javascript
import Koa from 'koa';
import KoaHystrix from 'koa-hystrix';

const app = new Koa();

app.use(KoaHystrix({url: '/hystrix.stream'}));
```

## 参考文章
1. [在微服务系统中使用Hystrix, Hystrix Dashboard与Turbine](http://blog.csdn.net/pingyan158/article/details/52764427)