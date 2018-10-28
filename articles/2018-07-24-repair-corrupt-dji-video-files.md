---
title: Repair corrupt DJI video files
creation: 2018-07-24 22:00:00
published: true
---

Having my new drone for some days now I was facing a corrupt video file today. I guess it got corrupted when I turned off the drone before ending the recording. According to some information from the DJI forum this seems to be a known issue for some (maybe all) DJI drones.

Even though the `.mp4` file seems to be created properly on the SD card, beside the video file itself you can find a `.trinf` and a `.avc1` file.

Inside the DJI forum I found out that I'm not the first person who had this problem. But luckily I also found a solution for this issue inside the forum. You can use the tool __djifix__ which can be found [__here__](http://djifix.live555.com/). Inside the forum it is mentioned that the homepage seems to be offline sometimes.

Using the tool is pretty easy. Simply put the tool and the corrupt file inside a directory and run the following command:

    djifix name-of-video-file-to-repair-including-any-.MP4-or-.MOV-filename-suffix

Afterwards you will have a `.h264` file. If needed this file can then be converted to `.mp4` afterwards using [__ffmpeg__](https://www.ffmpeg.org/download.html).