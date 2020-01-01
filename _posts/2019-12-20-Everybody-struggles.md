---
layout: post
title: Everybody struggles
---

The purpose of this post is to affirm that it is okay to get stuck, seek help and struggle during the Outreachy internship (and ofcourse, it is okay to struggle outside of the internship too :)). Here is how I struggled with setting up Qemu during the contribution period.

One of the project specific tasks during the contribution period was to write a kernel module that would cause the system to crash and to  setup Qemu with persistent storage RAM and retrieve the crash log from PSTORE. I came up with a kernel module that would create a file under tracing directory during module initialization and any write to this file would cause the kernel to panic. I foolishly thought the next part of setting up Qemu and running this new module from within it wouldn't take much time. How wrong I was!

My mentor had given me the command line options that I had to use to setup pstore with Qemu. I had never used Qemu earlier. After quick google search, I realized that Qemu was a Virtual Machine. At this point, the right thing to do would have been to read Qemu documentation and more on the command line options that were already provided to me. Since I was using Windows on my PC (and was running Linux on VMPlayer), I searched the internet for "Running Linux in Qemu on windows" and followed a tutorial which instructed me to install the entire distro on the VM. Needless to say, it was excruciatingly slow.I spent the next few days in the StackOverflow forum. Finally, I went back to the command line options my mentor had given and Qemu documentation, and realized that I could provide the kernel image through -kernel option rather than installing it as disk image. 
I did hit a few roadblocks after this in setting up PSTORE due to missing libraries etc but I made progress.

What did I learn from this - Read, read and read the documentation.


