# 骁龙835(MSM8998)的EDK2 UEFI固件

- **在编译该项目前，请确定你有一定的Linux常识，以下步骤已经是最简单的方法，如果你看不懂，那么请使用Releases中的编译成品**
- **此存储库基于[Edk2-Msm8998](https://github.com/edk2-porting/edk2-msm8998)**

## 资源

[项目官网](https://renegade-project.org/)

[项目论坛](https://forum.renegade-project.org/)

[Telegram英语交流群](https://t.me/joinchat/MNjTmBqHIokjweeN0SpoyA)

[Discord英语交流群](https://discord.gg/XXBWfag)

QQ中文交流群: 
主群：697666196 (已满，人数小于1900后开放)  
二群：996450026        
摸鱼专用群：737223105（需具有一定知识储备并正确回答入群问题）     
情感交流群：991796138（仅限邀请）       
核心管理群：766060878（暂不开放）


## 警告

- **请勿尝试移植到任何索尼和谷歌设备上**

- **你的UFS会被清空!!!**

## 已支持的设备
1. 摩托罗拉 Z2 Force  (nash)
2. 小米 MIX2         (chiron)
3. 小米 Mi6          (sagit)
4. LG V30            (joan)
5. 一加5t             (dumpling)
6 一加5             (cheeseburger)

## 依赖

Ubuntu 20.04:

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git gettext
```

## 构建

**不建议使用Ubuntu 18.04版本，请使用Ubuntu 20.04或以上版本**

1.克隆此项目（默认使用国内fastgit镜像加速）

```bash
git clone https://hub.fastgit.org/qaz6750/edk2-msm8998.git --depth=1
cd edk2-msm8998
```

2.编译此项目（默认使用fastgit加速submodule克隆，若不需要请删去 `--chinese`）

```bash
bash build.sh --chinese --device DEVICE
```

3.启动镜像

```bash
fastboot boot boot_DEVICE.img
```

(请将DEVICE替换成你的设备代号.)

## 贡献