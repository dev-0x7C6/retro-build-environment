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

## Login
Default user is **retro**, passsword is same as user name. Pulseaudio is configured to work with retro user and is disabled in root account.

## Patches

Please submit any patches against the retro-build-environment by pull requests.

#### Support and tests

I'm currently testing builds with those machines: 
* intel-core2-32 *(meta-intel)*
* intel-corei7-64 *(meta-intel)*
* raspberrypi3 *(meta-raspberrypi)*
* raspberrypi3-64 *(meta-raspberrypi)*
* raspberrypi4 *(meta-raspberrypi)*
* raspberrypi4-64 *(meta-raspberrypi)*
