# Ubuntu
## 安装ss
先安装SS
```bash
apt install shadowsocks
```
## 替换配置文件
ss的配置文件在`/etc/shadowsocks/`下面
```bash
cp ./config.json /etc/shadowsocks/
```
## 配置浏览器
### chrome
#### 安装**SwitchyOmega**插件
1. 可以进入[项目地址](https://github.com/FelisCatus/SwitchyOmega)自行编译
2. **推荐** 直接下载[SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega/releases/download/v2.5.10/SwitchyOmega_Chromium.crx)插件
3. 然后通过进入[扩展列表](chrome://extensions/)
4. 将*CRX*文件直接拖入浏览器，完成安装
#### 配置**SwitchyOmega**
5. 新建模式Proxy
6. 协议选择**SOCKS5**，代理服务器选择**127.0.0.1**，端口选择**1080**。
7. 保存模式

## 试运行
在bash下面直接输入
`sslocal -c /etc/shadowsocks/config.json`
在浏览器右上角选择**Proxy**即可上网。

## 加入启动项
在`/etc/rc.local `文件的 `exit 0`前面添加
`sslocal -c /etc/shadowsocks/config.json`
然后保存退出后重启计算机，ss将在每次开机自动后台启动。

# Windows
[windows教程](https://github.com/shadowsocks/shadowsocks-windows)
其中服务器配置请参考config.json
# Android
[Android APP](https://play.google.com/store/apps/details?id=com.github.shadowsocks)
其中服务器配置请参考config.jason
