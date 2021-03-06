# passwall plus  

[![GitHub release](https://img.shields.io/github/release/yiguihai/luci-app-passwall-plus.svg)](https://github.com/yiguihai/luci-app-passwall-plus/releases/latest)
[![GitHub downloads](https://img.shields.io/github/downloads/yiguihai/luci-app-passwall-plus/latest/total.svg)](https://github.com/yiguihai/luci-app-passwall-plus/releases/latest)
[![GitHub downloads](https://img.shields.io/github/downloads/yiguihai/luci-app-passwall-plus/total.svg)](https://github.com/yiguihai/luci-app-passwall-plus/releases)
[![GitHub issues](https://img.shields.io/github/issues/yiguihai/luci-app-passwall-plus.svg)](https://github.com/yiguihai/luci-app-passwall-plus/issues)  
[![arm_cortex-a9](https://github.com/yiguihai/luci-app-passwall-plus/workflows/arm_cortex-a9/badge.svg)](https://github.com/yiguihai/luci-app-passwall-plus/actions)  

这是一个简陋的项目，个人精力与学习能力有限仍然有许多的不足之处。目前仅用于测试使用。已经实现:

- 能直连的直连
- 撞墙自动切换服务器
- 自动选择最优线路(国内)
- 自动选择最优dns返回(国内)
    
使用了以下开源项目
    
1. [ipt2socks](https://github.com/zfl9/ipt2socks)，透明代理   
2. [TcpRoute2](https://github.com/GameXG/TcpRoute2) 代理核心   
3. [SmartDNS](https://github.com/pymumu/smartdns) 防止dns污染  

云编译默认使用了[bcm53xx-generic](https://downloads.openwrt.org/snapshots/targets/bcm53xx/generic/)的工具链
不会用云编译的可以编译好二进制文件分别命名为 ipt2socks tcproute2 smartdns 移动到/usr/bin目录并授予执行权限，再自行编译安装ipk

必须包含有一组国外dns像8.8.8.8，主要是针对运营商返回 127.0.0.1 的污染，如 rfa.org jav321.com 和域名黑名单等功能。  
其它的推荐添加使用运营商的dns服务

## 计划
* ~~增加自动编译ipk包~~  
* ~~透明代理替换成ipt2socks~~  
* ~~开启运行时自动修改dns劫持流量到smartdns来处理~~
* 添加Shadowsocks-libev与Obfs混淆插件
* 添加Tor暗网访问功能
* ~~优化Makefile文件代码~~
### 预览图
<img src="https://github.com/yiguihai/luci-app-passwall/raw/master/view/1.jpg" alt="展示图" title="查看图片" />
<img src="https://github.com/yiguihai/luci-app-passwall/raw/master/view/2.png" alt="展示图" title="查看图片" />
