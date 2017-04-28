---
layout: default
title: React-driven Style Guide
overview: Leveraging React for tighter design-engineering feedback loops and better quality production releases. 
date: 2015-12-20
---

![Work sample from this case study]({{ site.url }}/assets/sg/cover.png)

# <small>Case Study</small>: <br />React-driven Style Guide

> I plan to give a talk on this topic at the May 2017 [ReactJS San Francisco meetup](https://www.meetup.com/ReactJS-San-Francisco/). 

## Overview

Leveraging React for tighter design-engineering feedback loops and better quality production releases. 

## Problem Definition

At TheRightMargin's early startup phase, we followed a rapid design and development cycle for our online writing product. We shipped fixes and features every two weeks while still validating our business model. 

While our new front-end architecture of [React.js](https://facebook.github.io/react/) components sped up ideation and development, our design consistency and quality suffered. Our product evolved so quickly that many states weren't designed for, taken into account in the code, and missed during our equally rapid-fire regression testing. 

> Problem: How can we set a baseline of design quality without sacrificing startup speed?

## Audience

Our audience for this quality problem was our small, fast-moving startup team whose mistakes cascaded to a subpar product experience. 

## Team / Role

As Senior UX Engineer, I worked on a team of four: 
* with our UX Designer to create tighter design-engineering feedback loops
* with our full-stack engineer to define the smallest amount of effort to solve the problem
* with our founder to reshape how we explored new features and regression tested what was implemented

## Constraints

The primary constraint was scope. The team acknowledged the design quality problem but struggled with how much time or effort to devote to improving it.

# Design Process

What was your design process? 
Did you facilitate any design exercises? 
What deliverables were you responsible for? 
Speak to messiness.

## Tracing the problem's root causes

Initial discussions led to the following insights:

* regression testing tends to take too long and thus the team hesitates doing a thorough job (Founder)
* click testing all possible states is time-consuming (UX Designer)
* regression testing uncovers problems that may have been designed and engineered for earlier in the process (me)

## 1st solution: Regression testing script

If regression testing is valuable but time-consuming, can we solve this problem with a script or checklist? Here are the areas of the product you should check. I wrote a script that enumerated basic product interactions—largely <abbr title="Create, Read, Update, and Delete">CRUD</abbr>. The script became a checklist in a recurring Trello card that we could use for regression testing every two weeks.

While exhaustive, the script's length only reinforced that regression testing was a lot of work. Everyone, myself included, felt intimidated by the long list. It also didn't address how problems could be found earlier. 

> Observation: the checklist begged to be nested by product feature or area, which usually mirrored a React component or set of nested components

### Current React component hierarchy

![Current React component hierarchy]({{ site.url }}/assets/sg/hierarchy.jpg)

## 2nd solution: Integration testing our UI in code

Could we transform my regression testing script from the previous solution to a set of integration tests for our interface? I explored testing our interface in code as an option with our full-stack engineer. From our past experience:

* integration tests are generally slower to write due to their dependence on particular markup, even if React components generate the markup
* integration tests are generally slower to execute, though faster than manual click testing a regression build
* integration tests quickly become outdated, as the underlying markup changes
* this may be an especially poor investment of time given how rapidly our product is evolving

> Observation: developing React components addresses some of the pains of traditional DOM-based integration testing

## Breakthrough Insight

I took a step back and saw a connection between these points:

* click testing all possible states is time-consuming (UX Designer)

...because this requires remembering. But a regression testing script is an intimidating way to jog your memory.

* Observation: the checklist begged to be nested by product feature or area, which usually mirrored a React component or set of nested components

* integration tests are generally slower to write due to their dependence on particular markup, even if React components generate the markup

> Couldn't there be a happy middle between a *static script* that you have to act on and *fully-automated test suite* that becomes quickly outdated?

## 3rd Solution: React-driven Style Guide

Given that React components can be: 

1. initially rendered via a series of properties (props) 
2. and then transformed (state)

let's render each component of our main interface separately, with all likely properties. 

This would be a way to visually enumerate all the ways a component can begin. It would still be up to someone to click test but at least they begin from a complete set of initial possibilities. They don't have to remember them or reference them from a long script. Furthermore, properties are much easier to maintain and update than markup, so the maintenance cost is much lower than traditional integration tests. We're trading code-level thoroughness for a faster jumping off point. 

### Self-documenting

I built the style guide to be self-documenting, every component is grouped by name and documents it's own properties:

![example components with props]({{ site.url }}/assets/sg/first-components.png)

### Backgrounds

Different background colors support various background colors and help find what should be white vs. transparent:

![picking a new background]({{ site.url }}/assets/sg/bg-1.png)

![the new background applied]({{ site.url }}/assets/sg/bg-2.png)

### Real components

Because each rendered component is an actual part of our app, they can be a quick way to test things like hover states and interactivity:

![interacting with a component]({{ site.url }}/assets/sg/interact-component.gif)

### Catching problems

New visual bugs, inconsistencies, and states that weren't designed or implemented are quick to spot:

![inconsistencies]({{ site.url }}/assets/sg/bug.png)

### Easier triage

The style guide is available at an admin-only URL available on production, staging, and local servers. This makes bugs easier to reproduce, isolate, and fix, based on what code is running.

# Retrospective

The style guide became our de-facto launching point for discussing new features and designs. It became much easier to see where things can move or what may be affected. Design critiques and feedback loops tightened. The React-driven style guide sped up regression testing and we shipped more consistently designed features. 

If I were to repeat this process, I would consider new open source tools that emerged to solve similar problems, such as [React Storybook](https://storybooks.js.org/).

> I plan to give a talk on this topic at the May 2017 [ReactJS San Francisco meetup](https://www.meetup.com/ReactJS-San-Francisco/). 

## Final style guide

![TheRightMargin's React-driven style guide]({{ site.url }}/assets/sg/full-style-guide.png)

{% include footer_case_study.md %}