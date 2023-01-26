My VGA CRT gaming setup for Wii, PS2, and emulators running at 240p through retroarch.

# Getting true 240p through retroarch

### CRU

### Retroarch config

### Dealing with handhelds
We've set  320x240 to our main resolution, but handhelds such as the GBC and GBA work with smaller resolutions. If you just try to run their emulators without any changes to the configuration, you'll notice that the image occupies the correct vertical space, but horizontally it stretches out to the edges of the screen.

Being that we're working with super an weird 1920x240 resolution, we need to calculate the correct width so as to get the same aspect ratio as the original handheld's screen.

Here's how I've done that, using the GBC as an example:

1. Get the handheld's aspect ratio
    * 10:9 for the GBC
2. Our resolution has an aspect ratio of 8:1, so multiply that by the height of the handheld's aspect ratio
    * 9, in this example, so our new aspect ratio becomes 72:9
3. Divide our new aspect ratio's width by the aspect ration's width of the handheld.
    * 72/10 = 7.2
4. Get that value and multiply by the handheld's horizontal resolution
    * 7.2 * 160 = 1152

With this new resolution we'll add an override for the handheld's emulator core, so that this resolution only get's used with the correct emulator. Here's how that looks like:

```
aspect_ratio_index = "23"
custom_viewport_height = "144"
custom_viewport_width = "1152"
```

The emulator's image will not fill the entire screen, so feel free to use to use some overlays. Here's my results:

![handhelds](images/handhelds.jpg)


# Wii & PS2
The Wii and PS2 can be connected to the CRT Monitor using a Component to VGA adapter. This one I've got allows you to switch between scaling resolutions (starting at 480p itself) and aspect ratios, and it also allows for picture adjustments.

You can find Component to VGA adapters on [Aliexpress](https://pt.aliexpress.com/item/1005002393774648.html?spm=a2g0o.detail.1000060.1.cc6a72a4Lg4Y9k&gps-id=pcDetailBottomMoreThisSeller&scm=1007.13339.291025.0&scm_id=1007.13339.291025.0&scm-url=1007.13339.291025.0&pvid=8be36fc2-dae1-4634-a140-6ffe1f39f0dd&_t=gps-id%3ApcDetailBottomMoreThisSeller%2Cscm-url%3A1007.13339.291025.0%2Cpvid%3A8be36fc2-dae1-4634-a140-6ffe1f39f0dd%2Ctpp_buckets%3A668%232846%238116%232002&pdp_ext_f=%7B%22sku_id%22%3A%2212000020523449551%22%2C%22sceneId%22%3A%223339%22%7D&pdp_npi=2%40dis%21BRL%21430.93%21258.55%21%21%21%21%21%402101f6b116747343014295494ed6a9%2112000020523449551%21rec&gatewayAdapt=glo2bra) (Not recommending this seller, this is just the first one I've found that looks just like the converter I have)
