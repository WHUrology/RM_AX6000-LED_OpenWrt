# What's New:（20251125，22：48）
更新了.config文件
之前编译的文件没有包含passwall，其它功能正常。通过固件网页上传刷新sysupgrade固件测试通过。
今日加入openclash和passwall，passwall2，测试哪个好用。
所以重新编译固件。

GitHub代码更新后导致Fork源代码无法运行，总是报错；整体逻辑没有问题，只有编译后改名以及标签命名等问题存在错误导致无法顺利完成云编译，本地编译没有问题。
所以在Fork源代码后进行了相应的修改得到现在这个版本，只需要Fork我这个仓库过去，直接选择Actions，左边的Redmi-AX6000-padavanonly.yml，选中后在右侧会出现Runworkflow，直接运行，等待大约3-4小时，固件编译完成后会自动上传到Release。


# 借助 GitHub Actions 的 OpenWrt 在线自动编译.

OpenWrt官方有过三种分区固件：OpenWrt stock layout、OpenWrt layout和OpenWrt U-Boot layout。

OpenWrt stock layout对应保留官方分区刷OpenWrt，我称为stock固件。

OpenWrt layout对应的就是hanwckf大佬的不死uboot(ubi 110MB)，我称为uboot固件。

OpenWrt U-Boot layout对应的是HZFrodo大佬的不死ubootmod(ubi 122.5MB)，我称为ubootmod固件。


目前OpenWrt官方、X-Wrt只保留了stock固件和ubootmod固件。

padavanonly和hanwckf大佬闭源驱动固件只支持stock固件和uboot固件。

Lean源码只支持uboot固件。

## Redmi AX6000 闭源驱动固件 源码来源
- padavanonly-[padavanonly/immortalwrtARM](https://github.com/padavanonly/immortalwrtARM/tree/mt7986).
```bash
git clone -b mt7986 --single-branch https://github.com/padavanonly/immortalwrtARM
```
- hanwckf-[hanwckf/immortalwrt-mt798x](https://github.com/hanwckf/immortalwrt-mt798x).
```bash
git clone -b openwrt-21.02 --single-branch https://github.com/hanwckf/immortalwrt-mt798x
```

## Redmi AX6000 开源驱动固件 源码来源
- OpenWrt官方-[openwrt/openwrt](https://github.com/openwrt/openwrt).
```bash
git clone https://github.com/openwrt/openwrt
```
- Lean-[coolsnowwolf/lede](https://github.com/coolsnowwolf/lede).
```bash
git clone https://github.com/coolsnowwolf/lede
```
- ptpt52-[x-wrt/x-wrt](https://github.com/x-wrt/x-wrt).
```bash
git clone https://github.com/x-wrt/x-wrt
```

## Redmi AX6000 不死uboot
- hanwckf-[hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x).

## Redmi AX6000 不死ubootmod
- HZFrodo-[HZFrodo/uboot-mediatek: add support for Xiaomi Redmi Router AX6000](https://github.com/openwrt/openwrt/commit/1613e3340b829ea9aa6da954bf0ff98214b71751).


### 感谢名单（向他们学习才有这个项目）
- [P3TERX](https://github.com/P3TERX/Actions-OpenWrt)
[Read the details in my blog (in Chinese) | 中文教程](https://p3terx.com/archives/build-openwrt-with-github-actions.html)
