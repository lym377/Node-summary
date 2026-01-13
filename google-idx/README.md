## Usage

```bash
export PORT=8080 UUID=2584b733-9095-4bec-a7d5-62b473540f7a
curl -sSL https://raw.githubusercontent.com/vevc/one-node/refs/heads/main/google-idx/install.sh | sh
```
### Google idx 问题汇总篇 | 使用 Argo 隧道内网穿透，为节点提速

Google idx 官网地址：
https://idx.google.com

Cloudflare 官网地址：
https://www.cloudflare.com

cloudflared 项目地址：
https://github.com/cloudflare/cloudflared

本期项目地址：
https://github.com/vevc/one-node

问题汇总
```
    xhttp 协议不好用，客户端兼容性不好
    直连速度很慢，希望引入 CDN 加速、优选等
    搭建流程正常，测试节点-1
    二次怎么获取订阅信息
```
    加入 Websocket 协议节点

    修改 Xray 配置文件
    https://github.com/lym377/Node-summary/blob/main/google-idx/argo/xray-config-example.json

重启 Xray 进程
```
ps aux | grep -v grep | grep xray | awk '{print $2}' | xargs kill -9
app/xray/startup.sh
```
临时隧道 vs 固定隧道

临时隧道：Cloudflare 提供域名，服务重启，域名会变化

固定隧道：需自备域名，长期使用域名固定不变

Argo 服务安装
```
export ARGO_TOKEN=
curl -sSL https://raw.githubusercontent.com/vevc/one-node/refs/heads/main/google-idx/argo/install.sh | sh
```
设置开机自启
```
argo-ws = "/home/user/WORKSPACE_NAME/app/argo/startup.sh";
```

节点-1问题

修改 alpn 为 h2

封号提醒

Google idx: 谷歌云端服务由于违反规定被禁用，群友及评论区反馈。
Cloudflare: 大面积封禁代理相关服务。










