# 本项目支持的机型列表

>  ### x86-64 工作流

| 🖥️ 工作流分类            | 处理器            | 备注         | luci版本        |
| ---------------- | -------------- | ---------- |---------- |
| x86-64 efi.img.gz  | Intel/AMD | EFI向下兼容传统BIOS |24.10.x |
| x86-64 OpenWrt安装器   | Intel/AMD | ISO格式适用于任何虚拟机和任何物理机 引导后输入ddd来安装 |24.10.x |

>  ### Rockchip 工作流

> ### ~~GL-iNet 和 Cudy MediaTek Filogic 工作流~~ 归入build-wireless-router.yml 

| 📦 SoC平台                         | 型号                           | 厂商       | 处理器型号     | luci版本   |
|-----------------------------------|--------------------------------|------------|----------------|------------|
| MediaTek Filogic (MT7981B, Quad-core Cortex-A53 @1.3GHz) | cudy_tr3000-v1          | Cudy       | MT7981B        | 24.10.x    |
| MediaTek Filogic (MT7981B, Quad-core Cortex-A53 @1.3GHz) | cudy_tr3000-v1-ubootmod | Cudy       | MT7981B        | 24.10.x    |

> ### 斐讯N1 电视盒子
> 构建的是armsr-armv8的rootfs Flippy打包工具打包为OpenWrt镜像<br>
> 用户基数比较庞大 所以我是单独一个工作流 build-n1.yml 支持根据具体 特定内核版本来构建

>  ### MediaTek 路由器工作流（大约103种）build-wireless-router.yml 

| 机型 | 机型 | 机型 |
|------|------|------|

| zbtlink_zbt-z8102ax | zbtlink_zbt-z8103ax | zbtlink_zbt-z8103ax-c |


> ### 硬路由固件格式说明

| 文件类型 | 用途        | 内容               | 常用场景             |
| ---- | --------- | ---------------- | ---------------- |
| FIP  | Arm 固件包   | BL1/BL2/BL31 等   | CPU 上电启动         |
| BIN  | 泛二进制      | Bootloader/内核等   | 烧录或加载执行          |
| UBI  | NAND 文件系统 | UBIFS 镜像         | 嵌入式 NAND 路由器/开发板 |
| ITB  | U-Boot 镜像 | 内核+设备树+initramfs | U-Boot 启动镜像      |

