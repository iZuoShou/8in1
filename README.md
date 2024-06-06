

#  8in1 共存脚本+伪装站点
   原作者已回，此版本自用。

## 特性
- 支持[Xray-core[XTLS]]、[v2ray-core]
- 支持VLESS/Trojan前置[VLESS XTLS -> Trojan XTLS]、[Trojan XTLS -> VLESS XTLS]
- 支持不同核心之间的配置文件互相读取
- 支持 VLESS/VMess/trojan 协议
- 支持Debian、Ubuntu、Centos系统，支持主流的cpu架构。
- 支持任意组合安装、支持多用户管理、支持DNS流媒体解锁、支持添加多端口、[支持任意门解锁Netflix](https://github.com/iZuoShou/8in1/blob/master/documents/netflix/dokodemo-unblock_netflix.md)
- 支持卸载后保留tls证书
- 支持IPv6，[IPv6注意事项](https://github.com/iZuoShou/8in1/blob/master/documents/ipv6_help.md)
- 支持WARP分流、IPv6分流
- 支持BT下载管理、日志管理、域名黑名单管理、核心管理、伪装站点管理
- [支持自定义证书安装](https://github.com/iZuoShou/8in1/blob/master/documents/install_tls.md)

## 支持的安装类型

- VLESS+TCP+TLS
- VLESS+TCP+xtls-rprx-direct
- VLESS+gRPC+TLS【支持CDN、IPv6、延迟低】
- VLESS+WS+TLS【支持CDN、IPv6】
- Trojan+TCP+TLS【**推荐**】
- Trojan+TCP+xtls-rprx-direct
- Trojan+gRPC+TLS【支持CDN、IPv6、延迟低】
- VMess+WS+TLS【支持CDN、IPv6】


## 注意事项

- **修改Cloudflare->SSL/TLS->Overview->Full**
- **Cloudflare ---> A记录解析的云朵必须为灰色【如非灰色，会影响到定时任务自动续签证书】**
- **如用CDN又同时使用直连，关闭云朵+自选IP，自选IP(https://github.com/XIU2/CloudflareSpeedTest)**
- **使用纯净系统安装，如使用其他脚本安装过并且自己无法修改错误，请重新安装系统后再次尝试安装**
- wget: command not found [**这里需要自己手动安装下wget**]
  ，如未使用过Linux，[点击查看](https://github.com/iZuoShou/8in1/tree/master/documents/install_tools.md)安装教程
- 不支持非root账户
- **如发现Nginx相关问题，请卸载掉自编译的nginx或者重新安装系统**
- **为了节约时间，反馈请带上详细截图或者按照模版规范，无截图或者不按照规范的issue会被直接关闭**
- **不推荐GCP用户使用**
- **不推荐使用Centos以及低版本的系统，如果Centos安装失败，请切换至Debian10重新尝试，脚本不再支持Centos6、Ubuntu 16.x**
- **Oracle Cloud有一个额外的防火墙，需要手动设置，懒得设置就直接ufw disable**
- **如果使用gRPC通过cloudflare转发,需要在cloudflare设置允许gRPC，路径：cloudflare Network->gRPC**
- **gRPC目前处于测试阶段，可能对你使用的客户端不兼容，如不能使用请忽略**


## [脚本使用指南](https://github.com/iZuoShou/8in1/blob/master/documents/how_to_use.md)、[脚本目录](https://github.com/iZuoShou/8in1/blob/master/documents/how_to_use.md#5脚本目录)



## 安装脚本

- 支持快捷方式启动，安装完毕后，shell输入【**vasma**】即可打开脚本，脚本执行路径[**/etc/8in1/install.sh**]

- Version【当前版本:v2.6.12】

```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/iZuoShou/8in1/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```




