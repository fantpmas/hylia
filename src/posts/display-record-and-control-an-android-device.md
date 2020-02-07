---
title: 'Display, record and control an android device'
socialImage: /images/scrcpy.jpg
date: '2020-02-07'
tags:
  - tech
---
As a mobile QA engineer I find myself recording screen videos almost every day.

I've been using the command line tool [scrcpy](https://github.com/Genymobile/scrcpy) for this for a while now.

It can be used to display your android phone screen, to control it using the mouse and also record.

## Prerequisites

- ADB installed on your computer
- USB Debugging enabled on your phone
- Phone connected to Macbook with USB cable for best results (wifi also possible)

## Benefits

What I like most about this solution is that it is very lightweight and fast. I use Quicktime for iOS and that always takes longer. Being a command line tool you can also script and use aliases for it.

I frequently use the following aliases:

`alias record='scrcpy -t -b2M -m800 --record /Users/thomas/Downloads/$(date +%Y%m%d-%H%M%S).mp4'`

Record in low resolution to use with bug reports, automatically appends a timestamp to the filename and saves it in the same folder

`alias recorddemo='scrcpy -t --record /Users/thomas/Downloads/$(date +%Y%m%d-%H%M%S).mp4'`

Used to record demo videos of new features to showcase, in high resolution

`alias demo='scrcpy -t'`

Used to demo features with touch visible so people can see the clicks, does not record


