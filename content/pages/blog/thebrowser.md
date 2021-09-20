---
title: The browsers best friend == you
date: '2021-09-19'
categories: []
tags: []
excerpt: Lets go!
thumb_image_alt: lorem-ipsum
image_alt: lorem-ipsum
image_position: top
seo:
  title: ''
  description: ''
  robots: []
  extra: []
layout: post
image: /images/3SDgmYs73L95a1e13d-2ae0-4ba4-812e-eb8d9c53a63d-1632040289.png
---
### So I always get these questions. \[part one/six]

> TLDR; These are the manual process that all can be automated and for me they are.

I'm always asked what and how I use the browser for my OSINT operations, so I will explain most of my processes within this blog. This process should enable you to gain an insight into my methods and how I used them effectively.

The main points I will cover are:

*   Information storage and integrations \[this post]

*   Email collection

*   Phone collection

*   Name/user/handle/alias collection

*   Infrastructure collection; and

*   Breached data collection.

#### Information storage and integrations

The main goal of OSINT collection and storage, is having the ability to have a repeatable, searchable and taggable system that ensures the data you want to store is stored correctly.  There are three key points:

*   Process of collection

*   Searching your collected data

*   Tagging said data and ensuring its relevance.

##### Process of collection

In one of my previous posts [\[Operators handbook\]](https://inteloperator.medium.com/operational-intelligence-handbook-4e5f0538cfb), I detail these steps in an overall view, but here I will elaborate on it. Have the mindset that each artefact that you collect can be reinvested into the next search/lookup and continually in a cyclic form.

For example, you search for a "handle", that handle returns an email, then we search that email, which returns more results, then we search the email and handle and so on and so forth.

![](/images/1\_CXL5Ersq1gHztPK44sVCKw.png)

When I'm collecting OSINT I will full text save the page which contains the data using raindrop\[.]io with tags. If the page I'm looking at has email, phone and ABN, ill save the page with "#email_acc #phone_pers #ABN #target_ref_number #artefact".

This enables me to search at a later time, key fields "if i cant remember the specifics". Furthermore, to that point, I will extract the key fields into my Jira instance (which has auto-tagging rules, ill get to this later) and start building a dossier on the target in question. Images below are some examples.

![](/images/bwzMBQJQvYfafaf573-9300-40b7-b140-887b90266624-1632097066-da8fc61f.png)

The above image is me storing this OSINT data with relevant tagging within raindrop for later analysis and parsing. Another good idea is to use the wayback machine archive function for redundancy.

![](/images/55h1NxiTT758783663-1713-4d00-a1f9-2964ced99d44-1632101920-4e54d7b2.png)

Then I did a quick TinEye reverse image search and also saved and tagged all references.

![](/images/vYaogCv4y62ce2dabd-4537-4756-8acf-47810fdfa826-1632114811.png)

Then I double-checked that the data was full-text indexed and it was, love it!

![](/images/RQtHM0zSMo22ba1d35-39ea-4771-a906-071a4a686176-1632114717.png)

I then scraped all the user's images and videos to give me an understanding of the persons life and online persona.

![](/images/KXsMC86veZ00da81b8-a0de-4ab7-8eb1-f89a7ec933c3-1632115882.png)

I used a regex for Twitter hash-tags to visually highlight points of interest from the exported CSV twitter scrape.

![](/images/ou16MMUV8idfdb6f54-a64d-47d0-b566-89bee0918b49-1632116465.png)

The above image is an example osint comment within my Jira to ensure all data points are correctly tagged. Furthermore, the below image is an example tagging rule (which I have a lot) that enables me to search over the vast osint sources I have previously completed.



Searching

tba

##### Relevance

tba
