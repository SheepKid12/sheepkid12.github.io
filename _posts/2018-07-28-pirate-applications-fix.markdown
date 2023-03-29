---
layout: single
title:  "What happens when you fix a pirate application"
category: blog
date:   2018-07-28
---

*How one person brought Deezer (and maybe Disroot) to it's knees.*



This was just recent (at the time of this going live on my blog thing), but there's an application called Deezloader, which allows you to download music from the streaming service Deezer. **I'm not going to link it here, go do some googling and** ~~you'll find a deezloader sub with a fix post potentially stickied.~~ They (Deezer) recently (at the time this was posted) changed their API for logging in to your account, which broke all applications that do similar tasks to deezloader. Then, someone over on r/piracy posted code with a potential fix, so I added it to my copy of deezloader. Turns out, it WORKED. I was excited, I HAD to post about it with a fix, [and I did](https://www.removeddit.com/r/Piracy/comments/921xiw/deezer_api/e33exqx) (switched to removeddit because r/Piracy wiped old posts).

I had to find a place to upload the fixed file. I chose Disroot Cloud, because it's all I could think of at the time (I had to leave to go somewhere and needed it quickly uploaded). I eventually figured out that they show how many people download your files.

This is what happened (part 1):

<link rel="stylesheet" href="https://cdn.plyr.io/3.5.3/plyr.css" />
<script src="https://cdn.plyr.io/3.5.3/plyr.js"></script>

<div class="container">
<video controls crossorigin playsinline id="player1">
	<source src="http://sheepkid12.gitlab.io/assets/video/video1.mp4" type="video/mp4" size="720">
</video>
</div>
<br>
Part 2:

<video controls crossorigin playsinline id="player2">
	<source src="https://sheepkid12.gitlab.io/assets/video/video2.mp4" type="video/mp4" size="720">
</video>

<script>
const players = Plyr.setup('video', {captions: {active: true}});
window.players = players;
</script>
<br>
~~It's probably still going up and up as I type and commit this post to my GitLab blog thing.~~

**A few months later edit:** Tunrs out I was wrong about me not using this page anymore after this page. And yes, the DL count on the files keeps going up. ~~I had also uploaded pre-fixed versions for people who couldn't get the js file to work to MEGA and Disroot Cloud (even AppImages for linux). The MEGA links were DMCA'd. Search for "deezloader fix" and my reddit post comes up as the first result.~~

2021 edit: I had become the mod of the sub in question, and I had enough trying to fight Deezer for keeping links alive, so I removed everyting and privated it.

2022 edit: forgot to mention that I got a personal message from Disroot Cloud admins saying Deezer got in touch with then, and that it was my first warning. All my files were quickly removed from that file hosting platform.
