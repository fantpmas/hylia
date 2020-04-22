---
title: 'Take Android and iPhone screenshots using terminal'
socialImage: https://www.fantomas-ls.com/images/screenshots-using-terminal.png
date: '2020-04-20'
tags:
  - tech
---

Here's a handy little script to take screenshots from a connected iPhone and/or Android device and save them directly to your MacBook. Yay, no more e-mailing or AirDropping screenshots to yourself!​

```bash
#!/usr/bin/env bash
set -e
datetime=$(date +%Y%m%d-%H%M%S)
adb get-state 1>/dev/null 2>&1 && adb exec-out screencap -p > ~/Downloads/"$datetime-android.png" && sips -Z 1024 ~/Downloads/"$datetime-android.png"
idevice_id -l | grep -q '\d' && idevicescreenshot ~/Downloads/"$datetime-ios.png" && sips -Z 1024 ~/Downloads/"$datetime-ios.png"
```

It first checks if an iPhone or Android device is connected and then saves a screenshot to your `Downloads` folder on your MacBook. The name contains the timestamp and a `-android` or `-ios` suffix. Screenshots are automatically resized to make them smaller so Jira doesn't freak out. 

For iOS you need install `libimobiledevice` (`brew install libimobiledevice`). As usual, USB debugging is required for Android.