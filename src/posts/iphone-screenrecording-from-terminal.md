---
title: 'Make iPhone screen recordings using terminal'
socialImage: https://www.fantomas-ls.com/images/ios-screenrecordings-from-terminal.png
date: '2020-12-04'
tags:
  - tech
---

You can make screen recordings from your iPhone using QuickTime or using the iOS built-in feature but you can also do this using terminal.​
The following script makes a screen recording from an iPhone connected to your Mac via a cable, compresses and saves it directly to your MacBook. Say goodbye to e-mailing or AirDropping massive screen recordings to yourself!

You'll need to install [iOS Debug Bridge](https://fbidb.io/docs/installation) (you might need to wrestle with Python on your Mac, you're on your own there), `ideviceinstaller` (`brew install ideviceinstaller`) and `ffmepg` (`brew install ffmpeg`) for this to work.

```bash
#!/usr/bin/env bash
set -e
datetime=$(date +%Y%m%d-%H%M%S)
video=~/Downloads/"$datetime-orig.mp4"
videocompressed=~/Downloads/"$datetime-ios.mp4"
udid=$(idevice_id -l)

idb record video --udid "$udid" "$video" && ffmpeg -loglevel quiet -i "$video" -vcodec h264 -acodec mp2 "$videocompressed"
rm "$video"
echo "Compressed video: ~/Downloads/$datetime-ios.mp4"
```
