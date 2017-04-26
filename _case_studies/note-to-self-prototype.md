---
layout: default
title: Note to Self Prototype
overview: In 4 weeks, create, test, and launch a prototype to help writers continue writing across sessions by preserving mental context at the end of each session.
date: 2017-03-31
---

# <small>Case Study</small>: <br />Note to Self Prototype

## Overview

In 4 weeks, create, test, and launch a prototype to help writers continue writing across sessions by preserving mental context at the end of each session.

## Problem Definition

### Pain Points

Coming back to a creative writing project requires remembering:

  - where you left off
  - what you planned to do next (exemplified by order, dates, or other priority)
  - what you wanted to do
  - what you want to do now

### Hypothesis

> TheRightMargin can bridge writing sessions to help writers retain context and continue writing via a "note to self" prototype.

### Design Goals

Within TheRightMargin's online writing product:

```
1. Preserves a user’s context so they can continue working by writing or planning.
2. Does not become annoying or disruptive with repeat use.
3. Does not force the user to do work they wouldn’t normally do.

    a. Supports writer's process  
    b. Are users coming to TheRightMargin and already doing the things we’re allowing?  
    c. Or are we changing their behavior in some way?  

        - One way to gather insight: existing timer use — are users new to timers?

4. Useful with one project, more useful with more projects.
5. Useful even if user doesn’t return for some time.
6. Increases retention (though hard to prototype)
7. Unique relative to other tools

    a. Definitely writing tools  
    b. Ideally productivity tools

8. Integrates smoothly with current product and feature set

    a. Ties back to vision of goal-driven writing  
    b. Ties back to smart writing tool

```

## Audience

I hypothesized the following traits of an ideal prototype tester:

1. Writer who leaves post it notes to himself or herself around their workspace.

    _Hypothesis: Our solution should appeal most to those who've already taken steps to solve the problem of retaining context by leaving notes to themselves, not writers who'd have to be trained on both the solution and the benefits of retaining context._

2. Writes regularly enough to need reminders
    a. One project that takes longer than a week or 
    b. Concurrent projects

    _Hypothesis: Infrequent writers don't lose context often enough to suffer from the problem our prototype would solve._

3. Already adopts Getting Things Done (GTD) mindset of writing everything down (i.e. capture phase of GTD)

    _This is an example behavior of item 1 with a corollary from productivity. GTD practices are a strong indicator of existing patterns we can tap into, though it may limit our audience if we only solved their problem._


## Team / Role

As Senior UX Engineer, I worked: 
* to define, test, and implement the prototype
* with our UX designer to recruit users and run prototype tests
* with our full-stack engineer to brainstorm technical feasibility of solutions
* with our Founder to approve design goals and deliverables

## Constraints

1. Move from concept to viable prototype collecting real data in 2 sprints (4 weeks).
2. Technical feasibility to create a solution not reliant on interruptive browser modals or prompts.
3. Recruiting testers. I worried about the time to recruit at least 5 testers based on it taking over two weeks in past prototypes for TheRightMargin.

# Design Process

## 1. Recruit Users

Recently, we began to offer users who wrote into support the ability to opt-in to a UX tester bank for future prototypes. We recruited 7 existing users of TheRightMargin from this UX tester bank within the first week. This was a speedy, welcome relief from casting a broad net to recruit any existing users out of the blue or appealing to local or online writing communities. Thus, we quickly overcame our last constraint.

## 2. Gather Supporting Data

> I strongly disagreed with our 3rd design goal: __"Does not force the user to do work they wouldn’t normally do."__ 

I felt we needed to successfully tap into existing behavior of writers leaving notes to their future selves, rather than encourage new behavior.

Our existing product had a corollary that I thought we could learn from—a writing timer. Timed writing exercises are not a new concept to our new product. __I hypothesized that only those who already used timers in their writing used our timer.__

I pulled metrics data on users active in the last month who had started or finished TheRightMargin's writing timer and emailed them:

```
Fellow wordsmith,

Art from TheRightMargin here. Thanks for using the timer on our writing tool! Would quickly love to know your impressions so we can improve: Have you used a timer before for your writing? Did our timer help you?

Thanks,
— Art
```

> The user responses were largely consistent with my hypothesis about leveraging existing behavior...

```
Yes, I'm always using a timer when I'm writing.

I  like  to  set  the  timer  at  52 minutes and then write. But I use Scrivener for that.
```

```
it does help, but I decided I preferred the “Pomodone” app, which I can link with Todoist, and which synchronizes with my calendar to show how much time I spent working on what.  However, timers for writing are generally very useful.  Have you seen the “mostdangerouswritingapp.com “?  Very scary, and depends on timers: )
```

```
I think there is no tool out there right now, which is tracking actual production "writing" and then giving a picture of the progress the writer is making from let's say typing 500 words in an hour to in 30 mins.
```

```
I've not used a timer for writing prior to this. As a new tool for me, I'm excited to discover it's performative potential. Perhaps it could be likened to "speed chess," in the sense that engagement in the thoughtful act is elevated to a stream of consciousness as a function of time.
```

```
Yes I have used the timer and it was the first time I wrote with a timer since high school. Personally, it helped me feel the pressure to write and have an incentive to get going. It added a simple element of challenge and helps me benchmark my progress. 
```

This initial data effectively eliminated the design goal of encouraging new behavior.

## 3. Design Initial Prototypes

We condensed 10 initial concepts to the following two prototypes.

### Prototype A: when leaving a project, ask users what they want to accomplish when they come back

**Prototype A Hypothesis**

> Asking the right question (i.e. about context) at the right time (i.e. when a user is done working), will help a user continue working next time.

__Failure indicators:__
1. Users find the question intrusive
2. Users don’t want to answer the question
3. Users don’t provide answers that help them in their next working session.

__Success indicators:__
1. Users provide answers that aren’t already in their timeline or top of mind.
2. Users answer “yes” to “Would you use this tactic in other writing tools / in the future?”

![Prototype A flow]({{ site.url }}/assets/note_to_self/prototype_a.jpg)

The only design goals **NOT** met by Prototype A were:
```
  2. Does not become annoying or disruptive with repeat use.
      a. Depends on how accurately we can capture user leaving and the UI...
  ...
  5. Useful even if user doesn’t return for some time.
      a. Hopefully, because the last thing you did will be the first thing you’ll see?
```

---

### Prototype B: when returning to a project, ask users if the next milestone is still what they want to work on 

**Prototype B Hypothesis**

> Asking the right question (i.e. about what’s next to do) at the right time (i.e. when a user comes back to work), will help a user start working.

**Failure indicators:**
1. Users find the question intrusive
2. Users answer “No” consistently

**Success indicators:**
1. Users answer “Yes” more often than “No”
2. Users add new milestones


![Prototype B flow]({{ site.url }}/assets/note_to_self/prototype_b.jpg)

The only design goals **NOT** met by Prototype B were:
```
  2. Does not become annoying or disruptive with repeat use.
      a. Depends on how frequency of prompt and efficacy after repeat exposure.
```

## 4. Prototype Testing

5 of the 7 recruited users were available for an hour-long prototype test via screen sharing. 

Rather than rely on static screens, which could not simulate writing, or taking a week (1/4 of our constrained time) to build the first prototype in our product, I tested a version of Prototypes A and B using the following script...

### Prototype Test Script

```
1. Prep / before interview
    a. Given that all recruits are TheRightMargin users, look up their project data to gauge type of writing they do. 
    b. Add user on Skype or Google Hangout
    c. Set up Google Doc for taking notes on user
    d. Set up new Google Doc prototype for user

2. During interview
    a. Q: What type of writing do you do?
    b. Q: A new project you’re itching to write?
    c. Q: Ask user about their current way of keeping context between writing sessions.
    d. Q: How exactly do you currently end your writing sessions?
    e. Share prototype with user, confirm they can edit it
    f. Open the prototype
      Backup writing prompt, in case no active projects: 
You've finally managed to discover the secret to immortality. Suddenly, Death appears before you, hands you a business card, and says, "When you realize living forever sucks, call this number, I've got a job offer for you." 
    g. First session gap
      i. SESSION 1: Do 3 minutes of freewriting
      ii. Refresh document
      iii. Close eyes to simulate passage of time OVER A WEEK
      iv. Open eyes to simulate passage of time
      v. SESSION 2: Do 3 minutes of freewriting
    h. Second session gap
      i. Ask question about next writing session 
          1. Ask either:
              a. Verbally
              b. On-screen somehow
          2. Capture answer either:
              a. Note taker transcribes user answer
              b. User writes down answer
      ii. Refresh document
      iii. Close eyes to simulate passage of time OVER ANOTHER WEEK
      iv. Move user answer to visible place where it’ll be tested
      v. Open eyes to simulate passage of time
      vi. SESSION 3: Do 3 minutes of writing

    How we gauge prototype success
    i. Compare your experience of writing between your sessions
      1. Ideally user reports session 3 being easier than 2 and attributes it to their answer before session 3
      2. Maybe ask explicitly: 
        a. were the last 2 sessions were different?
        b. did you notice anything different between sessions 2 and 3?
        c. did the answer you give between 2 and 3 help your next session?
    ii. When would you expect to be asked about your next writing session?
    iii. Where would you expect to see this asked in TheRightMargin?
    iv. Where would you expect to see your answer in TheRightMargin?
    v. Would you use this tactic in other writing tools / in the future?
    vi. Share our risks with prototype

3. After interview
    Thank you follow up email. Ask any clarifying questions. Say we’re open to any more feedback as it occurs. 
```

### Prototype Test Synthesis

>  How exactly do you currently end your writing sessions? e.g. close browser, save doc, close laptop? ***No consistency.***

1.  1 tester keeps writing open
2.  ***4 testers save and close writing***
3.  Additional data
    1.  [*Writers Helping
        Writers*](https://www.facebook.com/groups/mikegeffnerpresentswritershelpingwriters/permalink/10154633085286026/?ref=notif&notif_t=group_post_approved&notif_id=1489448381358202)
        — 2 open, 3 close, 1 both
    2.  [*WDNWC
        group*](https://www.facebook.com/groups/WDNWCAttendeeGroup/permalink/613603405505949/)
        — 2 close, 1 open
    3.  [*TheRightMargin
        page*](https://www.facebook.com/therightmargin/posts/648917121984710)
        — no responses
    4.  [*Twitter
        poll*](https://twitter.com/TheRightMargin/status/841428542118232065)
        — 1 close
    5.  Reddit:
        [*r/writing*](https://www.reddit.com/r/writing/comments/5z8mqg/when_youre_done_writing_do_you_keep_it_open_or/),
        r/KeepWriting/ — no responses
    6.  WriterHangout
        [*\#general*](https://writerhangout.slack.com/archives/general/p1489447897891913)
        — 1 open, 1 close, 1 both

> How do you currently help yourself between writing sessions? ***No consistency.***

1.  Morning pages, writing group, reading
2.  Archive research on Google Docs to read for later
3.  Morning exercise, playing piano between sessions
4.  Freewriting, fighting off impostor syndrome and inner critic with persistence
5.  Outlining, editorial calendar

> ***Every participant chose to answer*** the question at the end of the second session and pretty much ***worked according to their answers***:

1.  “Direction. So when I come back next time, I have more direction in my freewriting.”
2.  “I want to start there in the article when I get back”
3.  “when i come back i wanna first review - maybe ask myself some questions. Maybe add structure here and there. And work on these things.”
4.  “I'd like to finish editing this article when I return.”
5.  “Finish this and prepare it for submission”

> Comparing writing sessions ***was generally favorable to the prompt***:

1.  The first was the hardest. After the first one, you have a feeling of accomplishment. I held onto that feeling… Third [session] was easier than the second. Maybe because I put down the goal of having more direction.
2.  If there was a way to pin a place where this was last, so i don't have to go back through… i didn't have to go back from the top, i knew exactly where i was starting, i could go from there with confidence.
3.  I like those kinds of prompts. That’s one of things that attracted me to TheRightMargin. The big trick is coming up with questions that are appropriate. … Questions are like loops they help you get into something.
4.  The third time was a little quicker because of the note. Each time was not that hard - but third time gave his mind objective.
5.  Would be good to see the prompt - and also would be good to see the last few edits she made. She jumps around a lot so it would be helpful to see what she last did. … But always a good thing to ask

> When should TheRightMargin ask? ***No consistency***

1.  A little ***later*** in the process.
2.  Somewhere ***in between*** writing sessions.
3.  Maybe ***at the end*** of a writing session?
4.  Probably ***at the end of the doc***
5.  Very useful ***at the beginning***. New chapter/new
    project/new section.
6.  It depends when the best time is ...sometimes it’s ***in the middle*** of writing
7.  ***Anytime you leave*** the writing session

> Where is the answer most helpful? ***In the content***. *Biased by Google Doc prototype?*

1.  Personalized email … when you log in or come back to set the tone for the session
2.  ***at the end of the doc***
3.  Maybe present as a box that floats over - or becomes an integral part of TheRightMargin - creative comments - or thought starters - maybe create a box where i can create “THOUGHT PROVOKING QUESTIONS” where i can add them and maybe you could also and they would be color coded.
4.  I would like to see it ***in the actual content*** where I left last.
5.  Would be similar to what Art did - she’d leave ***in line in the text***. … And then maybe making that a task at the top of the task list.

> Would you use this tactic in other writing tools / in the future? ***Consistently yes.***

1.  Yes, definitely. ... Wants to set more intentions for writing.
2.  it's a new thing, but it has a lot of potential to give you prompts to move to the next step. but i think there is probably something that's already in TheRightMargin that's supposed to prompt you to the next deadline rather than to the next activity?
3.  What you would do for me is integrate this in the document
4.  Has not written that much before. The whole thing started with TheRightMargin. To break down tasks. It’s what he’s always wanted.
5.  Yea can see it being useful in the future. Anytime you can know what you want o accomplish when you sit down at the paper and know what you want to do it’s useful.


> The qualitative prototype results were very encouraging after only 2 weeks of design and no engineering time. ***The biggest remaining risk was implementation given the lack of consistency in when to ask the question.***


## 5. Revise Design Goals

Based upon what we learned thus far, we revised our design goals. As we learned from timer users, appealing to new behavior was not a good place to start. Uniqueness was virtually guaranteed based on prototype responses and no longer worth emphasizing.

```
1. Make returning to a writing project a seamless, more delightful experience that helps you retain your context (reduce cognitive load)

    a. Help users easily discover the answer upon return to be immediately useful/actionable

2. Make sure it’s delightful/useful for the 1st time as well as the 100th time (no annoying UX!)

    a. Opt out or design a way that you don’t need to

3. The solution should tie back to your writing goals (milestones and tasks in TheRightMargin)

    a. How does this tie back/step forward towards our vision for creating a smarter writing app?

4. Make it discoverable easily upon entering and accessible whenever you want it
5. Do not create an experience that involves exit interruptions
6. This experience should be most useful for projects that you don’t write everyday or longer-form projects
```

## 6. Build Initial Production Version

The biggest remaining problem from the initial prototype testing was when to present the note to self or context-preserving question. I quickly began to enumerate TheRightMargin workspace UI and settled on a bottom right placement that wouldn't distract from ongoing writing or conflict with potential commenting features. Here's my thought process on paper:

![Where should we ask the question?]({{ site.url }}/assets/note_to_self/build_placement.jpg)

Then, I fleshed out the entry points and initial flows of this UI. The founder and I quickly scoped these down (i.e. the red ink) for a first version to build:

![Note to self entry points]({{ site.url }}/assets/note_to_self/build_ui.jpg)

I defined more precise states and flows:

![Note to self states and flows]({{ site.url }}/assets/note_to_self/build_leave_flows.jpg)

And even sketched Prototype B, which unfortunately wasn't implemented due to time constraints: 

![Prototype B implementation sketch]({{ site.url }}/assets/note_to_self/build_return_flows.jpg)

---

Here's what made it into production on [TheRightMargin in March 2017](https://www.therightmargin.com/?ref=avkux). 

The main affordance uses the language of **"Done working for now?"** to support both notes that relate directly to writing and other non-writing work (planning, brainstorming, research, outlining, etc.) that TheRightMargin currently supports.

The UI _subtly_ draws attention to itself by pulsating the affordance at the bottom 30 minutes into a writing session:

![Production build v1]({{ site.url }}/assets/note_to_self/production_pulse.gif)

The feature can also be manually triggered at any other time, in case 30 minutes doesn't work for the current writing session...

![Production build v1]({{ site.url }}/assets/note_to_self/production_v1.gif)

It provides basic error checking for task length and it saves the notes to self in the most visible place for next time (the top of the current milestone).

I instrumented the following metrics to measure the success of the first production version:

1. a new `Opened Note to Self` event when clicking the affordance with a `content` property for comparing future CTA copy iterations.
2. a new `task_count` property on the existing `Added Task` event: how many tasks were added simultaneously (blank in normal flow, 1+ in Note to Self flow)

## Retrospective

We hit our goals within our constraints, but it's too early to gauge success without collecting more production metrics and user feedback over a longer period of time. 

The prototype tests were successful in discovering viable solutions to the pain of continuing to write across sessions. Implementation proved to be the biggest challenge as we had to pick a version we can build within the remaining time, rather than the ideal one. The 30 minute interval and general entry point to the UI still feel like untested hypotheses. Usability testing or even screen captures of longer sessions could begin to illuminate their effectiveness in the product. 

Production feels incomplete without the Prototype B implementation to close the loop on how to rebuild context by drawing attention to the note(s) to self from the previous session, after a reasonable interval of time. 
