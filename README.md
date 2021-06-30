# 重要更新
2021年6月18日，上游大雕全面更新了最新代码，受影响，60+或60+o版本升级61版本的，建议重新安装，如果不想刷U盘全新安装，也可以用升级脚本升级，只是选择是否保存配置时，选“n”

2021年6月6日，加入科学上网常用ipk输出Releases
每日定时更新最新科学上网插件IPK
使用方式：先去Releases下载需要更新的ipk [点我跳转](https://jcnf.xyz/ipk)
* 软路由后台-系统-软件包-过滤器-查找你要替换的IPK（如passwall，你就搜passwall就行）-移除
* 下载下面对应的IPK文件， 软路由后台-系统-文件传输-选择本地文件-选择ipk上传-上传文件列表-安装

2021年5月24日，同步更新F大佬的快照功能
![增加快照功能](https://cdn.jsdelivr.net/gh/Netflixxp/N1HK1dabao/img/kuazhao.jpg)

使用方法：固件新刷入或采用新版的 update-xxx-openwrt.sh 脚本升级之后就具备了快照功能，工具包名称：由于取名困难，故采用了 flippy 为命令名称（/usr/sbin/flippy)，在ssh或ttyd下输入即可，全程中文菜单，全交互式操作。
# 特别提醒
不要盲目追新，仓库自动打包的固件或插件，均为最新的版本，最新版本意味着有BUG；如果之前固件使用稳定，无需追新。
总结一句话：**追新有风险、更新须谨慎**

# +和+o的版本区别
+的内核版本较新；+o的版本相对+的内核更稳定；f大不太建议N1等盒子使用+的版本，因此比较推荐使用+o的版本。


此项目基于flippy的56+o打包N1和s905X3 （hk1等）的openwrt，为jcnf个人正在使用的固件版本。openwrt来自我自己的另一个项目[N1Openwrt](https://github.com/Netflixxp/op-)

# 默认IP及密码
默认IP 192.168.1.1  密码 password

# N1全新安装
* 下载对应版本固件
![固件链接地址](https://cdn.jsdelivr.net/gh/Netflixxp/N1HK1dabao/img/sj.png)
* 将固件写入U盘或TF卡 推荐写盘软件 [rufu](https://rufus.ie/zh/)或者[balenaEtcher](balena.io/etcher/)任选其一
* 插入U盘启动盒子，输入192.168.1.1进入后台
* 在系统——TTYD终端——输入用户名root；密码password
* 输入安装命令 `./install-to-emmc.sh`
* 如果显示挂载失败，重新执行上述安装命令`./install-to-emmc.sh`

# N1在线升级方法
* cd /mnt/mmcblk2p4
* wget 升级脚本下载.sh后缀文件 [点这里跳转](https://github.com/Netflixxp/N1HK1dabao/releases)
![固件链接地址](https://cdn.jsdelivr.net/gh/Netflixxp/N1HK1dabao/img/zx.png)
* wget .gz后缀名的固件链接,鼠标右击后缀.gz文件获取链接地址 [点这里跳转](https://github.com/Netflixxp/N1HK1dabao/releases)
* gzip -d 上一步下载的固件全名
* chmod +x *.sh
* ./升级脚本名字 img固件名

# 插件包括
![插件列表](https://cdn.jsdelivr.net/gh/Netflixxp/N1HK1dabao/img/lb.png)
* SSR-Plus
* passwall
* openclash
* hello word
* Bypass
* Argon主題 
* docker-ce
* AdGuard Home
* 实时监控
* TTYD终端
* 动态DNS
* UPdp
* AdGuard Home
* 网易音乐解锁
* 京东薅羊毛
* Frp
* 无线wifi
* CPU性能调节

# 自动更新说明
固件采用自动编译，Acrions将会在每天监控上游代码是否更新，如passwall ssrp等，一旦检测到上游代码更加将会自动编译打包，于每天上午7时30分发布最新版固件。

# N1新版固件如何刷

非54+o版升级到55+o版，如果一直卡在fdisk失败那里的解决办法：一是再多试几次，如果还不成功，则需要手动清空分区表然后再重试，具体命令:
```
  dd   if=/dev/zero   of=/dev/mmcblk2  bs=512  count=1  &&  sync
```

# [购买奈飞正规合租车](https://www.vip6.pro/?uid=IwUL03C37v90/#/)

# 感谢
 * [flippy](https://www.right.com.cn/forum/space-uid-285101.html)提供内核
 * [coolsnowwolf/Lede](https://github.com/coolsnowwolf/lede)提供源码
 * [mingxiaoyu](https://github.com/mingxiaoyu)提供自动编译脚本
 * [hibuddies](https://github.com/hibuddies/openwrt/)提供源码