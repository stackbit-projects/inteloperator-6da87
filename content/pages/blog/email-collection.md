---
title: Email Collection
subtitle: 'Finding emails at scale, with a focus on automation!'
date: '2021-10-09'
categories: []
tags: []
excerpt: 'Finding emails at scale, with a focus on automation!'
thumb_image_alt: lorem-ipsum
image_alt: Code it!
image_position: right
seo:
  title: ''
  description: ''
  robots: []
  extra: []
layout: post
image: /images/CzjaxAcPUB72fc35fe-b00b-4201-93c6-be2103228951-1633752753.png
---
## So you want to get some emails?

TLDR; Don't do what everyone else does, and create your own email collection pipeline.

There are hundreds of posts out there regarding email collection on individuals and companies, but this post differs from the norm. So instead, we will focus on automation and structured outputs that will enable us to provide consistent results!

> ![](/images/pIcySymeHf7c9a521a-a37c-4027-8b86-c9281ef034b4-1633752525.png)

The above image is representative of one of the tools I have written that scrapes a target website and extracts the emails from said site.

There are a few points I will be discussing here

*   API's and how useful/bad they can be

*   Understanding how the web handles embedded emails

*   Data dumps and breaches

*   Learning how to get emails, regex etc

*   Writing your tools to fill the gaps in your collection/analysis cycle.

### API

> ![](/images/pyPsunS1OZ662eb184-41da-4a5d-b37b-abc0a7846362-1633753072.png)

API's are an excellent resource for "known" email accounts at a specific DTG. API's also enable you not to touch the target infrastructure, which is also good in some cases but hardly ever needed, as you should be using a VPN like IVPN or torsocks. Furthermore, API's have limits and do cost $$$, so you need to way up the cost/benefit analysis or create multiple accounts for the same site and rotate API keys.

### Handling Email

> ![](/images/FuIQW7k3z1fc48274f-6a25-46b8-aec6-7e53622be1f6-1633753262.png)

Understanding how websites protect emails is key to being able to write your custom extractors. For example, in the above image, there is a mailto:email@domain link. Still, the actual email is broken down into three parts, with the first part being account, the domain is being excluded, and the TLD is also broken out into a different code segment. So, in this case, a regex would work a treat (more on that later), but some open-source scanners wouldn't find this email account because it's not in the correct format, and it's muddied via "security via obscurity!"

### Data Dumps

> ![](/images/QCzONHwZTBc655e02f-2f0a-46f1-9501-502a997ffc9d-1633753483.png)

Having your source of breached data dumps can assist you in collecting the information you need. In windows, you can use a great tool, "Agent Ransac", or in Unix, you can use yara-scanner. Yara rule link [here](https://ghostbin.com/R14DM/raw)

![](/images/Gpvw4x3bJk023d9926-e1b6-43d1-bf62-d02f0baaf422-1633757430-96e67e7e.png)

### Regex foo

> ![](/images/RiajnUp3ur56c3991d-fcd9-4d28-a38e-4dd8a36fdf60-1633753566.png)

To collect emails, you need to use regex! The regex's below should work for you, or check out <https://regexr.com> (or write your own!)

\[a-zA-Z0-9.\_%+-]+@\[a-zA-Z0-9.-]+.\[a-zA-Z]{2,4}

\[a-zA-Z0-9.*%+-]+@\[a-zA-Z0-9.-]+.\[a-zA-Z]{2,4}(:|;|,)\[a-zA-Z0-9.*%+-@#\*)(!<>?\ &:]+

### Tooling

> ![](/images/bGJ8FAUqlc0a14ffbe-d921-443d-9580-c3f8fc566394-1633756235.png)

So there are hundreds of tools out there that can scrape emails for you, but sometimes those tools don't fit into your process flow, and in my case, they don't. So I created my own tooling, ruby based that will:

*   Spider the target sites for all URLs

*   Scrape the site for emails

*   Parse, dedupe and unique the emails; and finally

*   Extract only the targets emails.

So my main point here is that you either use someone else's tools and trust said tool to give you the outcomes you want or write your own tool that enables you to gather the information you need. Furthermore, choose the language that works for you and don't just become a sheep and follow the pack; make sure its works for you. E.g. a lot of tooling is written in go or py, but that might not work for you!

And then wella, your emails you asked for!

> ![](/images/ENxGFaLYlN482ca377-b5af-4f02-b859-ee8f58eb5f63-1633756536.png)
