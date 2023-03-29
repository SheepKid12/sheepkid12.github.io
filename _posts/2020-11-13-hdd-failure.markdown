---
title:  "HDD Failure - My First Experience"
category: blog
date:   2020-11-13
---

*Otherwise known as "the worst experience (if you're not prepared)"...*

I don't know how I was able to go for so long without experiencing one of the worst feelings in all of tech: seeing that your spinning rust drives have given up. There's a time for everyting, and today (date this was posted) was that day...

I've been considering purchasing a Synology DiskStation NAS for a better backup solution (compared to a WD Passport and rsync), and to try to keep costs down as low as I possibly could, I decided to attempt to salvage some old drives and re-use them. **This turned out to bite me in the rear. Long story short: my parents figured out I had torn apart their laptops for the drives.** One of those drives was an HGST 1TB drive (the 2.5" size), and all was looking up until just recently, when (during testing with the drive plugged into my Raspberry Pi 4 as a test jellyfin server), I started to notice slower R/W speeds. 

2 things to note here: I've never heard about HGST until taking apart 2 ASUS laptops for their drives, and 2: this drive did suffer a partial fall off the table (where it was just hanging by the usb connector). 

*I think the second thing is what lead this drive to it's inevitable doom, but I have no substantial evidence to prove or disprove that.*

Attempting to boot to Ultimate Boot CD on an old HP laptop immediately brought up an error saying that (based off SMART data) the drive was going to inevitably fail. Built-in diagnostics failed to even complete a short scan of the drive.

Finally, once I was in UBCD, a quick open and reading of the SMART data from HDAT2 gave me my answer: the raw read/write error value was going up, and there were pending sectors on the drive (which after some quick research, those look to be uncorrectable blocks).

To me, this drive is nothing more than junk, since I am not willing to potentially loose data in the case of me actually using this in the eventual Synology NAS I get. At least this was a salvage drive that I backed up beforehand...

I eventually smashed the drive with needle-nosed plyers...
