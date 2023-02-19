# 1 安装下载工具
https://macappstore.org/rkflashtool/

# 2 使用下载工具给开发板下载img
http://rockchip.wikidot.com/rkflashtool

# 3 编译libusb 在MacBook上
https://gist.github.com/vitorio/c239128dea1a4af23031059d6ca32c35

# 4 编译kernel
make ARCH=arm64 firefly-rk3308_linux_defconfig
make ARCH=arm64 rk3308-roc-cc-dmic-pdm_emmc.img -j12
