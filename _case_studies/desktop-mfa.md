---
layout: default
title: Protecting Every Login to macOS &amp; Windows
overview: Generated <mark>$1mm ARR</mark> in first 7 weeks by protecting users on every login to their Mac or PC.
skills: prototyping, visual design, usability testing
date: 2023-10-05
cover_image: /assets/mfa/macOS-FS-factors.png
active: true
---

<img
  src="{{ site.url }}/assets/mfa/macOS-FS-factors.png"
  alt="Work sample from this case study"
  class="screenshot screenshot-landscape"
/>

# <small>Case Study:</small> <br />{{ page.title }}

<a href="https://www.okta.com/products/device-access/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2023)</a>



* [Overview](#1)
  * [Problem](#1.1)
  * [Audience & Needs](#1.2)
  * [Skills](#1.3)
  * [Team](#1.4)

* [Design Process](#2)
  * [Competitive Research](#2.1)
  * [Constraints](#2.2)
  * [Prototyping](#2.3)
  * [Usability testing](#2.4)

* [Outcomes](#3)



<a name="1"></a>
## Overview



<a name="1.1"></a>
### Problem

<img
  src="{{ site.url }}/assets/mfa/macOS-pw-login.png"
  alt="Password prompt on macOS 12"
  class="screenshot screenshot-landscape"
/>

Passwords are no longer enough to protect employees logging into their work Mac or PC. These sensitive computers now require Multi-Factor Authentication (MFA) to comply with cybersecurity insurance requirements or follow the [Executive Order on Improving the Nation’s Cybersecurity](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/). Computer logins now <mark>require a password and a separate factor</mark>, such as one-time code, a push notification, or a security key.



<a name="1.2"></a>
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



<a name="1.3"></a>
### Skills

* <mark>prototyping</mark>
* <mark>visual design</mark>
* <mark>usability testing</mark>



<a name="1.4"></a>
### Team

My team at Okta:

- Design: <mark>Lead Product Designer</mark> (me), a Product Designer, a User Researcher
- Engineering: a manager, 2 macOS, 3 Windows, 2 QA
- 2 Product Managers
- a Documentation Writer



<a name="2"></a>
## Design Process



<a name="2.1"></a>
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



<a name="2.2"></a>
### Constraints

Following the Windows and macOS interface conventions came with heavy constraints. On Windows login, we were limited to [strictly 10 basic UI elements](https://learn.microsoft.com/en-us/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_type) and <mark>couldn't even include images or customize the login font in any way</mark>.

On macOS login, we could use the UI elements of any macOS app, but had to either cover up the username &amp; password fields or emulate the entire login window, down to the colorful background image that varies with each release.



<a name="2.3"></a>
### Prototyping for feasibility

I prototyped early in low fidelity to clarify what was possible and needed from our solution.

<mark>My prototypes mixed UI with authentication logic</mark>; both were fully clickable. Interactive logic was crucial since my prototype shared and informed the code engineers would eventually build. I presented these prototypes to the team on a weekly basis to confirm feasibility, eliminate unnecessary states, and ensure I delivered UI for every critical path.

Extensive prototyping allowed us to <mark>simulate and test a complete user experience before we committed to code</mark>.

<img
  src="{{ site.url }}/assets/mfa/macOS-logic-frame.png"
  alt="screenshot of logic frame"
  class="screenshot screenshot-landscape zoomable"
/>

<img
  src="{{ site.url }}/assets/mfa/macOS-logic-with-UI.jpg"
  alt="screenshot of logic frame next to UI frame with prototype connections visible"
  class="screenshot screenshot-landscape zoomable"
/>

<img
  src="{{ site.url }}/assets/mfa/macOS-prototype.jpg"
  alt="screenshot of zoomed out prototype with all connections visible"
  class="screenshot screenshot-landscape zoomable"
/>



<a name="2.4"></a>
### Usability testing improved enrollment

Usability testing my Windows prototype with representative users found a key challenge. End users had 50 logins to enroll in additional security after being logged in. Not only did users defer enrollment until the count was low, they expected to enroll when the count reached 0. <mark><span class="decision">Decision</span>: meet end user expectations to minimize error states and troubleshooting costs.</mark>

macOS engineers revisited the feasibility of starting with enrollment during login.  I found inspiration in the macOS Setup interface, which also appears before users are logged in. 

<img
  src="{{ site.url }}/assets/mfa/macOS-setup.png"
  alt="screenshot of macOS setup screen before login"
  class="screenshot screenshot-landscape zoomable"
/>

This became how we introduced ourselves and enrolled users:

<img
  src="{{ site.url }}/assets/mfa/macOS-enrollment.png"
  alt="screenshot of custom macOS enrollment screen before login"
  class="screenshot screenshot-landscape zoomable"
/>

Usability testing my macOS prototype eliminated all the enrollment friction we found with the original Windows approach. This approach also simplified the code and implementation logic, making it easier to QA and document.



<a name="3"></a>
## Outcomes &amp; Market Feedback

Following the Windows and macOS interface conventions led to interfaces that felt fully integrated into the existing, familiar, trusted login experience. In beta testing, administrators shared comments like <mark>"it looks like you partenered with Microsoft [or Apple],"</mark> even when we weren't soliciting UI feedback.

<img
  src="{{ site.url }}/assets/mfa/macOS-FS-factors.png"
  alt="screenshot of custom macOS Desktop MFA factors"
  class="screenshot screenshot-landscape zoomable"
/>

<img
  src="{{ site.url }}/assets/mfa/macOS-FS-offline.png"
  alt="screenshot of custom macOS device access code input"
  class="screenshot screenshot-landscape zoomable"
/>

<mark>We generated $1mm <abbr title="Annual Recurring Revenue">ARR</abbr> in the first 7 weeks</mark> after the product announcement in Washington, D.C.

<img
  src="{{ site.url }}/assets/mfa/on-stage.jpg"
  alt="Desktop MFA shown off on stage at Okta City Tour DC"
  class="screenshot screenshot-landscape zoomable"
/>



<a href="https://www.okta.com/products/device-access/" type="button" class="btn btn-success" target="_blank">&#10004; In Production (2023)</a>

{% include footer_case_study.md %}
