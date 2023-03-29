---
layout: single
title:  "Geek Squad and the Laptop with WiFi Issues"
category: blog
date:   2018-11-02
---

*"Geek" Squad, huh? More like "people who don't know what they're talking about squad".*



Oh boy, here's a post about me ranting about how I dislike Geek Squad. I personally dislike Geek Squad, but since it's all my parents know, I have to go with it. The story here starts a few months back, when I hear that the laptop in question (an old HP laptop) was having WiFi issues. Me being the one who knows (most of the times) how to fix issues like this, I tried some things to try to see if I could single out the problem.

Here's exactly what I tried:

1. Drivers (downgrading and reinstalling)
2. Windows troubleshooting (to make sure if it's a common issue, it's fixed)
3. Different OS (to make sure no viruses were causing the issue)

Which one do you think fixed the issue permanently? Turns out, none of them did. Drivers and troubleshooting were temporary fixes, and Linux was showing the same issues.

2020 edit: holup there on that Linux claim. How on earth was Linux showing the same issue?

I make the initial assumption that the WiFi card is fucked. **Keep this in mind when I start describing my experience with Geek Squad.**

## Day 1

My family arrives at the Best Buy where they have their Geek Squad people. Only one person's there (I find this funny), and they have to schedule us in for an appointment. No big deal, just walk around the store for a little bit and we're good.

The appointment time comes around, and we describe the issue. He goes for the first thing I did, which was drivers. I even mention that I tried this, and he makes the claim that the wrong drivers were being installed. Here's where I will get into some r/quityourbullshit territory.

How would Windows install the wrong driver, when it knows what hardware was there before?

2020 edit: hopping in here again to add to the quityourbs claim here. Even clean installing Win10 will pull all the correct drivers on, so no incorrect driver bull could have happened here (unless somehthing went very wrong somehow). This claim was tested on an OLD (came with Win7 old) HP laptop for Android FRP bypassing (I'll put a post up about that soon).

I think that the Geek Squad person uninstalled and reinstalled the driver, which if you remember from earlier, I said I did this. The first signs of shit were showing up, and it only gets worse.

Either way, it was "fixed", and the moment my family gets back home, what do you think happens? **It breaks again.**

## Day 2

Longer wait time this time around, so we stay at Best Buy just walking around, eventually stopping by the Nintendo Switch demo and staying there for most of the time. It's unrelated to the Geek Squad thing, but whatever.

After what seems like hours, the time finally comes for round 2. It's the same person who tried the previous time, so this will be fun.

We tell the person that it broke again, but this time, Windows Activation was fucked over. He now jumps to the claim that the hard drive/OS is corrupted, and that the possibility of a rootkit is a thing. First off, this laptop is old, so I expect slower performance. **Let's talk about that rootkit...**

Newer systems have UEFI (Unified Extensible Firmware Interface), and only 1 known rootkit exists ([LoJax](https://www.welivesecurity.com/2018/09/27/lojax-first-uefi-rootkit-found-wild-courtesy-sednit-group/)). The problem with that is, this person says that AV software can't scan for it. If that's the case, then why does your couple hundered dollars AV scan for them (Webroot)? Oh, they hide from Windows? Didn't you ever think that AV's could scan processes? Maybe I'm incorrect in what I just said, but that part somewhat made me mad. 

Back on topic, I mention that I had used a Linux USB to test, and this guy says something about Tails. **Oh yeah, this is the same person who tried to help me when my laptop stopped booting (I mention Linux/Ubuntu, he mentions Tails). I thought I remembered this person from somewhere.** I say something back about Xubuntu 18.04, and he says something about the rootkit having the ability to run in Linux, and that their "diagnostics software" is the only thing that could find the real issue. Back onto the rootkit I guess. I did some research and found out that the part that could potentially control your hardware (RWEverything) only seems to have Windows binaries. Also, what does your diagnostics software run on? Maybe Linux, which is what I had tested on at the begining of this mess.

All of this for $200+ in a tech support plan, and we still had an only partially fixed laptop still, as it broke **again**. I will update this when day 3 comes around for this laptop, as my family is wanting to go back. 

This time, I have proof of 3 things: Windows troubleshooting showing that it could be driver or hardware issues (it's hardware), Webroot and Malwarebytes and their ability to scan for rootkits, and a full install of Kubuntu 18.04 running on a USB drive showing the same issue.

**Months later edit:** Yes, I think the title was supposed to be similar to "Ant-Man and the Wasp". Back on topic again, there was no "day 3", because the laptop hasn't failed recently (which is weird, because I don't know what they did). They might have just replaced a wifi card or something...

I still don't understand how Linux failed me at that point...
