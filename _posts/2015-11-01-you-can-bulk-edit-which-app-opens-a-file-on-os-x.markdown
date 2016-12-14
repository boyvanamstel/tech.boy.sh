---
layout: post
title:  "You can bulk-edit which app opens a file on OS X"
tags: [osx]
date:   2015-11-01 13:35:00 +0100
---

Just fire up the Terminal and issue the following command:

`$ open ~/Library/Preferences/com.apple.LaunchServices/com.apple.launchservices.secure.plist`
You might need to reboot your Mac afterwards.

I needed this after deciding I no longer needed [Keka](http://www.kekaosx.com/en/) to open _every compressed file format known to man_ and got tired of seeing its file type icon on every .zip on my Mac.

![The launchservices plist shown in Xcode](/assets/blog/Screen_Shot_2015-12-01_at_13.43.15.png)
