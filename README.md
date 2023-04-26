 CocosCreator 集成 Pomelo 

下载 ccc-pomelo-chat-client 源码,ccc-pomelo-chat-client/assets/pomelo 拷贝到你的 CocosCreator 项目 assets 目录下。

文件内需要做一下修改
pomelo-client中第5行，将var Protocol = window.Protocol修改为: var Proctocol = require("protocol")
protobuf.js第37行：修改为： (typeof(window) == "undefined"? module.exports:{},this);
protocol.js最后，第350行，修改为： ('undefined' !== typeof protobuf ? protobuf : module.exports, this)
这样在你的项目中即可使用 pomelo-client 相关 API 了。
