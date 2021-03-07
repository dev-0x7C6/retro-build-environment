## Reference build environment for Retro distribution

This is a commplete build enviroment that is integrating **Yocto** and **meta-retro** layer. A starting point to build **RetroArch** system images for PC machines and for embedded machines like RaspberryPi.

Retro distribution is defined by **meta-retro** layer in [retro.conf](https://github.com/dev-0x7C6/meta-retro/blob/zeus/conf/distro/retro.conf). Is partially based on poky configuration file provided by Yocto.

![Raspberry Pi 4 Poky build](https://devwork.space/wp-content/uploads/2020/01/IMG_20200108_205652-scaled.jpg)

## Customization
File [local.conf](build/conf/local.conf) contains default configuration that can be changed. RetroArch and libretro cores releated settings are explained in [meta-retro readme](https://github.com/dev-0x7C6/meta-retro/blob/zeus/README.md)

## Building system images

```sh
#~ git clone --recursive https://github.com/dev-0x7C6/retro-build-environment.git
#~ cd retro-build-environment
#~ source source.me
#~ MACHINE="raspberrypi4" bitbake retro-image-minimal
```

## Support and tests

| Machine         | Layer                                                                             | Build against | Runtime testing | Notice |
|:--------------|:---------------------------------------------------------------------------------:|:----------------------:|:---------------:|:-------| 
| `cubietruck`      | [meta-sunxi](https://github.com/linux-sunxi/meta-sunxi)                           |  Often   | Rarely | Unable to run kms with lima(mesa) | driver
| `intel-core2-32`  | [meta-intel](https://git.yoctoproject.org/cgit/cgit.cgi/meta-intel/)              |  Often   | Sometimes | As pendrive dongle |
| `intel-corei7-64` | [meta-intel](https://git.yoctoproject.org/cgit/cgit.cgi/meta-intel/)              |  Often   | Sometimes | As pendrive dongle |
| `orange-pi-pc`    | [meta-sunxi](https://github.com/linux-sunxi/meta-sunxi)                           |  Often   | Rarely | --- |
| `raspberrypi3-64` | [meta-raspberrypi](https://git.yoctoproject.org/cgit/cgit.cgi/meta-raspberrypi/)  |  Often   | Sometimes | --- |
| `raspberrypi3`    | [meta-raspberrypi](https://git.yoctoproject.org/cgit/cgit.cgi/meta-raspberrypi/)  |  Often   | Sometimes | --- |
| `raspberrypi4-64` | [meta-raspberrypi](https://git.yoctoproject.org/cgit/cgit.cgi/meta-raspberrypi/)  |  Always   | Often | --- |
| `raspberrypi4`    | [meta-raspberrypi](https://git.yoctoproject.org/cgit/cgit.cgi/meta-raspberrypi/)  |  Always   | Often | --- |
| `rock-pi-4a`      | [meta-rockchip](https://git.yoctoproject.org/cgit/cgit.cgi/meta-rockchip/)        |  Often   | None  | Thanks to [@MarkusVolk](https://github.com/MarkusVolk) for sending patches |

## Login
Default user is **retro**, passsword is same as user name. Pulseaudio is configured to work with retro user and is disabled in root account.

## Patches
Please submit any patches against the [retro-build-environment](https://github.com/dev-0x7C6/retro-build-environment) by pull requests.
