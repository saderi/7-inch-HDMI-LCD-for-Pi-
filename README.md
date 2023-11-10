# Fixing 7 inch HDMI LCD screen on RaspberryPi 4

## My setup
* LCD: [Touch 7 inch HDMI LCD 1024x600](https://market.samm.com/touch-7-inch-hdmi-lcd)
* RaspberryPi: 4 Model B
* OS: Debian 12

**Step 1:** 

Add following lines in SD card to file `config.txt`:

```
framebuffer_width=1024
framebuffer_height=605
hdmi_cvt 1024 605 60 1 0 0 0
```

**Step 2:** 

Add `video=HDMI-A-1:1200x605@60D` to the beginning of `cmdline.txt` file in SD card
