---
title: "NexHunt CTF 2025 - HuntMe1 (Beginner)"
categories: [NexHunt, beginner]
tags: [linux]
layout: post
date: 2025-12-12
toc: true
published: true
---

# HuntMe1
## Challenge Description
``` The hunt begins at night. You follow a quiet trail through the forest, guided only by instinct and patience. Nothing reacts. Nothing responds. Yet something is there. ```

## Solution
The provided file, **HuntMe1**, was identified as a Linux executable. Since executable permissions were not initially set, the first step to make the file runnable using the following command:
```chmod +x HuntMe1```

After granting execute permissions, the program was run:
```./HuntMe1```

However, executing the file does not give us the flag. Instead, it prints an output of:
![Output](assets/image/nexhunt/huntme1-output.png)

To further analyze the executable, the ```strings``` utility was used. This command extracts human-readable strings embedded within binary files:
```strings HuntMe1 | grep -i "nexus" ```

Which gives us the flag.
```nexus{h1dd3n_1n_7h3_f0r357_4t_n1gh7}```

## Key Takeaway
Even if executable does not give valuable information when run, it may still be stored within the binary. Basic tools like ```strings``` are often sufficient to extract hidden data in beginner-level challenges.




