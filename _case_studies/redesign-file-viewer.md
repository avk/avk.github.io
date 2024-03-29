---
layout: default
title: Redesign File Viewer for 9,000+ Creative Orgs
overview: 50+ file types consistently displayed on desktop & mobile in &ldquo;as close to a <mark>perfect release</mark> as we've had.&rdquo;
skills: wireframing, visual design
date: 2018-01-31
cover_image: /assets/file_viewer/production-text-fullscreen.png
active: true
---

<img
  src="{{ site.url }}/assets/file_viewer/production-text-fullscreen.png"
  alt="Work sample from this case study"
  class="screenshot screenshot-landscape"
/>

# <small>Case Study:</small> <br />Redesign File Viewer for 9,000+ Creative Orgs

<a href="https://www.submittable.com/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2018-now)</a>





* [Overview](#1)
  * [Skills Used](#1.1)
  * [Problem Definition](#1.2)
  * [Audience](#1.3)
  * [Team](#1.4)
  * [Constraints](#1.5)

* [Design Process](#2)
  1. [Understand and Evolve the Spec](#2.1)
  2. [Experiment with Paper Cut-Outs](#2.2)
  3. [Create Thorough Wireframes](#2.3)
  4. [Start Mockups](#2.4)
  5. [Iterate on Mockups](#2.5)
  6. [Iterate in Parallel with Engineering](#2.6)
  7. [Iterate After Launch with User Feedback](#2.7)

* [Retrospective](#3)
* [Before & After](#4)

<hr />





<a name="1"></a>
## Overview

Wireframe & redesign a file viewer for displaying 50+ file types online&mdash;a core part of the review workflow for 9000+ organizations.

<a name="1.1"></a>
### Skills Used

* <mark>wireframing</mark>
* <mark>visual design</mark>

<a name="1.2"></a>
### Problem Definition

  <p>
    Submittable provides online tools to manage submissions and applications. A core part of this product involves reviewing various uploaded files to judge any given submission. Our previous file viewer implementation and interface depended on a Box library that Box would discontinue. This external deadline created an opportunity to revisit the UX for reviewing any kind of file Submittable accepts. <mark>The previous file viewer had discordant interfaces for viewing text-based files, images, audio, and video.</mark> It was responsible for over 50 distinct file types. We defined success as a consistent interface that was no longer dependent on Box.
  </p>

<a name="1.3"></a>
### Audience

  <p>
    Our target users were the majority of the 9,000+ Submittable organizations who used our online file viewer to review submissions. This excluded the minority of organizations who reviewed files outside of Submittable—paper, Kindle, or offline. A specific ratio of organizations who used our file viewer to those who reviewed files elsewhere was not available or measured.
  </p>
  <p>
    Organizations ranged from <mark>literary journals with a single editor to large teams with multi-stage review processes.</mark>
  </p>
  <p>
    No personas existed; due to the strict engineering deadline, we did not invest time to create them.
  </p>

<a name="1.4"></a>
### Team

  <p>
    As <mark>Senior UX Designer</mark>, in August 2017, I joined a team consisting of:
  </p>

  <ul>
    <li>a visual designer&mdash;first half of project</li>
    <li>a product manager (PM)</li>
    <li>two engineers</li>
  </ul>

  <p>
    From August-October, I ran deliverables by the visual designer and the PM. Afterwards, I largely collaborated with engineering on the implementation.
  </p>

<a name="1.5"></a>
### Constraints

  <p>Our primary constraints:</p>

  <ol>
    <li><mark>Hard deadline to be in production</mark> for 100% of Submittable organizations by January 15, 2018&mdash;when the Box View API would be discontinued.</li>
    <li>I was 100% remote for all but the initial 2 weeks of the project. This limited time for any casual, in-person testing.</li>
    <li>I planned to take one month of paternity leave in early Fall 2017.</li>
    <li>Our only source of user feedback were customer support requests. We did not budget time for prototype or usability testing due to the hard deadline and uncertainty with how much time engineering would need for the new implementation.</li>
    <li><mark>Our visual designer left</mark> before project completion</li>
  </ol>





<a name="2"></a>
## Design Process

  <ol>
    <li>
      Engineering and the PM requested mockups in InVision for viewing:
      <ul>
        <li>text-based files</li>
        <li>image files</li>
        <li>audio files</li>
        <li>video files</li>
      </ul>
    </li>

    <li>
      I advocated for and <mark>got buy in to create more iterative designs</mark> consisting of paper prototypes and wireframes.
    </li>

  </ol>

<a name="2.1"></a>
### 1. Understand and Evolve the Spec

  <p>
    The product manager started a spec with what functionality and UI affordances the new file viewer had to support. She also collected a few UI examples of other viewers in an InVision board. I started capturing screenshots of how our current viewer handled various file types. I noted inconsistencies, got clarifications about historical decisions, and captured cases not covered in the spec. For example, how do we handle files a submitter can upload but our file converter cannot render, such as executables?
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/initial-notes.jpg"
      alt="Notes on current UI"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

<a name="2.2"></a>
### 2. Experiment with Paper Cut-Outs

  <p>
    Due to the increasing number of states across the four file types (text, image, audio, video), I began on paper. I sketched affordances, cut them out, and rearranged them. The goal was to <mark>create more consistency across file type controls</mark> that are not naturally related.
  </p>

  <blockquote>
    <p>Can we find consistency across affordances like previous/next page in a document and volume controls in audio &amp; video?</p>
  </blockquote>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/paper-ui.jpg"
      alt="Reorder-able paper affordances"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    Afterwards, I worked bottom-up from the smallest UI elements to larger patterns. I played with different hierarchies within the file viewers.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/hierarchy-concepts.jpg"
      alt="Hierarchy concept sketches"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    I shared these concepts in person with the PM, the visual designer. I proceeded to wireframes without significant feedback.
  </p>

  <blockquote>
    <p>Being in person was invaluable to physically moving around UI affordances in meetings, though I subsequently didn't capture all the states we experimented with.</p>
  </blockquote>

<a name="2.3"></a>
### 3. Create Thorough Wireframes

  <p>
    There were no wireframes or wireframing process at Submittable. I decided to introduce InVision Freehand to the team since we were already using InVision prototypes. I hoped the monochrome palette would make it clear these weren’t the mocks the team expected from me.
  </p>

  <p>
    I employed <a href="https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/">Scott Hurff's UI Stack concept</a> to structure my wireframes into more thorough states.
  </p>

  <p><img src="{{ site.url }}/assets/file_viewer/ui-stack.jpg" alt="The UI Stack"></p>

  <p>
    <mark>I surprised my team with the number of states I covered</mark>. They wondered how these states rendered in our current viewer. Thus, I included a screenshot of the current state before each wireframed screen.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/wires-1.png"
      alt="Initial wireframes in Freehand"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/wires-1-compare.png"
      alt="Detailed wireframes in Freehand"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <blockquote>
    <p>Freehand made it easy to show many low-fi screens at once, but quite difficult to leave comments.</p>
  </blockquote>

  <p>
    Users could only comment by inserting text into the Freehand itself. This proved to be a frustrating and limiting deviation from InVision prototype comments.
  </p>

  <p>
    Only at this point did the visual designer inform me that we would also need mobile web designs for the viewer. I regretted not seeking that clarification up front in the spec, but added the mobile states:
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/wires-2-mobile.png"
      alt="Mobile wireframes in Freehand"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/wires-2-mobile-detail.png"
      alt="Detailed mobile wireframes in Freehand"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>





<a name="2.4"></a>
### 4. Start Mockups

  <p>
    By September 2017, I expected to start paternity leave any day. After I got approval for my wireframes, I proceeded to create the first mockups in Sketch.
  </p>

  <p>
    I started with viewing text files. Engineering agreed that text files were crucial and they would start with that viewer experience.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/mocks-1.png"
      alt="My first mockups"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    When I finished the initial mockups, I walked the visual designer through my InVision screens and Sketch artboards. Then, I went on paternity leave for 30 days.
  </p>





<a name="2.5"></a>
### 5. Iterate on Mockups

  <p>
    In the intervening 30 days, the visual designer had iterated quite a bit on my initial mocks.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/mocks-iterated.png"
      alt="Mockup iterations during my leave"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    I returned from paternity leave just as the visual designer announced she was departing from the company. I iterated on the final visual details to the satisfaction of product and engineering.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/mocks-final.png"
      alt="My final mockups"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/mocks-final-mobile.png"
      alt="My final mobile mockups"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>





<a name="2.6"></a>
### 6. Iterate in Parallel with Engineering

  <p>
    Engineering began building in October 2017. They based the backend implementation on their requirements. They based the frontend implementation on my final mockups. I worked closely with the lead frontend engineer to work out small details.
  </p>

  <p>
    I started a Google Doc to keep a running list of improvements based on his emerging implementation.
  </p>

  <blockquote>
    <p>My feedback took the form of an observed vs. expected list of items for the engineer to triage.</p>
  </blockquote>

  <p>
    The process worked well for the two of us. We worked through the list, encouraging other stakeholders to provide input. They did so and followed my format.
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/eng-diffs.png"
      alt="Observed-expected feedback example"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>There were no substantial UI changes at this phase.</p>





<a name="2.7"></a>
### 7. Iterate After Launch with User Feedback

  <p>
    Our <mark>VP of Engineering praised the production release</mark> of the new file viewer to being as close to a perfect release as they've had.
  </p>

  <p>
    Submittable organizations who've been <mark>longtime customers praised the file viewer</mark>:
  </p>

  <blockquote>
    <p>&quot;I'm LIKING what I see so far...&quot; <br />&mdash;a longtime customer</p>
  </blockquote>

<details>
    <summary>Challenge: an unintentional "notch"</summary>
  <p>
    Most customer support requests involved backend issues (e.g. missing fonts, unsupported files). The only prominent UI issue came from the bottom toolbar when viewing text files:
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/notch-problem.png"
      alt="Reading issue from bottom toolbar"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    I suggested a few alternatives to our own innocent &quot;notch&quot; problem:
  </p>

  <p>
    <img
      src="{{ site.url }}/assets/file_viewer/notch-solutions.png"
      alt="Reading issue solutions"
      class="screenshot screenshot-landscape zoomable"
    />
  </p>

  <p>
    We expanded the toolbar to be full width. This reduced the viewing area by one line of text but never interfered with the reading experience.
  </p>
</details>





<a name="3"></a>
## Retrospective

<details>
  <p>
    We reached our design goal of a new file viewer with a more consistent interface across 50+ file types. Engineering deemed the new viewer a success. We interpreted the lack of customer support issues as a big positive.
  </p>

  <p>
    I'm proud of covering more states in the new viewer, especially loading and error states for users who experience slowness or problems. The mobile redesign was also a step in a better direction to serve 20% of our 2017 traffic.
  </p>

  <p>
    If I were to do this project again:
  </p>

  <ol>
    <li>
      <p>
        <strong>Avoid InVision Freehand for feedback.</strong> Commenting by inserting text is a poor feedback experience that didn't reflect well on wireframing as an approach. Seeking comments elsewhere would reduce friction when introducing wireframing to a team unfamiliar with the technique.
      </p>
    </li>
    <li>
      <p>
        <strong>Trade visual design time for usability testing.</strong> This was painfully missing from our process. Perhaps we got lucky that users were happy with the approach our interface took. I prefer to validate my guesses.
      </p>
    </li>
    <li>
      <p>
        <strong>Seek explicit user feedback, earlier.</strong> Submittable is reliant on qualitative feedback and lacks certain product metrics. Thus, I would seek direct feedback from users. During this project I suggested:
      </p>

      <ul>
        <li>
          doing a task analysis or otherwise light prototype testing using our InVision mockups
        </li>
        <li>
          prompting organizations for file viewer feedback via Intercom while they're in the product
        </li>
        <li>
          emailing a follow up survey to organizations who've used the new file viewer
        </li>
      </ul>

      <p>
        We didn't act on those ideas. Product wasn’t convinced the UI changes were obvious enough such that asking for feedback would be meaningful. I would still pursue some form of follow feedback to test our assumptions, especially at the interaction level.
      </p>
    </li>
  </ol>
</details>





<a name="4"></a>
## Before & After

__Previous file viewer, July 2017:__

<img
  src="{{ site.url }}/assets/file_viewer/production-text-before.png"
  alt="2017 file viewer with text"
  class="screenshot screenshot-landscape screenshot-borderless zoomable"
/>

__New file viewer, January 2018:__

<img
  src="{{ site.url }}/assets/file_viewer/production-text.png"
  alt="New file viewer with text"
  class="screenshot screenshot-landscape screenshot-borderless zoomable"
/>

<img
  src="{{ site.url }}/assets/file_viewer/production-text-fullscreen.png"
  alt="New file viewer with text in full screen"
  class="screenshot screenshot-landscape screenshot-borderless zoomable"
/>

<a href="https://www.submittable.com/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2018-now)</a>

{% include footer_case_study.md %}
