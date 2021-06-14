# UcasSrunLoginGo

国科大2021年5月11日起使用深澜校园网，本项目是一个由Go语言编写的，可以在mips架构的路由器下实现认证功能，自动登录。

支持Windows、Linux、macOS和OpenWRT，[点击此处](https://github.com/Risid/UcasSrunLoginGo/releases)下载现有发行版。

> 深澜校园网登录脚本Go语言版。GO语言可以直接交叉编译出mips架构可执行程序（路由器）（主流平台更不用说了），从而免除安装环境。

> 代码逻辑来自 https://github.com/coffeehat/BIT-srun-login-script

> 代码fork自 https://github.com/Mmx233/BitSrunLoginGo ，北理的校园网登录脚本。

**首次运行将生成Config.json文件**

Config.json说明：

```json5
{
 "from": {
  "domain": "124.16.81.61", // 认证网址
  "username": "",           // 学号
  "password": ""            // 密码
 },
 "meta": {
  "n": "200",
  "v_type": "1",
  "acid": "1",              // 可以从登录请求中获得，无需修改；如果登录失败，可以自行抓包确认
  "enc": "srun_bx1"
 },
 "settings": {
  "quit_if_net_ok": true,   // 默认true，有网就不尝试登录
  "demo_mode": false,       // 调试模式
  "dns": "1.2.4.8",         // 北京联通DNS
  "test_url": "https://hm.baidu.com/h.js"   // 用于测试是否有网的网站，务必HTTPS网站，否则会被跳转到认证网址，会被判为有网络。
 }
}
```