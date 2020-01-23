## Reference environment for Retro distribution

![Raspberry Pi 4 Poky build](https://devwork.space/wp-content/uploads/2020/01/IMG_20200108_205652-scaled.jpg)

## Building

```sh
#~ git clone --recursive https://github.com/dev-0x7C6/retro-build-environment.git
#~ cd retro-build-environment
#~ source source.me
#~ MACHINE="raspberrypi4" bitbake retroarch-image-minimal
```

#### Support and tests

I'm currently testing builds with those machines: 
* intel-core2-32 *(meta-intel)*
* intel-corei7-64 *(meta-intel)*
* raspberrypi3 *(meta-raspberrypi)*
* raspberrypi3-64 *(meta-raspberrypi)*
* raspberrypi4 *(meta-raspberrypi)*
* raspberrypi4-64 *(meta-raspberrypi)*

But feel free to test other machines as well.

## Patches

Please submit any patches against the retro-build-environment by pull requests.
