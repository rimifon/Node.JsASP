# Node.JsASP

一个 node 版的 “IIS”，支持经典的 JScript 版 asp 语法，并实现了 #include 指令、Session处理、应用缓存等。

进入目录，运行
``` bash
node .
```
即可，默认 HTTP 为 3000 端口，HTTPS 为 4433 端口。也可以指定服务端口（1024以下端口需要 root 权限）：
``` bash
node . 80 443
```
注意，证书 key 文件需要使用 pem 格式。

支持运行多个网站，打开 index.js，编辑第四行，即可添加多个站点。

默认数据库为 SQLite，第一次使用数据库，需要先安装 sqlite3 模块：
``` bash
npm install better-sqlite3
#yarn add better-sqlite3   # 或者用 yarn 安装
```
