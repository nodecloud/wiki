<!-- TITLE: Koa Configuration -->
<!-- SUBTITLE: Koa Configuration 中间件文档 -->

# Koa Configuration
使用这个中间件会创建一个 /config api，该 api 返回当前服务的实时配置信息。


## 如何使用

``` javascript
import Koa from 'koa';
import KoaConfig from 'koa-configuration';
import ConfigClient from 'nodecloud-config-client';

const app = new Koa();
const client = new ConfigClient(/* ignire */);

app.use(KoaConfig(client));
```

## API

### KoaConfig(client)

config client 详细配置请查看文档 [config-client](http://wiki.nodecloud.cn/nodecloud/config-client)