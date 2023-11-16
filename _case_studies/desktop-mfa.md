---
layout: default
title: Protecting Every macOS Login with Desktop MFA 
overview: Generated $1mm ARR in first 7 weeks by protecting users on every login to their Mac or PC
skills: prototyping, visual design, usability testing
date: 2023-10-05
active: true
---

# <small>Case Study:</small> <br />Protecting Every macOS Login with Desktop MFA

<a href="#" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2023)</a>



* [Overview](#1)
  * [Problem Definition](#1.1)
  * [Skills Used](#1.2)
  * [My Role on the Team](#1.3)

* [Design Process](#2)


* [Retrospective](#3)



## Overview



### Problem Definition

<img
  src="{{ site.url }}/assets/mfa/macOS-pw-login.png"
  alt="Password prompt on macOS 12"
  class="screenshot screenshot-landscape"
/>

Passwords are no longer enough to protect employees logging into their work Mac or PC. These sensitive computers now require Multi-Factor Authentication (MFA) to comply with cybersecurity insurance requirements or follow the [Executive Order on Improving the Nation’s Cybersecurity](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/). Computer logins now <mark>require a password and a separate factor</mark>, such as one-time code, a push notification, or a security key.



### Audience & Needs

Protecting every desktop login with <abbr title="Multi-Factor Authentication">MFA</abbr> affects administrators and end users. 

<details>
    <summary>Administrator needs</summary>

    <ul>
        <li>deploy software that changes the login experience for every computer in their organization</li>
        <li>configure which end users are affected</li>
        <li>minimize end users being locked out of their work computers</li>
    </ul>

</details>

<details>
    <summary>End user needs</summary>

    <ul>
        <li>understand their computer login will change</li>
        <li>get enrolled in any new security measures for <abbr title="Multi-Factor Authentication">MFA</abbr></li>
        <li>use <abbr title="Multi-Factor Authentication">MFA</abbr> on every computer login</li>
        <li>still be able to login when their computer is offline</li>
    </ul>
</details>



### Skills Used

* <mark>prototyping</mark>
* <mark>visual design</mark>
* <mark>usability testing</mark>



### My Role on the Team

My team at Okta:

- Design: <mark>Lead Product Designer</mark> (me), a Product Designer, a User Researcher
- Engineering: a manager, 2 macOS, 3 Windows, 2 QA
- 2 Product Managers
- a Documentation Writer



## Design Process



### Competitive Research

We weren't the first to market with Desktop <abbr title="Multi-Factor Authentication">MFA</abbr>. But each competitor used a custom interface, rather than following Windows or macOS conventions. 

<img
  src="{{ site.url }}/assets/mfa/duo-win.png"
  alt="Duo Desktop MFA on Windows"
  class="screenshot screenshot-landscape"
/>

<img
  src="{{ site.url }}/assets/mfa/tecmfa-mac.png"
  alt="TecMFA on macOS"
  class="screenshot screenshot-landscape"
/>

I advocated for this opportunity to speak to one of Okta's strengths&mdash;vendor neutrality. <mark><span class="decision">DECISION</span>: follow the Windows and macOS interface conventions</mark>, because end users probably trust them more than any security product.



### TBD

TBD



## Retrospective

lessons learned — did you reach success metrics? Work through the right problem? What would you do better if you could do it again?



<a href="#" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2023)</a>

{% include footer_case_study.md %}
