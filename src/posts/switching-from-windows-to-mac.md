---
title: 'Switching from Windows to Mac'
socialImage: /images/macbook.jpg
date: '2019-10-08'
tags:
  - tech
---

![MacBook stock image, because, why not?](/images/macbook.jpg)

About a year ago I changed jobs and went from a Windows machine to a MacBook Pro. Here are some of the issues I struggled with at first.

# Keyboard & Mouse
## How on earth do I right click?
Click with two fingers on the trackpad. Okay, that was easy.

Using the magic mouse you can either `control + click` or enable right-clicking:

1. Select `Command + space bar`.
2. Type `mouse` and hit enter.
3. Enable `Secondary click`.


## Where the hell is the Delete key?
There is no delete key on the MacBook keyboard (seriously). Use `fn + backspace` instead.

## Command + tab to switch between windows
If you use `command + tab` to switch between windows, it will not work for minimised windows. Instead of minimising windows you can hide them using `command + h`. `Command + tab` works for hidden windows. 

Minimising works differently than on Windows and eventually I got used to this and I actually like it now.

## Lock screen
The default command to lock your screen is `Command + Control + Q` (seriously). You can remap this to `Command + L` if desired: 

1. Select `Command + space bar`.
2. Type `keyboard` and hit enter.
3. Go to `Shortcuts` tab.
4. Select `App Shortcuts`.
5. Click `+`.
6. Select`All Applications`, type in `Lock Screen` as `Menu Title` and enter your shortcut.


## Open finder shortcut
Use `Option + Command + Space` to open a Finder window, opened to Spotlight.
I originally remapped the shortcut to `Command + E` but that was causing conflicts with other software so I ditched that.

## Zoom
Using trackpad:

1. Hold down the control key.
2. Take two fingers and swipe upwards on the trackpad area to zoom in, then use your two fingers to swipe downwards to zoom out.

Using magic mouse:

1. Hold down the control key.
2. Slide your finger to the top or bottom of the mouse.
3. You can also enable Smart zoom on the mouse so double-tapping with one finger also works.

## Shift lock does not work for numbers on AZERTY keyboard

If you have a MacBook with a Belgian AZERTY layout, using Shift lock to be able to enter numbers does not work. Use `French - Numerical` instead.

1. Select `Command + space bar`.
1. Type `keyboard` and hit enter.
1. Select `Input sources`.
1. Use the `+` sign to add `French - Numerical`.
1. Use the `-` sign to remove `Belgian`.

This does not change anything else for the keyboard layout (also, I really should've chosen QWERTY).

## Magic mouse scrolling causes Google Calendar in Chrome to change months

When scrolling down the page while in Google Calendar, Chrome interprets the scrolling with the mouse roller or laptop mouse pad by scrolling through the months, catapulting you into the distant future or past.

Install [this plugin](https://chrome.google.com/webstore/detail/google-calendar-scroll-di/nghndfiaocgpmcbeafglhknklfgddebe?hl=en-US) to disable this behaviour in Chrome.

# Software
## Installing and removing software
First try the App store to see if the app is there (`command + spacebar` > `App store`). Not all apps are available here.

Otherwise, download the app from the vendor's website. In case of *.dmg files, double-click the *.dmg file and drag the application’s icon to your Applications folder. Other apps are packaged in zip files. Unzip them and then drag the application’s icon to your Applications folder. Unmount the .dmg file after installation.

To remove applications, quit the app and drag the app from the Applications folder to the Trash (located at the end of the Dock), then choose `Finder > Empty Trash`.

## Finder
By default the search in Finder searches your complete Mac (again, seriously). To change this to the current folder:

1. Pull down the Finder menu and choose `Preference`.
2. Click on the `Advanced` tab.
3. Pull down the menu under `When performing a search:`.
4. Selecting `Search the Current Folder` from the pulldown menu.

## Zipping
MacOS natively supports (un)zipping. For RAR files you need an external app like [theunarchiver.com](https://theunarchiver.com/).

## Screenshots
MacOS 10.14 Mojave now supports [native annotation on screenshots](https://www.macworld.com/article/3286528/macs/article.html). You can also use [Evernote's Skitch](https://evernote.com/intl/nl/products/skitch) to edit screenshots like SnagIt on Windows.

## Text Editor 

Nothing compares to the powerful text editor beast that is [EditPad Pro](https://www.editpadpro.com/) on Windows (ignore the retro looks, the programme works beautifully). [Visual Studio Code](https://code.visualstudio.com/download) comes close but you have to install a gazillion plugins to even come near EditPad Pro. Especially support for regular expression enabled find and replace is still lacking.