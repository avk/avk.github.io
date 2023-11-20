---
layout: default
title: Secure Threading for Encrypted Email
overview: Solved an encryption usability problem that closed enterprise customers like Equifax and Dish Network, delighted Capital One and Verizon, and had a <mark>98+% success rate</mark>.
skills: user flows, visual design, product metrics, usability testing
date: 2021-05-21
cover_image: /assets/sr_threading/SR-threading-cover.png
active: true
---

<img
  src="{{ site.url }}/assets/sr_threading/SR-threading-cover.png"
  alt="Work sample from this case study"
  class="screenshot screenshot-landscape"
/>

# <small>Case Study:</small> <br />Secure Threading for Encrypted Email

<a href="https://www.virtru.com/secure-collaboration/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2021)</a>





* [Overview](#1)
  * [Skills Used](#1.1)
  * [Problem Definition](#1.2)
  * [My Role on the Team](#1.3)

* [Design Process](#2)
  1. [Choose "threading" definition](#2.1)
  2. [Account for all message states](#2.2)
  3. [Design for mobile web](#2.3)
  4. [Confirm direction with stakeholders](#2.4)
  5. [Design for desktop web](#2.5)
  6. [Usability test](#2.6)
  7. [Track production metrics & customer feedback](#2.7)

* [Retrospective](#3)

<hr />





<a name="1"></a>
## Overview

Virtru's Secure Reader (<abbr title="Secure Reader">SR</abbr>) is a web app that allows reading and replying to encrypted email. But <abbr title="Secure Reader">SR</abbr> displays only one message at a time. Following an encrypted email conversation means jumping between your email client and <abbr title="Secure Reader">SR</abbr> to read more than one message. Virtru customers need to see earlier encrypted emails in a thread with minimal friction in a performant way, even for long threads.





<a name="1.1"></a>
### Skills Used

* user flows  
* visual design
* product metrics
* usability testing





<a name="1.2"></a>
### Problem Definition

<p>
  Secure Reader users want to read all the messages in an encrypted email thread even if they open a later message. Currently, users have to find separate emails in their email client and click a link to Secure Reader to decrypt each individual message.
</p>

<details>
  <div>
    <h4>Step 1. Find latest encrypted email (2 of 2)</h4>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_1-email_2_of_2.png"
      alt="Encrypted email 2 of 2 in email client"
      class="screenshot screenshot-landscape zoomable"
    />

    <h4>Step 2. Authenticate & decrypt latest email</h4>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_3-SR_2_of_2.png"
      alt="Decrypted email 2 of 2 in Secure Reader"
      class="screenshot screenshot-landscape zoomable"
    />

    <h4>Step 3. Find previous encrypted email (1 of 2)</h4>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_5-email_1_of_2.png"
      alt="Encrypted email 1 of 2 in email client"
      class="screenshot screenshot-landscape zoomable"
    />

    <h4>Step 4. Authenticate & decrypt previous email (1 of 2)</h4>
    <img
      src="{{ site.url }}/assets/sr_threading/cur_SR_7-SR_1_of_2.png"
      alt="Decrypted email 2 of 2 in Secure Reader"
      class="screenshot screenshot-landscape zoomable"
    />
  </div>

  Challenges:
  <ul>
    <li>
      Understand if users expect "threading" to mean conversation view, quoted content, or something else.
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





<a name="1.3"></a>
### My Role on the Team

<ul>
  <li>myself, Senior Interaction Designer to design solutions</li>
  <li>a Front-end Engineer to implement</li>
  <li>a Product Manager to prioritize</li>
  <li>a User Researcher to evaluate</li>
</ul>





<a name="2"></a>
## Design Process

Product Management asked me to design for Secure Reader (<abbr title="Secure Reader">SR</abbr>) threading in Spring 2021. Engineering had already started evaluating technical feasibility and exploring implementations. My first discussions and anecdotal research ensured we built the best slice of this feature, not everything various customers thought it should be.





<a name="2.1"></a>
### 1. Choose "threading" definition

The first problem was that email "threading" is ambiguous.

<details>

  <h4>Conversation view in Gmail and Outlook</h4>

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





  <h4>Quoted content in the body of an email</h4>

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

  <blockquote>
    Both conversation view and quoting preserve context. Either would help <abbr title="Secure Reader">SR</abbr> users understand more about where the currently unlocked message fits in. So which should we do?
  </blockquote>





  <h4>Conversation view as "<abbr title="Secure Reader">SR</abbr> threading"</h4>

  <strong>Upsides</strong>

    <ul>
      <li>Easier to follow the conversation because each message has the same visual weight.</li>
      <li>Existing message design already works for smaller resolutions like mobile web.</li>
      <li>Future-proofing <abbr title="Secure Reader">SR</abbr> — a similar visual treatment of each message leaves room to show security controls (e.g. revoke, expire, watermark, etc.). This enhances the security of messages you send.</li>
      <li>Future-proofing <abbr title="Secure Reader">SR</abbr> — a similar visual treatment of each message leaves room to reply to earlier messages directly from <abbr title="Secure Reader">SR</abbr>.</li>
    </ul>

  <strong>Downsides</strong>
  <ul>
    <li>For performance reasons, we shouldn’t load the entire
    conversation like an email client. Decrypting every earlier message would make reading the latest message take too long.</li>
  </ul>





  <h4>Quoted content as "<abbr title="Secure Reader">SR</abbr> threading"</h4>

  <strong>Upsides</strong>
  <ul>
    <li>Since the UI emphasizes the current message and not earlier ones, it’s faster to read.</li>
    <li>Also faster to scan for and read in cases where earlier messages aren’t useful or necessary to the context of the current message.</li>
  </ul>

  <strong>Downsides</strong>
  <ul>
    <li>Each quoted message shrinks the width available to display the message body, like Russian nesting dolls.</li>
    <li>Readability suffers for longer conversations.</li>
    <li>Because <abbr title="Secure Reader">SR</abbr> has to work on mobile web at a minimum resolution of 375x667, there may be no readable mobile layout for longer conversations. Landscape orientation could help here, but if the quotes continue, that will eventually find a limit as well.</li>
  </ul>

  <mark>I choose conversation view as "<abbr title="Secure Reader">SR</abbr> threading"</mark>, because it had more upsides and felt like a more modern approach.
</details>





<a name="2.2"></a>
### 2. Account for all message states

  <p>
    I sketched out the message states in my notebook as I understood them. Engineering helped me confirm and revise the possible transitions:

    <img
      src="{{ site.url }}/assets/sr_threading/message-states.jpg"
      alt="Proposed transitions for Secure Reader threading"
      class="screenshot screenshot-landscape zoomable"
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





<a name="2.3"></a>
### 3. Design for mobile web

<p>I started with mobile designs; it's <mark>easier to scale up to larger screens than shrink the experience down.</mark></p>

  <p>
    If this is our current state (1 of ? messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/current.png"
      alt="Current state of Secure Reader - 1 decrypted email, no threading" class="screenshot screenshot-portrait zoomable"
    />
  </p>

  <p>
    An ideal state would be (all messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/ideal.png"
      alt="Ideal state of Secure Reader - 2 decrypted emails in a thread" class="screenshot screenshot-portrait zoomable"
    />
  </p>

  <p>
    We just need a transition affordance, like "Read previous [message]" or "decrypt previous [message]" to start off the process. Ideally, reading previous messages <mark>scales to long threads without security or performance penalties</mark>.

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/states-overview.png"
      alt="Threading states in Secure Reader - unsupported, 1st message, 2nd message, Nth message"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    Here's what a transition looks like&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/decrypting.png"
      alt="Decrypting the previous message in a thread in Secure Reader"
      class="screenshot screenshot-portrait zoomable"
    />
  </p>

  <p>
    Many things can go wrong when trying to decrypt a previous message (as listed in the section above). My designs included many auxiliary screens to describe security logic:

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/decrypting-decision-tree.png"
      alt="Numerous checks when decrypting a previous message in a thread in Secure Reader" class="screenshot screenshot-portrait zoomable"
    />
  </p>

  <p>
    Though the number of interactions and hotspots exploded&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/SR-threading-hotspots.png"
      alt="Screenshot of dozens of Sketch hotspots to support Secure Reader threading design"
      class="screenshot screenshot-landscape screenshot-borderless zoomable"
    />

    &hellip;most error states were as elegant as this&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/mobile/error.png"
      alt="Screenshot of typical error state designed for Secure Reader threading"
      class="screenshot screenshot-portrait zoomable"
    />
  </p>





<a name="2.4"></a>
### 4. Confirm direction with stakeholders

<p>
  When I demoed the mobile web design prototype before proceeding, there was pushback from stakeholders. <mark>I persuaded the team to not decrypt more than one previous message at a time.</mark>
</p>

<details>
  <p>Everyone was excited we were bringing threading to Secure Reader (<abbr title="Secure Reader">SR</abbr>). But most people asked why we weren't decrypting the entire thread of previous messages.</p>

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





<a name="2.5"></a>
### 5. Design for desktop web

<p>The mobile screens scaled up nicely to the larger resolution of desktop browsers.</p>

<details>

  <p>
    Here's what a transition looks like&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/decrypting.png"
      alt="Decrypting the previous message in a thread in desktop web Secure Reader"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    An example error state&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/error.png"
      alt="Screenshot of typical error state designed for desktop web Secure Reader threading"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    An ideal state (all messages in a thread decrypted)&hellip;

    <img
      src="{{ site.url }}/assets/sr_threading/desktop/ideal.png"
      alt="Ideal state of desktop web Secure Reader - 2 decrypted emails in a thread" class="screenshot screenshot-landscape zoomable"
    />
  </p>

</details>





<a name="2.6"></a>
### 6. Usability test

<p>
  Before launch, I worked with one of our User Researchers to evaluate the effectiveness of the design with 10 external users. We recruited  participants via UserTesting.com. We split participants into two groups&mdash;<strong>current experience vs. new experience</strong>.
</p>

<details>
  <h4>Current experience&mdash;no threading</h4>
  <ol>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_0.png">See Gmail inbox with unread messages</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_1.png">Open Gmail conversation to see latest message encrypted</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_2.png">Load Secure Reader in new tab to decrypt</a>
    </li>
    <li>
      See latest message decrypted (2 of 2)
      <img
        src="{{ site.url }}/assets/sr_threading/usertest/no_threading.png"
        alt="A decrypted message without threading in desktop web Secure Reader"
        class="screenshot screenshot-landscape zoomable"
      />
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_4.png">Navigate back to Gmail conversation</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_5.png">Expand previous message in Gmail conversation</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_6.png">Load Secure Reader in another new tab to decrypt again</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/cur_ux/cur_7.png">See previous message decrypted (1 of 2)</a>
    </li>
  </ol>

  <h4>New experience&mdash;threaded secure messages</h4>
  <ol>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/new_ux/new_0.png">See Gmail inbox with unread messages</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/new_ux/new_1.png">Open Gmail conversation to see latest message encrypted</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/new_ux/new_2.png">Load Secure Reader in new tab to decrypt</a>
    </li>
    <li>
      See latest message decrypted (2 of 2) with link to previous
      <img
        src="{{ site.url }}/assets/sr_threading/usertest/threading.png"
        alt="A decrypted message with threading support in desktop web Secure Reader"
        class="screenshot screenshot-landscape zoomable"
      />
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/new_ux/new_4.png">Load previous message</a>
    </li>
    <li>
      <a href="{{ site.url }}/assets/sr_threading/usertest/new_ux/new_5.png">See previous message decrypted (1 of 2)</a>
    </li>
  </ol>

  <p>
    We hypothesized that participants would spend less time to get to previous messages with the new experience and rank it as easier to use.
  </p>

  <p>
    <mark>Our hypotheses proved accurate</mark>, so we proceeded to production.
    <img
      src="{{ site.url }}/assets/sr_threading/usertest/test_results.png"
      alt="Slack results of high-level takeaways of user test of Secure Reader threading" class="screenshot screenshot-landscape zoomable"
    />
  </p>
</details>





<a name="2.7"></a>
### 7. Track production metrics & customer feedback

<p>
  I advocated for us to <mark>measure more than simple clicks</mark> on the previous message <abbr title="call to action">CTA</abbr>. With my involvement and planning, we were able to instrument the entire threading experience. Our resident product data expert was glad to be included and helped refine events and properties.
</p>

  <p>  
    Within a day of launching, threading was available for ~33% of encrypted messages:

    <img
      src="{{ site.url }}/assets/sr_threading/data-use.png"
      alt="Screenshot of day 1 - Secure Reader threading available on 43,940 messages, not available for 134,826 messages."
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <h4>Quantitative answers I sought</h4>

  <ol>
    <li>
      How many people that decrypted an <abbr title="Secure Reader">SR</abbr> message that’s part of a thread, used <abbr title="Secure Reader">SR</abbr> threading to read at least one earlier message?

      This helped us know <mark>the new UI was being noticed and used.</mark>

      <img
        src="{{ site.url }}/assets/sr_threading/data-funnel.png"
        alt="Screenshot of week 1 Secure Reader threading funnel from previous message shown to successfully used"
        class="screenshot screenshot-landscape zoomable"
      />

    </li>

    <li>
      Of those people (in 1), how many previous messages did they try to read?

      This helped us decide if we need to build any kind of bulk decryption for previous messages. Since most users only went back 1 message, <mark>we built the right subset of this feature.</mark>

      <img
        src="{{ site.url }}/assets/sr_threading/data-depth.png"
        alt="Screenshot of week 1 < 4% people read more than one previous message with Secure Reader threading"
        class="screenshot screenshot-landscape zoomable"
      />

    </li>

    <li>
      What is the success rate of decrypting previous messages in <abbr title="Secure Reader">SR</abbr> threading? How does that compare to the success rate of decrypting in <abbr title="Secure Reader">SR</abbr> overall?

      This helped prove <mark>we actually solved the user problem of seeing earlier parts of the conversation</mark> without going back to their email.

      <img
        src="{{ site.url }}/assets/sr_threading/data-success-rate.png"
        alt="Screenshot of week 1 98.4% successful decrypts for Secure Reader threading"
        class="screenshot screenshot-landscape zoomable"
      />

    </li>
  </ol>

  <h4>Qualitative feedback</h4>

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





<a name="3"></a>
## Retrospective

<p>
  I'm satisfied with the initial impact of this design. I'll revisit the retrospective when I have more distance from this effort.
</p>

<p>
  <a href="https://www.virtru.com/secure-collaboration/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2021)</a>
</p>

{% include footer_case_study.md %}
