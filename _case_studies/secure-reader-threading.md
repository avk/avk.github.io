---
layout: default
title: Secure Threading for Encrypted Email
overview: Solved an encryption usability problem that closed enterprise customers like Equifax and Dish Network, delighted Capital One and Verizon, and had a 98+% success rate.
skills: user flows, visual design, product metrics, usability testing
date: 2021-05-21
cover_image: /assets/sr_threading/SR-threading-cover.png
---

<img
  src="{{ site.url }}/assets/sr_threading/SR-threading-cover.png"
  alt="Work sample from this case study"
  class="screenshot screenshot-landscape"
/>

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

<p>
  Secure Reader users want to read all the messages in an encrypted email thread even if they open a later message. Currently, users have to find separate emails in their email client and click a link to Secure Reader to decrypt each individual message.
</p>

<details>
  <div>
    <h3>Step 1. Find latest encrypted email (2 of 2)</h3>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_1-email_2_of_2.png"
      alt="Encrypted email 2 of 2 in email client"
      class="screenshot screenshot-landscape"
    />

    <h3>Step 2. Authenticate & decrypt latest email</h3>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_3-SR_2_of_2.png"
      alt="Decrypted email 2 of 2 in Secure Reader"
      class="screenshot screenshot-landscape"
    />

    <h3>Step 3. Find previous encrypted email (1 of 2)</h3>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_5-email_1_of_2.png"
      alt="Encrypted email 1 of 2 in email client"
      class="screenshot screenshot-landscape"
    />

    <h3>Step 4. Authenticate & decrypt previous email (1 of 2)</h3>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_7-SR_1_of_2.png"
      alt="Decrypted email 2 of 2 in Secure Reader"
      class="screenshot screenshot-landscape"
    />
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

<ul>
  <li>myself, Senior Interaction Designer to design solutions</li>
  <li>a Front-end Engineer to implement</li>
  <li>a Product Manager to prioritize</li>
  <li>a User Researcher to evaluate</li>
</ul>

# Design Process

I was asked to design for Secure Reader (SR) threading after engineering had already started evaluating technical feasibility and exploring implementations. That is always frustrating, but I used my first discussions and anecdotal research to make sure we built the best slice of this feature, rather than everything various customers thought it should be.

## 1. Choose "threading" definition

<details>
  <h3>Email "threading" is ambiguous</h3>

  <ol>
    <li>
      <p>Conversation view in Gmail and Outlook</p>

      <img
        src="{{ site.url }}/assets/sr_threading/defn/conversation-view.png"
        alt="Gmail conversation view example of threading - 5 messages"
        class="screenshot screenshot-landscape"
      />

      <ul>
        <li>Messages with a shared subject line are displayed in a list where each message is given a similar visual treatment.</li>
        <li>Earlier messages are visible by default.</li>
        <li>Messages may or may not have quoted content in the body of each</li>
        email. Expanding the quoted content shows earlier messages.
        <li>Typically chronological (oldest to newest)</li>
      </ul>
    </li>

    <li>
      <p>Quoted content in the body of an email</p>

      <img
        src="{{ site.url }}/assets/sr_threading/defn/quoting.png"
        alt="Quoted email example of threading - 2 messages"
        class="screenshot screenshot-landscape"
      />

      <ul>
        <li>When composing a reply or forward, most email clients insert the</li>
        previous message body as a quote into the bottom of the new email.
        <li>When reading an email with a quoted message, earlier messages are</li>
        collapsed by default.
        <li>Quoted messages are given different visual treatment from the</li>
        currently viewed or composed message.
        <li>Typically reverse chronological (newest to oldest)</li>
      </ul>
    </li>

    <li>
      Both conversation view and quoting preserve context. Either would help SR users understand more about where the currently unlocked message fits in. So which should we do?
    </li>
  </ol>

  <h3>Conversation view as "SR threading"</h3>

  <h4>Upsides</h4>

    <ul>
      <li>Easier to follow the conversation because each message has the same visual weight.</li>
      <li>Existing message design already works for smaller resolutions like mobile web.</li>
      <li>Future-proofing SR — if each message is treated the same way visually, that leaves room to show policy controls (e.g. revoke, expire, watermark, etc.) for messages where you’re the policy owner.</li>
      <li>Future-proofing SR — if each message is treated the same way visually, that leaves room to reply to earlier messages directly from SR.</li>
    </ul>

  <h4>Downsides</h4>
  <ul>
    <li>For performance reasons, we shouldn’t load the entire
    conversation like an email client. Decrypting every earlier message would make reading the latest message take too long.</li>
  </ul>

  <h3>Quoted content as "SR threading"</h3>

  <h4>Upsides</h4>
  <ul>
    <li>Since the UI emphasizes the current message and not earlier ones, it’s faster to read.</li>
    <li>Also faster to scan for and read in cases where earlier messages aren’t useful or necessary to the context of the current message.</li>
  </ul>

  <h4>Downsides</h4>
  <ul>
    <li>Each quoted message shrinks the width available to display the message body (and earlier messages), like Russian nesting dolls.</li>
    <li>Readability suffers for longer conversations.</li>
    <li>Because SR has to work on mobile web at a minimum resolution of 375x667, there may be no readable mobile layout for longer conversations. Landscape orientation could help here, but if the quotes continue, that will eventually find a limit as well.</li>
  </ul>

  <mark>I choose conversation view as "SR threading"</mark>, because it had more upsides and felt like a more modern approach.
</details>

## 2. Account for all message states

<details>
  <p>
    I sketched out the message states in my notebook as I understood them. Engineering helped me confirm and revise the possible transitions:

    <img
      src="{{ site.url }}/assets/sr_threading/message-states.jpg"
      alt="Proposed transitions for Secure Reader threading"
      class="screenshot screenshot-landscape"
    />
  </p>

  <p>I'm a fan of using the five states from <a href="https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/" target="_blank">Scott Hurff's UI stack</a> as a starting point for most designs: <em>ideal, loading, error, partial, and blank</em>.</p>

  <p>But the five states wouldn't be enough considering how many possible states there are for each encrypted messages. <mark>These became my design checklist to confirm I covered the entire experience</mark>:

  <ul>
    <li>nothing to decrypt</li>
    <li>attempting to decrypt</li>
    <li>no authentication required to decrypt</li>
    <li>authentication required to decrypt</li>
    <li>access will expire</li>
    <li>access has expired</li>
    <li>access revoked</li>
    <li>not authorized to decrypt</li>
    <li>can decrypt</li>
  </ul>
  </p>
</details>

## 3. Design for mobile web

<p>I started with mobile designs; it's <mark>easier to scale up to larger screens than shrink the experience down.</mark></p>

<details>
  <p>
    If this is our current state (1 of ? messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/current.png"
      alt="Current state of Secure Reader - 1 decrypted email, no threading" class="screenshot screenshot-portrait"
    />
  </p>

  <p>
    An ideal state would be (all messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/ideal.png"
      alt="Ideal state of Secure Reader - 2 decrypted emails in a thread" class="screenshot screenshot-portrait"
    />
  </p>

  <p>
    We just need a transition affordance, like "Read previous [message]" or "decrypt previous [message]" to start off the process. Ideally, reading previous messages <mark>scales to long threads without serious security or performance penalties</mark>.

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/states-overview.png"
      alt="Threading states in Secure Reader - unsupported, 1st message, 2nd message, Nth message"
      class="screenshot screenshot-landscape"
    />
  </p>

  <p>
    Here's what a transition looks like&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/decrypting.png"
      alt="Decrypting the previous message in a thread in Secure Reader"
      class="screenshot screenshot-portrait"
    />
  </p>

  <p>
    Given the numerous things that can go wrong when trying to decrypt a previous message (as listed in the section above), my designs included many auxiliary screens to describe security logic:

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/decrypting-decision-tree.png"
      alt="Numerous checks when decrypting a previous message in a thread in Secure Reader" class="screenshot screenshot-portrait"
    />
  </p>

  <p>
    Though the number of interactions and hotspots exploded&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/SR-threading-hotspots.png"
      alt="Screenshot of dozens of Sketch hotspots to support Secure Reader threading design"
      class="screenshot screenshot-landscape screenshot-borderless"
    />

    &hellip;most error states were as elegant as this&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/error.png"
      alt="Screenshot of typical error state designed for Secure Reader threading"
      class="screenshot screenshot-portrait"
    />
  </p>

</details>

## 4. Confirm direction with stakeholders

<p>
  When I demoed the mobile web design prototype before proceeding, there was pushback from stakeholders. <mark>I persuaded the team to not decrypt more than one previous message at a time.</mark>
</p>

<details>
  <p>Everyone was excited we were bringing threading to Secure Reader (SR). But most people asked why we weren't decrypting the entire thread of previous messages.</p>

  <p>
    How I defended my design of one previous message at a time:

    <ol>
      <li>
        <strong>Simple enough to learn</strong>
        <br>
        We decided to not pause for primary user research up front, but there's more than one possible solution. Customers did not express a preference for how Secure Reader should do email threading. The quoted approach to threading, which we are not pursuing, could be what ultimately works best. So why build the maximum version of conversation view without this clarity?
      </li>
      <li>
        <strong>Performance concerns</strong>
        <br>
        How would decrypting more than one message at a time stay quick and accessible for longer threads? We already have at least half a dozen error states for each message, how would we handle errors for multiple messages?
      </li>
      <li>
        <strong>No historical data</strong><br>
        We had no data on how far back in a thread customers read or want to read. This was not something we tracked in Virtru's other email products.
      </li>
    </ol>
  </p>

</details>

## 5. Design for desktop web

<details>
  <p>The mobile screens scaled up nicely to the larger resolution of desktop browsers.</p>

  <p>
    Here's what a transition looks like&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/decrypting.png"
      alt="Decrypting the previous message in a thread in desktop web Secure Reader"
      class="screenshot screenshot-landscape"
    />
  </p>

  <p>
    And an example error state&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/error.png"
      alt="Screenshot of typical error state designed for desktop web Secure Reader threading"
      class="screenshot screenshot-landscape"
    />
  </p>

  <p>
    An ideal state (all messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/ideal.png"
      alt="Ideal state of desktop web Secure Reader - 2 decrypted emails in a thread" class="screenshot screenshot-landscape"
    />
  </p>

</details>

## 6. Usability test

<details>
  Describe defining the user test with Emily

  Include Emily's Slack results
</details>

## 7. Monitor production metrics & customer feedback

<p>
  I advocated for us to <mark>measure more than simply clicks</mark> on the previous message CTA. With my involvement and planning along with our resident product data expert, we were able to instrument the entire threading experience.
</p>

<details>

  <p>  
    Within a day of launching, threading was available for ~33% of encrypted messages:

    <img
      src="{{ site.url }}/assets/sr_threading/data-use.png"
      alt="Screenshot of day 1 - Secure Reader threading available on 43,940 messages, not available for 134,826 messages."
      class="screenshot screenshot-landscape"
    />
  </p>

  <h3>Quantitative answers I sought</h3>

  <ol>
    <li>
      How many people that decrypted an SR message that’s part of a thread, used SR threading to read at least one earlier message?

      This helped us know <mark>the new UI was being noticed and used.</mark>

      <img
        src="{{ site.url }}/assets/sr_threading/data-funnel.png"
        alt="Screenshot of week 1 Secure Reader threading funnel from previous message shown to successfully used"
        class="screenshot screenshot-landscape"
      />

    </li>

    <li>
      Of those people (in 1), how many previous messages did they try to read?

      This helped us decide if we need to build any kind of bulk decryption for previous messages. Since most users only went back 1 message, <mark>we built the right subset of this feature.</mark>

      <img
        src="{{ site.url }}/assets/sr_threading/data-depth.png"
        alt="Screenshot of week 1 < 4% people read more than one previous message with Secure Reader threading"
        class="screenshot screenshot-landscape"
      />

    </li>

    <li>
      What is the success rate of decrypting previous messages in SR threading? How does that compare to the success rate of decrypting in SR overall?

      This helped prove <mark>we actually solved the user problem of seeing earlier parts of the conversation</mark> without going back to their email.

      <img
        src="{{ site.url }}/assets/sr_threading/data-success-rate.png"
        alt="Screenshot of week 1 98.4% successful decrypts for Secure Reader threading"
        class="screenshot screenshot-landscape"
      />

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
