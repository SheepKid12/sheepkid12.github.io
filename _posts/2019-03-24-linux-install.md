---
title:  "Making the switch from Windows to Linux - my experiences"
category: blog
date:   2019-03-24
---

*My personal Windows -> Linux experiences.*

Well, I finally did it: I made the switch from Windows to Linux (KDE Neon user edition is what I went with). Here's what I had to go through to get it to work.

This is something I had wanted to do for **MONTHS**, and since Windows had finally pissed me off enough with the wireless dropping out randomly, I gave up and nuked it. This post documents that entire process from start to finish.

For anyone curious: My laptop is a Dell Insiron 3558 with an i5-5200U processor & 8GB of RAM.

This post was last updated: September 9, 2020. Everything below is considered "day 1".

# Installation

Installing KDE Neon was easy: copy the ISO to a USB drive with Rufus. Then I had to disable Secure Boot and then boot to the USB. Installation was smooth enough, other than this issue where every time I tried to mount my external drive (which is a Western Digital drive), the USB (install media?) would unmount itself, but the external drive was "mounted" (I think nothing showed up when it eventually loaded). One reboot and an install later, and that issue was solved.

# Package Installation

I have a script that "should" install everything I need, but when I needed it the most, it failed on me. The problem came from an untested line or 2 of code that would check for the virtualbox repository file (`/etc/apt/sources.list.d/virtualbox.list`) before adding it. All I had to do to fix that was add an `echo "nothing"` line into the else statement. During this process, I was going through and copying files from the external drive mentioned earlier, and that froze the terminal window I was on, which was fun. Closed it and ran `sudo dpkg --configure -a` and went on. I also had to re-run the apt install list to actually install everything, so I don't know what the dpkg reconfigure thing was attempting to do.

# Extra Tweaks

I've had to make one minor tweak, and that was for the touchpad. I like to have palm detection on so I don't move my mouse when I'm typing something, but I can't enable it from the system settings in Plasma (I think this has since been fixed in newer Plasma versions). I had to look up how to enable it and now it works just fine. This is what later broke my system on a reboot (as you'll see below).

_If you count adding widgets as tweaks, then that's what I also did. I added the sticky notes, weather, and the time. I also did some slight tweaking to the taskbar so it resembles Windows more (and to fit my workflow). These have since been removed, so all I see is just my wallpaper._

After all that nightmare was complete, I am left now with a fully functioning KDE Neon install that works just fine. Am I happy with what I've done? Yes.

# Even Linux isn't safe from me breaking it

Note to self: Do NOT follow steps from StackExchange/Overflow if you're unsure about what you're being told to do (this has gone through multiple wordings to end up here somehow). 

I wanted to get my touchpad to work properly with palm/edge detection, and the post I was following said to make a file in the X11 directories for it to apply on startup (which I copied line-for-line from the post). Well, it did. Guess what happened next? My install was temporarily fucked. I was almost ready to give up until I thought: "what if it was the touchpad file?" (or something like that). Removed it and I was back in. One sigh of relief later, and that install was perfectly fine.

# Day 2

MUCH better than day one. No major breakage here, and I got the rest of my apps working (specifically Telegram and DesMuMe, because pirate applications and my Pokemon HeartGold save). Still unsure of 2 things: default media player and iTunes (yes, I know. I *had* an iPhone). VLC has been my go-to for now, but I also have Lollypop installed, and can't decide which one to work with. I know that VLC is supposed to get an update with a new UI in version 4.0 (still hasn't happened, even 1 year later from initial post writing), and when that comes out I might use VLC for my music and remove Lollypop. Everything else is just fine.

Second thing is iTunes. I can either use Google Play Music and sync music that way, but that's a pain in the rear end (and it would take a lot of time), OR I could use a Windows VM (defeating the purpose of switching to Linux in the first place) with a shared folder with my music, and just use it that way.

I will (if I remember too) update this with whatever option I go with. So far the easiest looks like using Google for music management. This means I would have to re-tag all of my music to match the way Google does it (I even had a script for Mp3Tag that would do that, but it broke), and I don't want to have to go into every song and edit it's details on the web version.

2020 edit: I have since moved to a Pixel 3a XL, meaning I can use apps like syncthing (which is what syncs my music and pictures between my laptop and my other devices).

Also KRunner. Seems like it could be a very useful feature, so I will need to use it and see what my opinion on it is.

# Day (I forgot)

I forgot to update this with things from the previous days, and that's because there's nothing interesting to post anymore. Had to fix some issues with ruby gems (bundler, which is part of what makes this page work) not being detected, and that fix is now in the install script I've mentioned. I also had some weird issues with my XBox controller acting like a mouse (this required the risky X11 tweaks again, only this time it worked). I did forget about using KRunner becuase I only use the search from the application launcher.

I'm calling this a success. 

I was able to migrate everything I do from closed-source Windows 10 to Linux. There were high points and low points through this entire process (specifically the touchpad, which was a major low point). Once those were sorted out, I'm left with a very usable system that does what I want it to do without the tracking Microsoft does on Windows 10 (even down to Windows 7, which is sad).
