---
title: "Speaking"
layout: splash
permalink: /speaking/
date: 2019-06-30T21:39:00-04:00
classes: 
  - wide
  - landing
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: /assets/images/splash_bg_minkwic_2015.jpg
  caption: "Speaking at MINK WIC 2015, which I also helped organize"
---

Over the years, I've given over 55 presentations that range from workshops to keynote presentations. I've also spoken 
locally, regionally, nationally, and internationally. If you’re interested in having me speak, please reach out! Send 
me a message on my [Contact](/contact/) page.

Jump to section: 
[Upcoming Events](#upcoming-events){: .btn .btn--inverse .btn--large }
[About My Talks](#about-my-talks){: .btn .btn--inverse .btn--large }
[My Talks](#my-talks){: .btn .btn--inverse .btn--large }
[Past Events](#past-events){: .btn .btn--inverse .btn--large }
{: .notice--primary.text-center}

## Upcoming Events

{% assign today = "now" | date: "%Y-%m-%d" %}

| Date | Event, Location | Talk Type | Talk Title | 
|------|-----------------|-----------|------------|
{% for item in site.data.conftalks %}{% assign event_date = item.talk_date | date: "%Y-%m-%d" %}{% if event_date >= today %}{% if item.event_start_date == item.event_end_date %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.event_end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {% if item.event_url %}<a href="{{ item.event_url}}" target="_blank">{{ item.event_name }}</a>{% else %}{{ item.event_name }}{% endif %}, {{ item.event_location }} | {{ item.talk_type }} | {% if item.talk_url %}<a href="{{ item.talk_url}}">{{ item.talk_title }}</a>{% else %}{{ item.talk_title }}{% endif %}
{% endif %}{% endfor %}

## About My Talks

I really love speaking about the intersection of where tech and people come together. As a polyglot (multiple-language) 
software engineer, I've worked in a variety of tech stacks and fields and I have a wide range of interests. My talks 
often reflect this and I bring a different perspective to many topics in the field, both technically and professionally.

If you see a talk that interests you, or would like to discuss maybe creating a talk or discussing something 
specifically for your event, please reach out to me. I'd love to chat more about it. Drop me a line on my 
[Contact](/contact/) page.

## My Talks

Here's a list of my talks I've given.

**Keynote-Worthy Talks**
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [Doors](/speaking/doors/)
- [The Power of Secrets](/speaking/the-power-of-secrets/)

**Technical Talks**
- [A Primer on Functional Programming](/speaking/a-primer-on-functional-programming/)
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [“Hey Mycroft”: Getting Started with the Open Source Home Assistant](/speaking/hey-mycroft-getting-started-with-the-open-source-home-assistant/)
- [Intro to Hacking with the Raspberry Pi](/speaking/intro-to-hacking-with-the-raspberry-pi/)
    
**Professional Skills/Human Skills Talks**
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [Building Your Team to Last: Successful Onboarding and Mentoring Practices](/speaking/building-your-team-to-last/)
- [Doors](/speaking/doors/)
- Life as a Midwestern Developer
- [Maintaining Your Mental and Emotional Health While Job Hunting](/speaking/maintaining-your-mental-and-emotional-health-while-job-hunting/)
- [The Power of Secrets](/speaking/the-power-of-secrets/)
- [Pursuing a Passion Project: Struggles and Successes]()

**Workshops**
- [“What is a HashTrieStackFilter?” A Data Structures & Algorithms Refresher For Everyone](/speaking/wtf-is-a-hashtriestackfiltermap/)


## Past Events

| Date | Event, Location | Talk Type | Talk Title | 
|------|-----------------|-----------|------------|
{% for item in site.data.conftalks reversed %}{% assign date = item.talk_date | date: "%Y-%m-%d" %}{% if date < today %}{% if item.event_start_date == item.event_end_date %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.event_end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {% if item.event_url %}<a href="{{ item.event_url}}" target="_blank">{{ item.event_name }}</a>{% else %}{{ item.event_name }}{% endif %}, {{ item.event_location }} | {{ item.talk_type }} | {% if item.talk_url %}<a href="{{ item.talk_url}}">{{ item.talk_title }}</a>{% else %}{{ item.talk_title }}{% endif %}
{% endif %}{% endfor %}
