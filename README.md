## x86固件
[![Build X86 OpenWrt](https://github.com/taanng/x86_Openwrt/actions/workflows/build-x86-openwrt.yml/badge.svg)](https://github.com/taanng/x86_Openwrt/actions/workflows/build-x86-openwrt.yml)

基于Lean大神原版openwrt，固件每日同步最新代码

登陆IP：192.168.1.1 

用户名：root

密码： password

# config测试

1、默认情况只开启 qcow2 编译通过
2、开启 qcow2 基础上添加包




### 参考

- [P3TERX](https://github.com/P3TERX/Actions-OpenWrt)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [immortalwrt](https://github.com/immortalwrt/immortalwrt)



git clone -b v23.05.3 --single-branch https://github.com/immortalwrt/immortalwrt


 git clone --depth 1 https://github.com/vernesong/OpenClash.git
cp -r OpenClash/luci-app-openclash immortalwrt/package/


./scripts/feeds update -a
./scripts/feeds install -a


make meunconfig


cp /mnt/immortalwrt/.config X86/immortalwrt 
cp /mnt/lede/.config X86/lede 
cp /mnt/openwrt/.config X86/openwrt
cp /mnt/lienol-openwrt/.config X86/Lienol 


git config --global user.email "ttzhsz@163.com"
git config --global user.name "sunnoy"
