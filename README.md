# 1 安装下载工具
https://macappstore.org/rkflashtool/

# 2 使用下载工具给开发板下载img
http://rockchip.wikidot.com/rkflashtool

# 3 编译libusb 在MacBook上
https://gist.github.com/vitorio/c239128dea1a4af23031059d6ca32c35
https://mp.weixin.qq.com/s/e3l9pFUVLfr14nrzypAbTg

# 4 编译kernel
make ARCH=arm64 firefly-rk3308_linux_defconfig
make ARCH=arm64 rk3308-roc-cc-dmic-pdm_emmc.img -j12

内核对应的commit
<img width="499" alt="image" src="https://user-images.githubusercontent.com/11375905/219933164-986b21d7-ce97-4cac-ad32-10023c622e84.png">

编译后使用工具烧录
./rkdeveloptool wl 0x0000A800 boot.img
./rkdeveloptool rd

开机后确认烧录img是否正确
<img width="1074" alt="image" src="https://user-images.githubusercontent.com/11375905/219933225-f68a0c5b-73cd-4060-b064-9c7c48489132.png">


# 5 开发板资料
https://wiki.t-firefly.com/ROC-RK3308-CC/index.html
