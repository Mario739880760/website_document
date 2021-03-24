GitHub的服务器在国外，有时候加载速度慢甚至无法访问是一件很头疼的事情，网上看了很多教程，但是解决效果都不太明显甚至不能解决

下面给大家介绍一种亲测有效的方法（注：作者在西北地区测试，按理其他地区应该都能有效）

原理：绕过DNS解析，直接使用本地DNS记录进行直接跳转

打开命令符：win+R，输入cmd，回车即可调出命令符

ping：在命令行中输入ping http://github.com，记录红框中的IP

dns查询https://link.zhihu.com/?target=http%3A//tool.chinaz.com/dns%3Ftype%3D1%26host%3Dgithub.com%26ip%3D

修改windows/system32/drivers/etc/hosts

刷新本地DNS缓存
打开命令提示符，输入：ipconfig /flushdns

返回显示：
Windows IP 配置
已成功刷新 DNS 解析缓存
