---
layout: default
title: Flows Aren't Just for Designers
overview: Introduced user flows to improve an overlooked and under-tested sign up experience on a major consumer web property—vevo.com.
skills: user flows, product metrics
date: 2014-10-12
cover_image: /assets/vevo_flows/cover.png
---

![Work sample from this case study]({{ site.url }}/assets/vevo_flows/cover.png)

# <small>Case Study:</small> <br />Flows Aren't Just for Designers

> This was the inaugural post to kick off the [Vevo Engineering Blog](https://web.archive.org/web/20161205044129/http://blog.vevo.com/flows-arent-just-for-designers/)

## Overview

Introduced user flows to improve an overlooked and under-tested sign up experience on a major consumer web property&mdash;vevo.com.

## Skills Used

* user flows
* product metrics

# Design Process (Blog Post)

As a front-end or full-stack developer, what’s the first thing you do when you start on a new feature? Do you read the user story and dive in, cowboy-style? Do you search Google, StackOverflow, or GitHub to see if someone else has implemented it? Do you run git blame to find who worked on a related piece of code?

I start with user flows. A flow is essentially a series of steps a user can perform in your app. Flows involve what users see, what actions they take, what errors they trigger, and all the places a user can end up. [37signals has an elegant post I tend to revisit](https://signalvnoise.com/posts/1926-a-shorthand-for-designing-ui-flows).

But you’re a dev! Why start with flows? Shouldn’t a designer, a product manager, or someone dedicated to user experience take care of this? Possibly, but even if they have, that doesn’t absolve you of the responsibility of a solid implementation. A visual designer may not be aware of all the possible error states triggered by your app. A UX designer may not know what data is available at every step. A PM may not know that necessary API calls don’t exist. A data researcher may run reports based on assumptions about where metrics calls occur. If no one breaks down the flows, you end up shipping something incomplete. And until a feature flow is documented and shared, everyone has a different flow in their head. As a dev, you’re the last line of defense against a half-baked product.

> If no one breaks down the flows, you end up shipping something incomplete.

Vevo presented a great opportunity to show flows in action when we added Google+ as a sign up option last year. The spec was:

<pre><code>+ mimic our existing social login with Facebook
+ require a Vevo account (linked to a Google+ account)
+ add the functionality to vevo.com, iOS app, and Android app
+ implement thorough instrumentation to gauge success</code></pre>

Sound straightforward? Here’s the flow I ended up building in OmniGraffle, based on our existing Facebook implementation (GP is Google+):

<a href="{{ site.url }}/assets/vevo_flows/flows_init.png" target="_blank">
![Initial social flows for Vevo]({{ site.url }}/assets/vevo_flows/flows_init.png)
</a>

Doesn’t look so simple anymore! Note that some paths leave you hanging with dangling arrows. That means we have things that haven’t been implemented and probably need to be reconsidered for the Facebook implementation. These are points where we could leave users stranded. Let’s add those TODOs in orange:

<a href="{{ site.url }}/assets/vevo_flows/flows_todo.png" target="_blank">
![Vevo flows with todos]({{ site.url }}/assets/vevo_flows/flows_todo.png)
</a>

That’s better but wouldn’t it be better with clear areas of responsibility?

<a href="{{ site.url }}/assets/vevo_flows/flows_resp.png" target="_blank">
![Vevo social flows with areas of responsibility]({{ site.url }}/assets/vevo_flows/flows_resp.png)
</a>

Great, the large boxes help me separate the functionality into modules and expose opportunities for unit testing and code reuse. Now there’s only the instrumentation spec from my data researcher&hellip;

<a href="{{ site.url }}/assets/vevo_flows/flows_metrics.png" target="_blank">
![Vevo social flows with metrics events]({{ site.url }}/assets/vevo_flows/flows_metrics.png)
</a>

The purple labels correspond to metrics calls we plan to send to comScore (cS). Note how few there are, so we most likely need to define more for data and funnel accuracy.

All these iterations were captured in different layers in my OmniGraffle document so I can focus on whatever I need to and hide the rest:

![OmniGraffle layers]({{ site.url }}/assets/vevo_flows/graffle_layers.png)

# Retrospective

This document was how I justified my time estimate to my product and engineering managers. It provided a basis for iOS and Android developers to follow (or push back on) my decisions for a consistent implementation. It helped QA test the delivered functionality. Finally, it helped us discuss what metrics we were recording and what they actually meant by mapping them to the best place in the flow.

> This experience went live on [vevo.com](http://www.vevo.com/?ref=avkux) in Oct 2014. iOS and Android implementations followed.

Obviously, flow documents take time to create but the exercise is worth doing. Start on a whiteboard. Jump to something digital like OmniGraffle when necessary. Realize that when the diagram feels too big, that’s precisely the value of the exercise. Don’t be afraid to break things down, question your assumptions, and pare down to the essentials of what your changes need to accomplish. You’ll still make all these decisions in code so I find it incredibly helpful to brainstorm them up front and start asking questions early.

> This was the inaugural post to kick off the [Vevo Engineering Blog](https://web.archive.org/web/20161205044129/http://blog.vevo.com/flows-arent-just-for-designers/)

{% include footer_case_study.md %}
