---
layout: default
title: Secure Threading for Encrypted Email
overview: Solved an encryption usability problem that closed enterprise customers like Equifax and Dish Network, delighted Capital One and Verizon, and had a 98+% success rate.
skills: user flows, visual design, product metrics, usability testing
date: 2021-05-21
cover_image: TBD
---

# <small>Case Study:</small> <br />Secure Threading for Encrypted Email

<a href="https://www.virtru.com/secure-collaboration/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2021)</a>

## Overview

Virtru's Secure Reader (SR) is a web app that allows reading and replying to encrypted email. Since SR displays only one message at a time, following an encrypted email conversation involves jumping back and forth between two apps—your email client and SR—to read more than one message. Virtru customers (and their email recipients) need to see all encrypted emails in a thread with minimal friction in a performant way, even for long threads.

## Skills Used

* user flows  
* visual design
* product metrics
* usability testing

## Problem Definition

<details open>
  <p>
    Secure Reader users want to read all the messages in an encrypted email thread even if they open a later message. Currently, users have to find separate emails in their email client and click a link to Secure Reader to decrypt each individual message.
  </p>

  <div>
    <h3>Step 1. Find latest encrypted email (2 of 2)</h3>
    <img src="{{ site.url }}/assets/sr_threading/cur_SR_1-email_2_of_2.png" alt="Encrypted email 2 of 2 in email client">

    <h3>Step 2. Authenticate & decrypt latest email</h3>
    <img src="{{ site.url }}/assets/sr_threading/cur_SR_3-SR_2_of_2.png" alt="Decrypted email 2 of 2 in Secure Reader">

    <h3>Step 3. Find previous encrypted email (1 of 2)</h3>
    <img src="{{ site.url }}/assets/sr_threading/cur_SR_5-email_1_of_2.png" alt="Encrypted email 1 of 2 in email client">

    <h3>Step 4. Authenticate & decrypt previous email (1 of 2)</h3>
    <img src="{{ site.url }}/assets/sr_threading/cur_SR_7-SR_1_of_2.png" alt="Decrypted email 2 of 2 in Secure Reader">
  </div>

  Challenges:
  <ul>
    <li>
      Understand if users expect "threading" to mean conversation view, quoted content, or something else when they request this feature.
    </li>
    <li>
      Preserve as much email context as possible.
    </li>
    <li>
      Must not sacrifice performance or time to decrypt.
    </li>
    <li>
      Must work well on mobile web.
    </li>
    <li>
      Ideally, support threads of any length (1 message to many).
    </li>
  </ul>
</details>

## My Role on the Team

<details>
  <ul>
    <li>myself, Senior Interaction Designer to design solutions</li>
    <li>a Front-end Engineer to implement</li>
    <li>a Product Manager to prioritize</li>
    <li>a User Researcher to evaluate</li>
  </ul>
</details>

# Design Process

I was asked to design for Secure Reader (SR) threading after engineering had already started evaluating technical feasibility and exploring implementations. That is always frustrating, but I used my first discussions and anecdotal research to make sure we built the best slice of this feature, rather than everything various customers thought it should be.

## 1. Choose "threading" definition

<details>
  Include text or screenshot from exploratory Google Doc
</details>

## 2. Account for all message states

<details>
  Take photo of my notebook sketch

  Not only five states from Scott Hurff…

  List out all message states I found
</details>

## 3. Design for mobile web

<details open>
  Starting with the ideal state…

  Include mobile side-by-side experience

  Show not-so-happy paths
</details>

## 4. Confirm direction with stakeholders

<details open>
  Argued for not decrypting more than one message.
  More than one possible solution.
  Performance.
  We don't have data on how far back in a thread anyone wants to read.
</details>

## 5. Design for desktop web

<details>
  Include same screens as mobile (or user test screens)
</details>

## 6. Usability test

<details>
  Describe defining the user test with Emily

  Include Emily's Slack results
</details>

## 7. Monitor production metrics & customer feedback

<details open>

  <p>
  I advocated for us to <mark>measure more than simply clicks</mark> on the previous message CTA. With my involvement and planning along with our resident product data expert, we were able to instrument the entire threading experience.
  </p>

  <p>  
    Within a day of launching, threading was available for ~33% of encrypted messages:

    <img src="{{ site.url }}/assets/sr_threading/data-use.png" alt="Screenshot of day 1 - Secure Reader threading available on 43,940 messages, not available for 134,826 messages.">
  </p>

  <h3>Quantitative answers I sought</h3>

  <ol>
    <li>
      How many people that decrypted an SR message that’s part of a thread, used SR threading to read at least one earlier message?

      This helped us know <mark>the new UI was being noticed and used.</mark>

      <img src="{{ site.url }}/assets/sr_threading/data-funnel.png" alt="Screenshot of week 1 Secure Reader threading funnel from previous message shown to successfully used">

    </li>

    <li>
      Of those people (in 1), how many previous messages did they try to read?

      This helped us decide if we need to build any kind of bulk decryption for previous messages. Since most users only went back 1 message, <mark>we built the right subset of this feature.</mark>

      <img src="{{ site.url }}/assets/sr_threading/data-depth.png" alt="Screenshot of week 1 < 4% people read more than one previous message with Secure Reader threading">

    </li>

    <li>
      What is the success rate of decrypting previous messages in SR threading? How does that compare to the success rate of decrypting in SR overall?

      This helped prove <mark>we actually solved the user problem of seeing earlier parts of the conversation</mark> without going back to their email.

      <img src="{{ site.url }}/assets/sr_threading/data-success-rate.png" alt="Screenshot of week 1 98.4% successful decrypts for Secure Reader threading">

    </li>
  </ol>

  <h3>Qualitative feedback</h3>

  <blockquote>
    <p>
      Equifax loves it. Verizon didn't realize it rolled out but after we showed them they were happy about it. Capital One felt similarly.
    </p>

    <cite>- Virtru Enterprise <abbr title="Customer Success Manager">CSM</abbr></cite>
  </blockquote>

  <blockquote>
    <p>
      Art's willingness to dig in quickly and iterate on a minimal, slick UX for the feature was key to getting this win. And <mark>Secure Reader threading was essential to our successful roll-out at two of our largest customers - Dish and Equifax.</mark>
    </p>

    <cite>- Virtru <abbr title="Chief Executive Officer">CEO</abbr></cite>
  </blockquote>

  <blockquote>
    <p>
      It comes up occasionally and customers are delighted by it.
    </p>

    <cite>- Virtru <abbr title="Senior Vice President">SVP</abbr> of Customer Success</cite>
  </blockquote>

</details>

# Retrospective

<details>
  <p>
    I'm satisfied with the initial impact of this design. I'll revisit the retrospective when I have more distance from this effort.
  </p>
</details>

<hr />

<p>
  <a href="https://www.virtru.com/secure-collaboration/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2021)</a>
</p>

{% include footer_case_study.md %}
