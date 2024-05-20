---
layout: post
title:  When and How to Rewrite Apps
categories: lessons
author: groundh0g
---

I was 19 years old when I started programming professionally. I worked for a company that was a household name in the days of my parents&mdash;US Steel. I had never heard of them. It was a paid co-op position, primarily writing COBOL applications, but I got to write some Pascal code to track and their manage IT and shop inventory.

Most of the programs I worked on were older than me. I was too young to appreciate that fact. It was an important lesson that I wasn't prepared to receive. If things are working well, don't spend tons of cash to change just for change's sake.

There's no way I could have known, but around this same time the Alabama state Department of Education (ALSDE) was having a team write an application in Oracle Forms to automate their paper process. Their process involved shuffling papers from one office worker to the next to process applications and renewals for teacher certification. The paper process remained, but the software helped route and track each document packet throughout the lifecycle from start to finish.

Fast-forward 15 years. I was brought in to rewrite ALSDE's Oracle Forms application in C#/.NET. The software was rapidly outgrowing the hardware and storage capabilities of the single machine on which it ran. The small team that was tasked with the rewrite was not the first to attempt the task. Three other teams had attempted and failed to get the application onto more modern and scalable hardware.

The hardware, itself,  was an issue. Released starting in 1988, the AS/400 was a top-of-the-line piece of hardware. As a 15-year-old IBM AS/400 server, though, replacement parts and upgraded resources were impossible to come by. So, vertical scaling was out of the question. Adding a new AS/400 was not an option either. The only available machines were also 15 years old, and we only found those machines on the French-facing eBay site. The application software and OS were likewise so far removed from the support window that there was no upgrade path.

A rewrite and migration was definitely needed.

NOTES:

* Ray the BA: process improvement
* Sid the legacy DBA: duct tape and bubblegum
* Charles the DBA: quality gatekeeper for ALL applications, ours being just one
* ...
* Users - resistant to change

...

![Joe's Signature]({{ "/assets/images/signature-joe.png" | relative_url }})