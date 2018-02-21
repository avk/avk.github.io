---
layout: default
title: Redesign File Viewer
overview: Wireframe & redesign a file viewer for displaying 50+ file types online&mdash;a core part of the review workflow for 9000+ organizations.
skills: wireframing, visual design
date: 2018-01-31
cover_image: /assets/file_viewer/production-text-fullscreen.png
---

![Work sample from this case study]({{ site.url }}/assets/file_viewer/production-text-fullscreen.png)

# <small>Case Study:</small> <br />Redesign File Viewer

<a href="https://www.submittable.com/" type="button" class="btn btn-success" target="_blank"><i class="material-icons">done</i>In Production</a> 

## Overview

Wireframe & redesign a file viewer for displaying 50+ file types online&mdash;a core part of the review workflow for 9000+ organizations.

## Problem Definition

Submittable provides online tools to manage submissions and applications. A core part of this product involves reviewing various uploaded files to judge any given submission. Our previous file viewer implementation and interface depended on a Box library that Box would discontinue. This external deadline created an opportunity to revisit the UX for reviewing any kind of file Submittable accepts. The previous file viewer had discordant interfaces for viewing text-based files, images, audio, and video. It was responsible for over 50 distinct file types if we count file extensions. We defined success as a consistent interface that was no longer dependent on Box.

## Audience

Our target users were the majority of the 9,000+ Submittable organizations who used our online file viewer to review submissions. This excluded the minority of organizations who reviewed files outside of Submittable—paper, Kindle, or offline. A specific ratio of organizations who used our file viewer to those who reviewed files elsewhere was not available or measured.

Organizations ranged from literary journals with a single editor to large teams with multi-stage review processes. 

No personas existed; due to the strict engineering deadline, we did not invest time to create them. 

## My Role on the Team

As **Senior UX Designer**, in August 2017, I joined a team consisting of:

* a visual designer&mdash;departed before project completion
* a product manager (PM)
* two engineers

From August-October, I ran deliverables by the visual designer and the PM. Afterwards, I largely collaborated with engineering on the implementation.

## Constraints

Our primary constraints:

1. Hard deadline to be in production for 100% of Submittable organizations by January 15, 2018&mdash;when the Box View API would be discontinued.
1. I was 100% remote for all but the initial 2 weeks of the project. This limited time for any casual, in-person testing.
1. I planned to take one month of paternity leave in early Fall 2017.
1. Our only source of user feedback were customer support requests. We did not budget time for prototype or usability testing due to the hard deadline and uncertainty with how much time engineering would need for the new implementation.

# Design Process

## Design Deliverables

1. Engineering and the PM requested mockups in InVision for viewing:
    * text-based files
    * image files
    * audio files
    * video files
1. I advocated for and got buy in to create more iterative designs consisting of paper prototypes and wireframes.

## 1. Understand and Evolve the Spec 

The product manager started a spec with what functionality and UI affordances the new file viewer had to support. She also collected a few UI examples of other viewers in an InVision board. I started capturing screenshots of how our current viewer handled various file types. I noted inconsistencies, got clarifications about historical decisions, and captured cases not covered in the spec. For example, how do we handle files a submitter can upload but our file converter cannot render, such as executables?

![Notes on current UI]({{ site.url }}/assets/file_viewer/initial-notes.jpg)

## 2. Experiment with Paper Cut-Outs

Due to the increasing number of states across the four file types (text, image, audio, video), I began on paper. I sketched affordances, cut them out, and rearranged them. The goal was to create more consistency across file type controls that are not naturally related.

> Can we find consistency across affordances like previous/next page in a document and volume controls in audio &amp; video?

![Reorder-able paper affordances]({{ site.url }}/assets/file_viewer/paper-ui.jpg)

Afterwards, I worked bottom-up from the smallest UI elements to larger patterns. I played with different hierarchies within the file viewers.

![Hierarchy concept sketches]({{ site.url }}/assets/file_viewer/hierarchy-concepts.jpg)

I shared these concepts in person with the PM, the visual designer. I proceeded to wireframes without significant feedback. 

> Being in person was invaluable to physically moving around UI affordances in meetings, though I subsequently didn't capture all the states we experimented with. 

## 3. Create Wireframes

There were no wireframes or wireframing process at Submittable. I decided to introduce InVision Freehand to the team since we were already using InVision prototypes. I hoped the monochrome palette would make it clear these weren’t the mocks the team expected from me.

I employed [Scott Hurff's UI Stack concept](http://scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack) to structure my wireframes into more thorough states.

![The UI Stack]({{ site.url }}/assets/file_viewer/ui-stack.jpg)

I surprised my team with the number of states I covered. They wondered how these states rendered in our current viewer. Thus, I included a screenshot of the current state before each wireframed screen.

![Initial wireframes in Freehand]({{ site.url }}/assets/file_viewer/wires-1.png)

![Detailed wireframes in Freehand]({{ site.url }}/assets/file_viewer/wires-1-compare.png)

> Freehand made it easy to show many low-fi screens at once, but quite difficult to leave comments. 

Users could only comment by inserting text into the Freehand itself. This proved to be a frustrating and limiting deviation from InVision prototype comments. 

Only at this point did the visual designer inform me that we would also need mobile web designs for the viewer. I regretted not seeking that clarification up front in the spec, but added the mobile states:

![Mobile wireframes in Freehand]({{ site.url }}/assets/file_viewer/wires-2-mobile.png)

![Detailed mobile wireframes in Freehand]({{ site.url }}/assets/file_viewer/wires-2-mobile-detail.png)


## 4. First Mockups

By September 2017, I expected to start paternity leave any day. After I got approval for my wireframes, I proceeded to create the first mockups in Sketch. 

I started with viewing text files. Engineering agreed that text files were crucial and they would start with that viewer experience.

![My first mockups]({{ site.url }}/assets/file_viewer/mocks-1.png)

When I finished the initial mockups, I walked the visual designer through my InVision screens and Sketch artboards. Then, I went on paternity leave for 30 days.

## 5. Iterate on Mockups

In the intervening 30 days, the visual designer had iterated quite a bit on my initial mocks. 

![Mockup iterations during my leave]({{ site.url }}/assets/file_viewer/mocks-iterated.png)

I returned from paternity leave just as the visual designer announced she was departing from the company. I iterated on the final visual details to the satisfaction of product and engineering.

![My final mockups]({{ site.url }}/assets/file_viewer/mocks-final.png)

![My final mobile mockups]({{ site.url }}/assets/file_viewer/mocks-final-mobile.png)

## 6. Iterate in Parallel with Engineering 

Engineering began building in October 2017. They based the backend implementation on their requirements. They based the frontend implementation on my final mockups. I worked closely with the lead frontend engineer to work out small details.

I started a Google Doc to keep a running list of improvements based on his emerging implementation. 

> My feedback took the form of an observed vs. expected list of items for the engineer to triage. 

The process worked well for the two of us. We worked through the list, encouraging other stakeholders to provide input. They did so and followed my format.

![Observed-expected feedback example]({{ site.url }}/assets/file_viewer/eng-diffs.png)

There were no substantial UI changes at this phase. 

## 7. Iterate After Launch in Response to User Feedback

Our VP of Engineering praised the production release of the new file viewer to being as close to a perfect release as they've had. 

Submittable organizations who've been longtime customers praised the file viewer:

> "I'm LIKING what I see so far..." <br />&mdash;a longtime customer

Most customer support requests involved backend issues (e.g. missing fonts, unsupported files). The only prominent UI issue came from the bottom toolbar when viewing text files:

![Reading issue from bottom toolbar]({{ site.url }}/assets/file_viewer/notch-problem.png)

I suggested a few alternatives to our own innocent "notch" problem:

![Reading issue solutions]({{ site.url }}/assets/file_viewer/notch-solutions.png)

We expanded the toolbar to be full width. This reduced the viewing area by one line of text but never interfered with the reading experience.

# Retrospective

We reached our design goal of a new file viewer with a more consistent interface across 50+ file types. Engineering deemed the new viewer a success. We interpreted the lack of customer support issues as a big positive. 

I am satisfied with how the new file viewer looks and works. I'm proud of covering more states, especially loading and error states for users who experience slowness or problems. The mobile redesign was also a step in a more focused direction for 20% of our 2017 traffic.

## How Would I Improve?

If I were to do this project again: 

1. __Avoid InVision Freehand for feedback.__ Commenting by inserting text is a poor feedback experience that didn't reflect well on wireframing as an approach. Seeking comments elsewhere would reduce friction when introducing wireframing to a team unfamiliar with the technique. 

1. __Trade visual design time for usability testing.__ This was painfully missing from our process. Perhaps we got lucky that users were happy with the approach our interface took. I prefer to validate my guesses.

1. __Seek explicit user feedback, earlier.__ Submittable is reliant on qualitative feedback and lacks certain product metrics. Thus, I would seek direct feedback from users. During this project I suggested: 
  * doing a task analysis or otherwise light prototype testing using our InVision mockups
  * prompting organizations for file viewer feedback via Intercom while they're in the product
  * emailing a follow up survey to organizations who've used the new file viewer

  We didn't act on those ideas. Product wasn’t convinced the UI changes were obvious enough such that asking for feedback would be meaningful. I would still pursue some form of follow feedback to test our assumptions, especially at the interaction level.

## Previous file viewer, July 2017:

![2017 file viewer with text]({{ site.url }}/assets/file_viewer/production-text-before.png)

## New file viewer, January 2018:

![New file viewer with text]({{ site.url }}/assets/file_viewer/production-text.png)

![New file viewer with text in full screen]({{ site.url }}/assets/file_viewer/production-text-fullscreen.png)

{% include footer_case_study.md %}