## Reference environment for Retro distribution

![Raspberry Pi 4 Poky build](https://devwork.space/wp-content/uploads/2020/01/IMG_20200108_205652-scaled.jpg)

## Building

```sh
#~ git clone --recursive https://github.com/dev-0x7C6/retro-build-environment.git
#~ cd retro-build-environment
#~ source source.me
#~ MACHINE="raspberrypi4" bitbake retroarch-image-minimal
```

I'm currently testing builds with those machines: 
* genericx86_64
* genericx86
* raspberrypi4

But feel free to test other machines as well.

## Patches

Please submit any patches against the retro-build-environment by pull requests.
