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

For example, your search for a "handle", that handle returns an email, then we search that email, which returns more results, then we search the email and handle and so on and so forth.

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

![](/images/cApyH7AEie83139edb-202d-4bb7-ac70-eb46eab6beac-1632117092.png)

Just before we finish up with the Twitter images and base analysis, if we run my tool  "[metaextract](https://gitlab.com/interdiction\_/upgraded-goggles)" against the downloaded data we can see that all the data is JPEG. From experience, this leans towards most of the imagery being either copied or reused. The reasoning behind this is that people that create original data usually upload in PNG format as it's the default standard. Now saying that its not 100% conclusive but it gives you an idea of how tech-savvy the person is and what content they create or post.

> FYI: Twitter removes metadata on upload, hence me not extracting the full indicators of association's (IOA)

![](/images/AjoGa7Fj0V30edc9b5-d842-474e-9619-b8d67628a637-1632117382.png)

##### ![](/images/ocWhSAXym2b87a21a8-6f93-4c96-b8e4-bdf9b89462f4-1632117790.png)

##### Searching

This is where you will find all your data. This components output quality is based on how good you built your tagging on the collection and ensuring that all the data you entered in your relevant system (Jira) is correctly defined. I use a multi-search tool "searchcenter" to automate most of these searches. Examples below.

![](/images/TN6t2IeBUOff65c37a-cf63-4e0c-a68e-023fd085146e-1632118774.png)

![](/images/3Sn85miPDsb7af8a99-bd76-45bf-acab-daf89249827a-1632118390.png)

![](/images/Ng5xU8YcJUc6fca88a-33cd-4d1d-bee5-f84e34025948-1632118469.png)

> I hope you got some value from this post and it can enable you to collect in a cyclic more efficient manner.
