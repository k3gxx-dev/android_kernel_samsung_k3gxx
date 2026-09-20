# Linux Kernel 3.10.108 for Samsung Galaxy S5 Exynos 3G (k3gxx)

Canonical Linux 3.10.108 kernel source tree and Exynos 5422 Device Tree for the **Samsung Galaxy S5 Exynos 3G (SM-G900H / `k3gxx`)** targeting **LineageOS 18.1 (Android 11)**.

## Overview

- **Kernel Version**: Linux 3.10.108
- **Device Tree**: Exynos 5422 DTBs (`exynos5422-k3gxx_*.dtb`)
- **Key Subsystems**: FIMC-IS camera ISP, WM5110 audio codec, BCM4354 Wi-Fi/Bluetooth, sensorhub, and power management.

## Compilation Guide

Use the archived Linaro ARM toolchain and the canonical defconfig:

```bash
export ARCH=arm
export CROSS_COMPILE="$PWD/archive/exynos5420-ecosystem/armv7-cortex_a15-linux-gnueabihf-linaro-5.2-2016.09.02/bin/arm-eabi-"
make lineage_k3gxx_defconfig
make -j"$(nproc)" zImage dtbs
```

## Output Artifacts

- Kernel image: `arch/arm/boot/zImage`
- Device Trees: `arch/arm/boot/dts/exynos5422-k3gxx*.dtb`
