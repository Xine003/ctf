---
title: "NexHunt CTF 2025 - Allo! (Misc)"
categories: [NexHunt, misc]
tags: [wireshark, pcap]
layout: post
date: 2025-12-12
toc: true
published: true
---

# Allo!
## Challenge Description
``` a new quick wireshark skill unlocked! ```

## Traffic Analysis
Upon analyzing the provided PCAP file, it was observed that the primary protocol used was **RTP (Real-Time Transport Protocol)**, which is commonly utilized in **VoIP (Voice over IP)** communications. Since RTP is associated with audio streams, Wireshark's built-in **Telephony** tools can be used to inspect and reconstruct these calls.

To analyze the VoIP traffic, the following steps were performed:
1. Open the PCAP file in **Wireshark**
2. Navigate to **Telephony -> VoIP Calls**
3. Review the list of detected calls within the capture.

![Telephony](assets/image/nexhunt/allo-telephony.png)

Wireshark identified two VoIP calls present in the traffic. Each was then played using the **Play Streams** feature.
![Calls](assets/image/nexhunt/allo-streams.png)

Upon listening to the reconstructed audio streams, it was found that the **second call** contained a message revealing the flag.
![Audio](assets/image/nexhunt/allo-audio.png)

```nexus{1337483127*$}```
