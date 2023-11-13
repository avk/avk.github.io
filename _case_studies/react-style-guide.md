---
layout: default
title: React-driven Living Style Guide
overview: Enabled tighter design-engineering feedback loops, faster regression testing, and higher quality production releases.
skills: prototyping, engineering
date: 2015-12-20
cover_image: /assets/sg/first-components.png
active: false
---

![Work sample from this case study]({{ site.url }}/assets/sg/first-components.png)

# <small>Case Study:</small> <br />React-driven Living Style Guide

<a href="https://www.therightmargin.com/?ref=avkux" type="button" class="btn btn-secondary" target="_blank">&#10004; In Staging (2016-20)</a>

> I gave a talk on this topic at the May 2017 [ReactJS San Francisco meetup](https://www.meetup.com/ReactJS-San-Francisco/events/232716790/).

## Overview

Enabled tighter design-engineering feedback loops, faster regression testing, and higher quality production releases.

## Skills Used

* prototyping
* engineering

## Problem Definition

<details>

  <p>
    At TheRightMargin's early startup phase, we followed a rapid design and development cycle for our online writing product. We shipped fixes and features every two weeks while still validating our business model.
  </p>

  <p>
    While our new front-end architecture of <a href="https://facebook.github.io/react/">React.js</a> components sped up ideation and development, our design consistency and quality suffered. Our product evolved so quickly that many states weren't designed for, taken into account in the code, and missed during our equally rapid-fire regression testing.
  </p>

  <blockquote>
    <p>
      Problem: How can we set a baseline of design quality without sacrificing startup speed?
    </p>
  </blockquote>

</details>

## Audience

<details>
  <p>
    Our audience for this quality problem was our small, fast-moving startup team whose mistakes cascaded to a subpar product experience.
  </p>
</details>

## My Role on the Team

<details>

  <p>
    As Senior UX Designer &amp; Engineer, I worked on a team of four:
  </p>

  <ul>

    <li>
      with our UX Designer to create tighter design-engineering feedback loops
    </li>

    <li>
      with our full-stack engineer to define the smallest amount of effort to solve the problem
    </li>

    <li>
      with our founder to reshape how we explored new features and regression tested what was implemented
    </li>

  </ul>

</details>

## Constraints

<details>
  <p>
    The primary constraint was scope. The team acknowledged the design quality problem but struggled with how much time or effort to devote to improving it.
  </p>
</details>

# Design Process

## Tracing the problem's root causes

<details>

  <p>
    Initial discussions led to the following insights:
  </p>

  <ul>

    <li>
      regression testing tends to take too long and thus the team hesitates doing a thorough job (Founder)
    </li>

    <li>
      click testing all possible states is time-consuming (UX Designer)
    </li>

    <li>
      regression testing uncovers problems that may have been designed and engineered for earlier in the process (me)
    </li>

  </ul>

</details>

## 1st solution: Regression testing script

<details>

  <p>
    If regression testing is valuable but time-consuming, can we solve this problem with a script or checklist? Here are the areas of the product you should check. I wrote a script that enumerated basic product interactions—largely <abbr title="Create, Read, Update, and Delete">CRUD</abbr>. The script became a checklist in a recurring Trello card that we could use for regression testing every two weeks.
  </p>

  <p>
    While exhaustive, the script's length only reinforced that regression testing was a lot of work. Everyone, myself included, felt intimidated by the long list. It also didn't address how problems could be found earlier.
  </p>

  <blockquote>
    <p>
      Observation: the checklist begged to be nested by product feature or area, which usually mirrored a React component or set of nested components
    </p>
  </blockquote>

</details>

### Current React component hierarchy

<details>
  <p>
    <img src="{{ site.url }}/assets/sg/hierarchy.jpg" alt="Current React component hierarchy">
  </p>
</details>

## 2nd solution: Integration testing our UI in code

<details>

  <p>
    Could we transform my regression testing script from the previous solution to a set of integration tests for our interface? I explored testing our interface in code as an option with our full-stack engineer. From our past experience:
  </p>

  <ul>

    <li>
      integration tests are generally slower to write due to their dependence on particular markup, even if React components generate the markup
    </li>

    <li>
      integration tests are generally slower to execute, though faster than manual click testing a regression build
    </li>

    <li>
      integration tests quickly become outdated, as the underlying markup changes
    </li>

    <li>
      this may be an especially poor investment of time given how rapidly our product is evolving
    </li>

  </ul>

  <blockquote>
    <p>
      Observation: developing React components addresses some of the pains of traditional DOM-based integration testing
    </p>
  </blockquote>

</details>

## Breakthrough Insight

<details>


  <p>
    I took a step back and saw a connection between these points:
  </p>

  <ul>
    <li>click testing all possible states is time-consuming (UX Designer)</li>
  </ul>

  <p>
    &hellip;because this requires remembering. But a regression testing script is an intimidating way to jog your memory.
  </p>

  <ul>

    <li>
      <p>
        Observation: the checklist begged to be nested by product feature or area, which usually mirrored a React component or set of nested components
      </p>
    </li>

    <li>
      <p>
        integration tests are generally slower to write due to their dependence on particular markup, even if React components generate the markup
      </p>
    </li>

  </ul>

  <blockquote>
    <p>
      Couldn't there be a happy middle between a <em>static script</em> that you have to act on and <em>fully-automated test suite</em> that becomes quickly outdated?
    </p>
  </blockquote>

</details>

## 3rd Solution: React-driven Style Guide

<details>

  <p>
    Given that React components can be:
  </p>

  <ol>

    <li>
      initially rendered via a series of properties (props)
    </li>

    <li>
      and then transformed (state)
    </li>

  </ol>

  <p>
    let's render each component of our main interface separately, with all likely properties.
  </p>

  <p>
    This would be a way to visually enumerate all the ways a component can begin. It would still be up to someone to click test but at least they begin from a complete set of initial possibilities. They don't have to remember them or reference them from a long script. Furthermore, properties are much easier to maintain and update than markup, so the maintenance cost is much lower than traditional integration tests. We're trading code-level thoroughness for a faster jumping off point.
  </p>

</details>

### Self-documenting

<details>

  <p>
    I built the style guide to be self-documenting, every component is grouped by name and documents it's own properties:
  </p>

  <p>
    <img src="{{ site.url }}/assets/sg/first-components.png" alt="example components with props">
  </p>

</details>

### Backgrounds

<details>

  <p>
    Different background colors support various background colors and help find what should be white vs. transparent:
  </p>

  <p>
    <img src="{{ site.url }}/assets/sg/bg-1.png" alt="picking a new background">
  </p>

  <p>
    <img src="{{ site.url }}/assets/sg/bg-2.png" alt="the new background applied">
  </p>

</details>

### Real components

<details>

  <p>
    Because each rendered component is an actual part of our app, they can be a quick way to test things like hover states and interactivity:
  </p>

  <p>
    <img src="{{ site.url }}/assets/sg/interact-component.gif" alt="interacting with a component">
  </p>

</details>

### Catching problems

<details>

  <p>
    New visual bugs, inconsistencies, and states that weren't designed or implemented are quick to spot:
  </p>

  <p>
    <img src="{{ site.url }}/assets/sg/bug.png" alt="inconsistencies">
  </p>

</details>

### Easier triage

<details>
  <p>
    The style guide is available at an admin-only URL available on production, staging, and local servers. This makes bugs easier to reproduce, isolate, and fix, based on what code is running.
  </p>
</details>

# Retrospective

<details>

  <p>
    The style guide became our de-facto launching point for discussing new features and designs. It became much easier to see where things can move or what may be affected. Design critiques and feedback loops tightened. The React-driven style guide sped up regression testing and we shipped more consistently designed features.
  </p>

  <p>
    If I were to repeat this process, I would consider new open source tools that emerged to solve similar problems, such as <a href="https://storybooks.js.org/">React Storybook</a>.
  </p>

  <blockquote>
    <p>
      I gave a talk on this topic at the May 2017 <a href="https://www.meetup.com/ReactJS-San-Francisco/events/232716790/">ReactJS San Francisco meetup</a>.
    </p>
  </blockquote>

</details>

## Final style guide

![TheRightMargin's React-driven style guide]({{ site.url }}/assets/sg/full-style-guide.png)

<a href="https://www.therightmargin.com/?ref=avkux" type="button" class="btn btn-secondary" target="_blank">&#10004; In Staging (2016-20)</a>

{% include footer_case_study.md %}
