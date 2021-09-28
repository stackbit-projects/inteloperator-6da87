---
title: OSINT Quicki
subtitle: Makes the start of your OSINT just that little bit simpler and safer
date: '2021-09-28'
categories: []
tags: []
excerpt: lorem-ipsum
thumb_image_alt: lorem-ipsum
image_alt: lorem-ipsum
image_position: top
seo:
  title: ''
  description: ''
  robots: []
  extra: []
layout: post
---
## ![](/images/main.png)

I always find myself doing the same process at the start of a non-automated OSINT engagement, so I created a simple tool that gets you going quickly, and in the background, you can focus on what's important.

The main features are:

*   Checks VPN is connected *OpenVPN*

*   \*\*Checks burp **OR** zap proxy is running *127.0.0.1:8080*

*   \**Uses amass and* crt\[.]sh \*to create a starter subdomain list

*   Checks waybackmachine for more URLs

*   Scrapes subdomains found to speed up your OSINT

*   Sends all the data to burp **OR** zap; and

*   Sweet ASCII art.

Simple Install steps

*   sudo apt install -y fish

*   fish

*   curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

*   fisher install laughedelic/fish_logo

*   sudo apt install -y ruby && sudo gem install spidr && sudo gem install wayback_machine_downloader

**fish wriggle.fish domaininquestion.com**
