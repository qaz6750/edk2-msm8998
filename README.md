# EDK2 UEFI Firmware For Snapdragon 835 (msm8998)

- A broken but working EDK2 implementation for Snapdragon 835 platform.
- This Repo Is Based On [（edk2-porting）Edk2-Msm8998](https://github.com/edk2-porting/edk2-msm8998)
- 中国人请看中文版[Chinese version (中文版)](https://github.com/qaz6750/edk2-msm8998/blob/master/README.zh.md)

## Problem
- First of all, we need to solve the problem of entering Qualcomm 900e when installing AMSS driven by qcsubsys
- The repair of the battery will be tried later

## Resources

[Project website](https://renegade-project.org/)

[Project forum](https://forum.renegade-project.org/)

[Telegram group (recommended)](https://t.me/joinchat/MNjTmBqHIokjweeN0SpoyA)

[Discord group](https://discord.gg/XXBWfag)

QQ chinese group: 697666196 (Main group, full)  996450026 (Second group)  737223105 (Linux/edk2)

## WARNING

- **DO NOT EVER TRY TO PORT IT TO *SONY, SAMSUNG* DEVICES**

- **YOUR UFS WILL BE WIPED CLEAN!!!**

## Supported devices

-  OnePlus 5    (cheeseburger)
-  OnePlus 5T   (dumpling)
-  Xiaomi Mi6    (sagit)
-  Xiaomi Mi Mix 2   (chiron) 
-  LG V30        (joan)
-  Moto Z2 Force (nash)

## Supported devices

[Windows Status Matrix](https://renegade-project.org/#/en/windows/state-frame.html)

## Dependencies

Compiling has been tested on Debian 11 (bullseye) and on Ubuntu 20.04 LTS.

For Ubuntu 20.04:

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git gettext
```

## Building

1.Clone this project 

```bash
git clone https://github.com/qaz6750/edk2-msm8998.git --depth=1
cd edk2-msm8998
```

2.Build this project

```bash
bash build.sh --device DEVICE
```

3.Boot the image

```bash
fastboot boot boot_DEVICE.img
```

(DEVICE is the codename of your phone.)

## Credits
