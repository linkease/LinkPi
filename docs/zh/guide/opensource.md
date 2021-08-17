## 构建固件

**建议有动手能力的伙伴们去自行DIY，也可以直接用官方提供的稳定固件。**

自定义OpenWrt固件，先去开源地址：[ImageBuilder+SDK](https://firmware.koolshare.cn/binary/ars2/) 下载ImageBuilder和SDK。


1.准备好安装Debian10 x64或者ubuntu等Linux发行版的电脑或虚拟机；

2.安装必要软件；
```
sudo -E apt-get update
sudo -E apt-get install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs gcc-multilib g++-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler antlr3 gperf
```

3.将ImageBuilder解压到非中文目录；

4.进入ImageBuilder，执行：
```
make image PROFILE=ars2
```

5.成功的话会在bin/targets/realtek/rtd129x/下生成*.install.img固件。




## 构建扩展

1.如果需要控制打包到固件中的软件包，可以在make image时使用PACKAGES参数，例如想要增加luci-app-passwall，并删除luci-app-ttyd，则执行：
```
make image PROFILE=ars2 PACKAGES="luci-app-passwall -luci-app-ttyd -luci-i18n-ttyd-zh-cn"
```

2.默认的软件源只有ImageBuilder内置的，如果需要增加外部的软件源，可编辑ImageBuilder里的repositories.conf，例如增加Openwrt官方的软件源，则repositories.conf的内容如下:
```
src/gz openwrt_base http://downloads.openwrt.org/releases/19.07.7/packages/aarch64_cortex-a53/base

src/gz openwrt_packages http://downloads.openwrt.org/releases/19.07.7/packages/aarch64_cortex-a53/packages

src/gz openwrt_routing http://downloads.openwrt.org/releases/19.07.7/packages/aarch64_cortex-a53/routing


src imagebuilder file:packages
```

3.如果需要增加本地的软件源，则增加一行:src custom file:///usr/src/openwrt/bin/realtek/packages，例如增加已经编译好的lean的软件源(不要使用core和luci仓库，以免冲突):
```
src lean_base file:///home/build/lean-openwrt/bin/packages/aarch64_cortex-a53/base
```





