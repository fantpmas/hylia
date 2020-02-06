---
title: 'Display, record and control an android device'
socialImage: /images/android.jpg
date: '2020-01-02'
tags:
  - tech
---
As a mobile QA engineer I find myself recording lots of screen videos.

Been using the command line tool [scrcpy](https://github.com/Genymobile/scrcpy) for this for a while now.

It can be used to display your android phone screen, to control it using the mouse and also record. 

## Prerequisites

- ADB installed on your Macbook
- Developer options and USB Debugging enabled
- Phone connected to Macbook with USB cable

## Benefits

Wat I like most about this solution is that it is very lightweight and fast. I use Quicktime for iOS and that always takes longer. Being a command line tool you can also script and alias it.

I frequently use the following aliasses:

```
alias record='scrcpy -t -b2M -m800 --record /Users/thomas/Downloads/$(date +%Y%m%d-%H%M%S).mp4'
```

record in low resolution to use with bug reports, automatically appends a timestamp to the filename and saves it in the same folder

```
alias recorddemo='scrcpy -t --record /Users/thomas/Downloads/$(date +%Y%m%d-%H%M%S).mp4'
```

used to record demo videos of new features to showcase, in high resolution

```
alias demo='scrcpy -t'
```

Used to demo features with touch visible so people can see the clicks, does not record

![android](/images/android.jpg)
