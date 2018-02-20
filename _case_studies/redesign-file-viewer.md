---
layout: default
title: Redesign File Viewer
overview: Wireframe & redesign a file viewer for displaying 50+ file types online&mdash;a core part of the review workflow for 9000+ organizations.
skills: wireframing, visual design
date: 2018-01-31
cover_image: /assets/art.jpg
---

# <small>Case Study:</small> <br />Redesign File Viewer

<a href="https://www.submittable.com/" type="button" class="btn btn-success" target="_blank"><i class="material-icons">done</i>In Production</a> 

## Overview

Wireframe & redesign a file viewer for displaying 50+ file types online&mdash;a core part of the review workflow for 9000+ organizations.

## Problem Definition

Submittable provides an online platform to manage submissions and applications. A core part of this product involves reviewing various uploaded files to decide on any given submission. Our previous file viewer implementation and interface depended on a Box library that was being discontinued. This external deadline created an opportunity to revisit the UX for reviewing any kind of file Submittable accepts. The previous file viewer had discordant interfaces for viewing text-based files, images, audio, and video. We defined success as a consistent interface that was no longer dependent on Box.

## Audience

Our target users were the majority of the 9,000+ Submittable organizations who used our online file viewer to review and judge submissions. This excluded the minority of Submittable organizations who used Submittable to accept files but then downloaded and reviewed files elsewhere—paper, Kindle, or offline. A specific ratio of organizations who used our file viewer to those who reviewed files elsewhere was not available or measured.

Organizations ranged from literary journals with a single editor to larger organizations with numerous team members and multi-stage review processes. 

Due to the strict engineering deadline, we did not create specific personas. 

## Team / Role

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
1. I advocated for more iterative designs consisting of paper prototypes and wireframes.

## 1. Understand and Evolve the Spec 

The product manager started a spec with what functionality and UI affordances the new file viewer had to support. She also collected a few UI examples of other viewers in an InVision board. Inspired by this visual approach, I started capturing screenshots of how our current viewer handled various file types. I noted inconsistencies, got clarifications about historical decisions, and captured numerous edge cases not covered in the spec (e.g. how do we handle files a submitter is allowed to upload but our file converter cannot render, such as executables?). 

## 2. Experiment with Paper Cut-Outs

Due to the increasing number of states across the four file types (text, image, audio, video), I began on paper. I sketched affordances, cut them out, and rearranged them. The goal was to create more consistency across file type controls that are not naturally related, e.g. previous and next page in a document vs. volume controls in audio or video files.

> TODO: INCLUDE PAPER CUTOUTS IMG

I also explored various loading state iconography, stemming from our core brand icon.

> TODO: INCLUDE BRAND ICON
> TODO: INCLUDE LOADING STATE ICONS

Afterwards, proceeding bottom-up from the smallest UI elements to larger patterns, I played with different hierarchies within the file viewers. 

> TODO: INCLUDE HIERARCHIES IMG

I shared these concepts in person with the PM, the visual designer, and got the thumbs up to move to wireframes without significant feedback. Being in person was invaluable to physically moving around UI affordances in meetings, though I subsequently didn't capture all the states we experimented with. 

## 3. Create Wireframes

There were no wireframes or wireframing process at Submittable. I decided to introduce InVision Freehand to the team for creating, sharing, and gathering feedback on wireframes since everyone was already using InVision prototypes. I hoped the monochrome palette would make it clear these weren't the mocks I was expected to deliver.

> TODO: SHOW INITIAL FREEHAND

Freehand made it easy to show many low-fi screens at once, but quite difficult to leave comments. Users could only do so by inserting text into the Freehand itself. This proved to be a frustrating and limiting deviation from InVision prototype comments. 

My team mates were surprised at the number of states I displayed and wonder how these states rendered in our current viewer. In the next iteration, I included a screenshot of the current state right next to each wireframed screen.

> TODO: SHOW DESKTOP 2.0 FREEHAND STATES NEXT TO SCREENS

Only at this point did the visual designer inform me that we would also need mobile web designs for the viewer. I regretted not seeking that clarification up front in the spec, but added the mobile states:

> TODO: SHOW MOBILE FREEHAND STATES

## 4. First Mockups

By September 2017, I expected to start paternity leave any day. After I got approval for my wireframes, I proceeded to create the first mockups. 

I started with viewing text files. Engineering agreed that text files were crucial and would be built first.

> TODO: SHOW FIRST DOC MOCKUPS

I finished the initial mockups, walked the visual designer through my screens in InVision and my artboards in Sketch, and went on paternity leave for 30 days.

## 5. Iterate on Mockups

In the intervening 30 days, the visual designer had iterated quite a bit on my initial mocks. 

> TODO: SHOW SOCHA'S MOCKUPS

I returned from paternity leave just as the visual designer announced she was departing from the company. I iterated on the final visual details.

> TODO: SHOW FINAL MOCKUPS

## 6. Iterate in Parallel with Engineering 

Engineering began building both a backend implementation based on their requirements and a frontend implementation based on my final mockups in October 2017. I worked closely with the lead frontend engineer to work out small details. 

I started a Google Doc to keep a running list of improvements based on his emerging implementation. It took the form of a this is what I saw / this is what I expected list of items for him to triage. The process worked well for the two of us and we worked through the list, encouraging other stakeholders to provide input. 

> TODO: SHOW EXAMPLE FROM GOOGLE DOC

There were no substantial UI changes at this phase. 

## 7. Iterate After Launch in Response to User Feedback

Our VP of Engineering praised the production release of the new file viewer to being as close to a perfect release as they've had. 

Submittable organizations who've been longtime customers praised the file viewer:

> TODO: SHOW SUSAN & LINDA QUOTE

The majority of customer support requests involved backend issues relating to file conversion (e.g. missing fonts, unsupported files). The only prominent UI issue came from the bottom toolbar when viewing text files:

> TODO: SHOW "NOTCH" issue

I quickly suggested a few alternatives to our own innocent "notch" problem:

> TODO: SHOW "NOTCH" solutions

We expanded the toolbar to be full width, which reduced the viewing area by one line of text but never interfered with the reading experience and encouraged scrolling. 

# Retrospective

We reached our design goal of a new file viewer with a more consistent interface across numerous file types. Engineering deemed the new viewer a success. We took the lack of customer support issues as a big positive. 

I am satisfied with how the new file viewer looks and works. I'm proud of covering more states, especially loading and error states for those who experience slowness or problems. The mobile redesign is also a step in a more focused direction.

## How Would I Improve?

If I were to do this project again: 

1. Avoid InVision Freehand for feedback. Commenting by inserting text made it insufficient as a wireframing tool with a broken feedback experience. Seeking comments elsewhere would reduce friction when introducing wireframing to a team unfamiliar with the technique. 

1. Trade visual design time for usability testing. This was painfully missing from our process. It's hard to say we didn't simply get lucky that users were happy with the approach my interface took. 

1. Seek explicit user feedback, early. Since Submittable was reliant on qualitative feedback and lacks certain product metrics, I would seek direct feedback from users. During this project I suggested: 
  * prompting organizations for file viewer feedback via Intercom while they're in the product
  * emailing a follow up survey to organizations who've used the new file viewer

  Both ideas were shot down because we weren't sure "the UI changes are obvious enough to most users such that asking for feedback would be meaningful." I respectfully disagree.

## Example of the production viewer, as of February 2018:

> TODO: SHOW EXAMPLE VIEWER WITH GATSBY?

<a href="https://www.submittable.com/" type="button" class="btn btn-success" target="_blank"><i class="material-icons">done</i>In Production</a> 

{% include footer_case_study.md %}