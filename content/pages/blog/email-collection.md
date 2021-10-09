---
title: Email Collection
subtitle: 'Finding emails at scale, with a focus on automation!'
date: '2021-10-09'
categories: []
tags: []
excerpt: lorem-ipsum
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
## So you wanna get some emails?

There are hundreds of posts regarding how to collect email accounts on an individual and/or company, but this post differs from the norm. We are going to focus on automation and structured outputs, that will enable us to provide consistent results!

> ![](/images/pIcySymeHf7c9a521a-a37c-4027-8b86-c9281ef034b4-1633752525.png)

The above image is representative of one of the tools I have written that scrapes a target website and extracts the emails from said site.

There are a few points I will be discussing here

*   API's and how useful/bad they can be

*   Understanding how the web handles emails embedded on websites

*   Data dumps and breaches

*   Understanding how to get emails, regex etc

*   Writing your own tools to fill the gaps in your collection/analysis cycle.

### API

> ![](/images/pyPsunS1OZ662eb184-41da-4a5d-b37b-abc0a7846362-1633753072.png)

TBA

### Handling Email

> ![](/images/FuIQW7k3z1fc48274f-6a25-46b8-aec6-7e53622be1f6-1633753262.png)

TBA

### Data Dumps

> ![](/images/QCzONHwZTBc655e02f-2f0a-46f1-9501-502a997ffc9d-1633753483.png)

Having your own source of breached data dumps can assist you in collecting the information you need. In windows, you can use a great tool "Agent Ransac" or in Unix, you can use yara-scanner. Yara rule link [here](https://ghostbin.com/R14DM/raw)



### Regex foo

> ![](/images/RiajnUp3ur56c3991d-fcd9-4d28-a38e-4dd8a36fdf60-1633753566.png)

To collect emails you need to use regex! The regex's below should work for you, or check out <https://regexr.com> (or write your own!)

\[a-zA-Z0-9.\_%+-]+@\[a-zA-Z0-9.-]+.\[a-zA-Z]{2,4}

\[a-zA-Z0-9.*%+-]+@\[a-zA-Z0-9.-]+.\[a-zA-Z]{2,4}(:|;|,)\[a-zA-Z0-9.*%+-@#\*)(!<>?\ &:]+

### Tooling

> ![](/images/bGJ8FAUqlc0a14ffbe-d921-443d-9580-c3f8fc566394-1633756235.png)

So there are hundreds of tools out there that can scrape emails for you, but sometimes those tools don't fit into your process flow and in my case, they don't. So I created my own tooling, ruby based that will:

*   Spider the target for all URLs

*   Scrape the site for emails

*   Parse, dedupe and unique the emails; and finally

*   Extract only the targets emails.

So my main point here is that you either use someone else's tools and trust said tool to give you the outcomes you want or write your own tool that enables you to gather the information you need. Furthermore, choose the language that works for you and don't just become a sheep and follow the pack, make sure its works for you. E.g a lot of tooling is written in go or py, but that might not work for you!

And then wella, your emails you asked for!

> ![](/images/ENxGFaLYlN482ca377-b5af-4f02-b859-ee8f58eb5f63-1633756536.png)
