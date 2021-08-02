---
layout: default
title: Note to Self—From Research to Launch
overview: In 4 weeks, designed, tested, and launched a unique feature to successfully help writers continue writing across multiple creative sessions.
skills: user research, user flows, wireframing, prototyping
date: 2017-03-31
cover_image: /assets/note_to_self/production_v1.gif
---

![Work sample from this case study]({{ site.url }}/assets/note_to_self/production_v1.gif)

# <small>Case Study:</small> <br />Note to Self—From Research to Launch

<a href="https://www.therightmargin.com/?ref=avkux" type="button" class="btn btn-success" target="_blank">&#10004; In Production</a>

## Overview

In 4 weeks, designed, tested, and launched a unique feature to successfully help writers continue writing across multiple creative sessions.

## Skills Used

* user research
* user flows
* wireframing
* prototyping

## Problem Definition

### Pain Points

<details>
  <p>Coming back to a creative writing project requires remembering:</p>

  <ul>
    <li>where you left off</li>
    <li>what you planned to do next (exemplified by order, dates, or other priority)</li>
    <li>what you wanted to do</li>
    <li>what you want to do now</li>
  </ul>
</details>

### Hypothesis

<details>
  <blockquote>
    <p>
      TheRightMargin can bridge writing sessions to help writers retain context and continue writing via a &quot;note to self&quot; prototype.
    </p>
  </blockquote>
</details>

### Design Goals

<details>

  <p>
    Within TheRightMargin's online writing product:
  </p>

  <pre><code>
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
  </code></pre>

</details>

## Audience

<details>

  <p>
    I hypothesized the following traits of an ideal prototype tester:
  </p>

  <ol>

    <li>
      <p>
        Writer who leaves post it notes to himself or herself around their workspace.
      </p>
      <p>
        <em>Hypothesis: Our solution should appeal most to those who&#39;ve already taken steps to solve the problem of retaining context by leaving notes to themselves, not writers who&#39;d have to be trained on both the solution and the benefits of retaining context.</em>
      </p>
    </li>

    <li>
      <p>
        Writes regularly enough to need reminders
        <strong>
          a. One project that takes longer than a week
        </strong>
        or
        <strong>
          b. Concurrent projects
        </strong>
      </p>
      <p>
        <em>Hypothesis: Infrequent writers don&#39;t lose context often enough to suffer from the problem our prototype would solve.</em>
      </p>
    </li>

    <li>
      <p>
        Already adopts Getting Things Done (GTD) mindset of writing everything down (i.e. capture phase of GTD)
      </p>
      <p>
        <em>This is an example behavior of item 1 with a corollary from productivity. GTD practices are a strong indicator of existing patterns we can tap into, though it may limit our audience if we only solved their problem.</em>
      </p>
    </li>

  </ol>

</details>

## My Role on the Team

<details>

  <p>
    As Senior UX Designer &amp; Engineer, I worked:
  </p>

  <ul>
    <li>
      to define, test, and implement the prototype
    </li>
    <li>
      with our UX designer to recruit users and run prototype tests
    </li>
    <li>
      with our full-stack engineer to brainstorm technical feasibility of solutions
    </li>
    <li>
      with our Founder to approve design goals and deliverables
    </li>
  </ul>

</details>

## Constraints

<details>

  <ol>
    <li>
      Move from concept to viable prototype collecting real data in 2 sprints (4 weeks).
    </li>
    <li>
      Technical feasibility to create a solution not reliant on interruptive browser modals or prompts.
    </li>
    <li>
      Recruiting testers. I worried about the time to recruit at least 5 testers based on it taking over two weeks in past prototypes for TheRightMargin.
    </li>
  </ol>

</details>

# Design Process

## 1. Recruit Users

<details>
  <p>
    Recently, we began to offer users who wrote into support the ability to opt-in to a UX tester bank for future prototypes. We recruited 7 existing users of TheRightMargin from this UX tester bank within the first week. This was a speedy, welcome relief from casting a broad net to recruit any existing users out of the blue or appealing to local or online writing communities. Thus, we quickly overcame our last constraint.
  </p>
</details>

## 2. Gather Supporting Data

<details>

  <blockquote>
    <p>
      I strongly disagreed with our 3rd design goal:
      <q>Does not force the user to do work they wouldn’t normally do.</q>
    </p>
  </blockquote>

  <p>
    I felt we needed to successfully tap into existing behavior of writers leaving notes to their future selves, rather than encourage new behavior.
  </p>

  <p>
    Our existing product had a corollary that I thought we could learn from—a writing timer. Timed writing exercises are not a new concept to our new product. <strong>I hypothesized that only those who already used timers in their writing used our timer.</strong>
  </p>

  <p>
    I pulled metrics data on users active in the last month who had started or finished TheRightMargin&#39;s writing timer and emailed them:
  </p>

  <pre><code>
Fellow wordsmith,

Art from TheRightMargin here. Thanks for using the timer on our writing tool! Would quickly love to know your impressions so we can improve: Have you used a timer before for your writing? Did our timer help you?

Thanks,
— Art
  </code></pre>

  <p>
    The user responses were largely consistent with my hypothesis about leveraging existing behavior&hellip;
  </p>

  <pre><code>
Yes, I'm always using a timer when I'm writing.

I  like  to  set  the  timer  at  52 minutes and then write. But I use Scrivener for that.
  </code></pre>

  <pre><code>
it does help, but I decided I preferred the “Pomodone” app, which I can link with Todoist, and which synchronizes with my calendar to show how much time I spent working on what.  However, timers for writing are generally very useful.  Have you seen the “mostdangerouswritingapp.com “?  Very scary, and depends on timers: )
  </code></pre>

  <pre><code>
I think there is no tool out there right now, which is tracking actual production "writing" and then giving a picture of the progress the writer is making from let's say typing 500 words in an hour to in 30 mins.
  </code></pre>

  <pre><code>
I've not used a timer for writing prior to this. As a new tool for me, I'm excited to discover it's performative potential. Perhaps it could be likened to "speed chess," in the sense that engagement in the thoughtful act is elevated to a stream of consciousness as a function of time.
  </code></pre>

  <pre><code>
Yes I have used the timer and it was the first time I wrote with a timer since high school. Personally, it helped me feel the pressure to write and have an incentive to get going. It added a simple element of challenge and helps me benchmark my progress.
  </code></pre>

  <p>
    This initial data effectively eliminated the design goal of encouraging new behavior.
  </p>

</details>

## 3. Design Initial Prototypes

We condensed 10 initial concepts to the following two prototypes.

### Prototype A: when leaving a project, ask users what they want to accomplish when they come back

<details>

  <p>
    <strong>Prototype A Hypothesis</strong>
  </p>

  <blockquote>
    <p>
      Asking the right question (i.e. about context) at the right time (i.e. when a user is done working), will help a user continue working next time.
    </p>
  </blockquote>

  <p>
    <strong>Failure indicators:</strong>
  </p>

  <ol>
    <li>Users find the question intrusive</li>
    <li>Users don’t want to answer the question</li>
    <li>Users don’t provide answers that help them in their next working session.</li>
  </ol>

  <p>
    <strong>Success indicators:</strong>
  </p>

  <ol>
    <li>
      Users provide answers that aren’t already in their timeline or top of mind.
    </li>
    <li>
      Users answer “yes” to “Would you use this tactic in other writing tools / in the future?”
    </li>
  </ol>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/prototype_a.jpg" alt="Prototype A flow">
  </p>

  <p>
    The only design goals <strong>NOT</strong> met by Prototype A were:
  </p>

  <pre><code>
2. Does not become annoying or disruptive with repeat use.
    a. Depends on how accurately we can capture user leaving and the UI...
...
5. Useful even if user doesn’t return for some time.
    a. Hopefully, because the last thing you did will be the first thing you’ll see?
  </code></pre>

</details>

### Prototype B: when returning to a project, ask users if the next milestone is still what they want to work on

<details>

  <p>
    <strong>Prototype B Hypothesis</strong>
  </p>

  <blockquote>
    <p>
      Asking the right question (i.e. about what’s next to do) at the right time (i.e. when a user comes back to work), will help a user start working.
    </p>
  </blockquote>

  <p>
    <strong>Failure indicators:</strong>
  </p>

  <ol>
    <li>Users find the question intrusive</li>
    <li>Users answer “No” consistently</li>
  </ol>

  <p>
    <strong>Success indicators:</strong>
  </p>

  <ol>
    <li>Users answer “Yes” more often than “No”</li>
    <li>Users add new milestones</li>
  </ol>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/prototype_b.jpg" alt="Prototype B flow">
  </p>

  <p>
    The only design goals <strong>NOT</strong> met by Prototype B were:
  </p>

  <pre><code>
2. Does not become annoying or disruptive with repeat use.
    a. Depends on how frequency of prompt and efficacy after repeat exposure.
  </code></pre>

</details>


## 4. Prototype Testing

5 of the 7 recruited users were available for an hour-long prototype test via screen sharing.

Rather than rely on static screens, which could not simulate writing, or taking a week (1/4 of our constrained time) to build the first prototype in our product, I tested a version of Prototypes A and B using the following script&hellip;

### Prototype Test Script

<details>

  <pre><code>
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
  </code></pre>

</details>

### Prototype Test Synthesis

<details>

  <blockquote>
    <p>
      How exactly do you currently end your writing sessions? e.g. close browser, save doc, close laptop?
      <strong><em>No consistency.</em></strong>
    </p>
  </blockquote>

  <ol>

    <li>
      1 tester keeps writing open
    </li>

    <li>
      <strong><em>4 testers save and close writing</em></strong>
    </li>

    <li>
      Additional data

      <ol>

        <li>
          <a href="https://www.facebook.com/groups/mikegeffnerpresentswritershelpingwriters/permalink/10154633085286026/?ref=notif&amp;notif_t=group_post_approved&amp;notif_id=1489448381358202">
            <em>Writers Helping Writers</em>
          </a>
          — 2 open, 3 close, 1 both
        </li>

        <li>
          <a href="https://www.facebook.com/groups/WDNWCAttendeeGroup/permalink/613603405505949/">
            <em>WDNWC group</em>
          </a>
          — 2 close, 1 open
        </li>

        <li>
          <a href="https://www.facebook.com/therightmargin/posts/648917121984710">
            <em>TheRightMargin Facebook page</em>
          </a>
          — no responses
        </li>

        <li>
          <a href="https://twitter.com/TheRightMargin/status/841428542118232065">
            <em>Twitter poll</em>
          </a>
          — 1 close
        </li>

        <li>
          Reddit:
          <a href="https://www.reddit.com/r/writing/comments/5z8mqg/when_youre_done_writing_do_you_keep_it_open_or/">
            <em>r/writing</em>
          </a>,
          r/KeepWriting/ — no responses
        </li>

        <li>WriterHangout
          <a href="https://writerhangout.slack.com/archives/general/p1489447897891913">
            <em>#general channel</em>
          </a>
          — 1 open, 1 close, 1 both
        </li>

      </ol>

    </li>

  </ol>

  <blockquote>
    <p>
      How do you currently help yourself between writing sessions? <strong><em>No consistency.</em></strong>
    </p>
  </blockquote>

  <ol>

    <li>
      Morning pages, writing group, reading
    </li>

    <li>
      Archive research on Google Docs to read for later
    </li>

    <li>
      Morning exercise, playing piano between sessions
    </li>

    <li>
      Freewriting, fighting off impostor syndrome and inner critic with persistence
    </li>

    <li>
      Outlining, editorial calendar
    </li>

  </ol>

  <blockquote>
    <p>
      <strong><em>Every participant chose to answer</em></strong> the question at the end of the second session and pretty much <strong><em>worked according to their answers</em></strong>:
    </p>
  </blockquote>

  <ol>

    <li>
      “Direction. So when I come back next time, I have more direction in my freewriting.”
    </li>

    <li>
      “I want to start there in the article when I get back”
    </li>

    <li>
      “when i come back i wanna first review - maybe ask myself some questions. Maybe add structure here and there. And work on these things.”
    </li>

    <li>
      “I'd like to finish editing this article when I return.”
    </li>

    <li>
      “Finish this and prepare it for submission”
    </li>

  </ol>

  <blockquote>
    <p>
      Comparing writing sessions <strong><em>was generally favorable to the prompt</em></strong>:
    </p>
  </blockquote>

  <ol>

    <li>
      The first was the hardest. After the first one, you have a feeling of accomplishment. I held onto that feeling… Third [session] was easier than the second. Maybe because I put down the goal of having more direction.
    </li>

    <li>
      If there was a way to pin a place where this was last, so i don&#39;t have to go back through… i didn&#39;t have to go back from the top, i knew exactly where i was starting, i could go from there with confidence.
    </li>

    <li>
      I like those kinds of prompts. That’s one of things that attracted me to TheRightMargin. The big trick is coming up with questions that are appropriate. … Questions are like loops they help you get into something.
    </li>

    <li>
      The third time was a little quicker because of the note. Each time was not that hard - but third time gave his mind objective.
    </li>

    <li>
      Would be good to see the prompt - and also would be good to see the last few edits she made. She jumps around a lot so it would be helpful to see what she last did. … But always a good thing to ask
    </li>

  </ol>

  <blockquote>
    <p>
      When should TheRightMargin ask?
      <strong><em>No consistency</em></strong>
    </p>
  </blockquote>

  <ol>

    <li>
      A little <strong><em>later</em></strong> in the process.
    </li>

    <li>
      Somewhere <strong><em>in between</em></strong> writing sessions.
    </li>

    <li>
      Maybe <strong><em>at the end</em></strong> of a writing session?
    </li>

    <li>
      Probably <strong><em>at the end of the doc</em></strong>
    </li>

    <li>
      Very useful <strong><em>at the beginning</em></strong>. New chapte
      r/new project/new section.
    </li>

    <li>
      It depends when the best time is &hellip;sometimes it’s <strong><em>in the middle</em></strong> of writing
    </li>

    <li>
      <strong><em>Anytime you leave</em></strong> the writing session
    </li>

  </ol>

  <blockquote>
    <p>
      Where is the answer most helpful? <strong><em>In the content</em></strong>. <em>Biased by Google Doc prototype?</em>
    </p>
  </blockquote>

  <ol>

    <li>
      Personalized email … when you log in or come back to set the tone for the session
    </li>

    <li>
      <strong><em>at the end of the doc</em></strong>
    </li>

    <li>
      Maybe present as a box that floats over - or becomes an integral part of TheRightMargin - creative comments - or thought starters - maybe create a box where i can create “THOUGHT PROVOKING QUESTIONS” where i can add them and maybe you could also and they would be color coded.
    </li>

    <li>
      I would like to see it <strong><em>in the actual content</em></strong> where I left last.
    </li>

    <li>
      Would be similar to what Art did - she’d leave <strong><em>in line in the text</em></strong>. … And then maybe making that a task at the top of the task list.
    </li>

  </ol>

  <blockquote>
    <p>
      Would you use this tactic in other writing tools / in the future?
      <strong><em>Consistently yes.</em></strong>
    </p>
  </blockquote>

  <ol>

    <li>
      Yes, definitely. &hellip; Wants to set more intentions for writing.
    </li>

    <li>
      it&#39;s a new thing, but it has a lot of potential to give you prompts to move to the next step. but i think there is probably something that&#39;s already in TheRightMargin that&#39;s supposed to prompt you to the next deadline rather than to the next activity?
    </li>

    <li>
      What you would do for me is integrate this in the document
    </li>

    <li>
      Has not written that much before. The whole thing started with TheRightMargin. To break down tasks. It’s what he’s always wanted.
    </li>

    <li>
      Yea can see it being useful in the future. Anytime you can know what you want o accomplish when you sit down at the paper and know what you want to do it’s useful.
    </li>

  </ol>

  <blockquote>
    <p>
      The qualitative prototype results were very encouraging after only 2 weeks of design and no engineering time. <strong><em>The biggest remaining risk was implementation given the lack of consistency in when to ask the question.</em></strong>
    </p>
  </blockquote>

</details>

## 5. Revise Design Goals

<details>

  <p>
    Based upon what we learned thus far, we revised our design goals. As we learned from timer users, appealing to new behavior was not a good place to start. Uniqueness was virtually guaranteed based on prototype responses and no longer worth emphasizing.
  </p>

  <pre><code>
1. Make returning to a writing project a seamless, more delightful experience that helps you retain your context (reduce cognitive load)

    a. Help users easily discover the answer upon return to be immediately useful/actionable

2. Make sure it’s delightful/useful for the 1st time as well as the 100th time (no annoying UX!)

    a. Opt out or design a way that you don’t need to

3. The solution should tie back to your writing goals (milestones and tasks in TheRightMargin)

    a. How does this tie back/step forward towards our vision for creating a smarter writing app?

4. Make it discoverable easily upon entering and accessible whenever you want it
5. Do not create an experience that involves exit interruptions
6. This experience should be most useful for projects that you don’t write everyday or longer-form projects
  </code></pre>

</details>

## 6. Build Initial Production Version

<details>

  <p>
    The biggest remaining problem from the initial prototype testing was when to present the note to self or context-preserving question. I quickly began to enumerate TheRightMargin workspace UI and settled on a bottom right placement that wouldn&#39;t distract from ongoing writing or conflict with potential commenting features. Here&#39;s my thought process on paper:
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/build_placement.jpg" alt="Where should we ask the question?">
  </p>

  <p>
    Then, I fleshed out the entry points and initial flows of this UI. The founder and I quickly scoped these down (i.e. the red ink) for a first version to build:
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/build_ui.jpg" alt="Note to self entry points">
  </p>

  <p>
    I defined more precise states and flows:
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/build_leave_flows.jpg" alt="Note to self states and flows">
  </p>

  <p>
    And even sketched Prototype B, which unfortunately wasn&#39;t implemented due to time constraints:
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/build_return_flows.jpg" alt="Prototype B implementation sketch">
  </p>

  <p>
    Here&#39;s what made it into production on <a href="https://www.therightmargin.com/?ref=avkux">TheRightMargin in March 2017</a>.
  </p>

  <p>
    The main affordance uses the language of <strong>&quot;Done working for now?&quot;</strong> to support both notes that relate directly to writing and other non-writing work (planning, brainstorming, research, outlining, etc.) that TheRightMargin currently supports.
  </p>

  <p>
    The UI <em>subtly</em> draws attention to itself by pulsating the affordance at the bottom 30 minutes into a writing session:
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/production_pulse.gif" alt="Production build v1">
  </p>

  <p>
    The feature can also be manually triggered at any other time, in case 30 minutes doesn&#39;t work for the current writing session&hellip;
  </p>

  <p>
    <img src="{{ site.url }}/assets/note_to_self/production_v1.gif" alt="Production build v1">
  </p>

  <p>
    It provides basic error checking for task length and it saves the notes to self in the most visible place for next time (the top of the current milestone).
  </p>

  <p>
    I instrumented the following metrics to measure the success of the first production version:
  </p>

  <ol>

    <li>
      a new <code>Opened Note to Self</code> event when clicking the affordance with a <code>content</code> property for comparing future CTA copy iterations.
    </li>

    <li>
      a new <code>task_count</code> property on the existing <code>Added Task</code> event: how many tasks were added simultaneously (blank in normal flow, 1+ in Note to Self flow)
    </li>

  </ol>

</details>

## Retrospective

<details>

  <p>
    We hit our goals within our constraints, but it's too early to gauge success without collecting more production metrics and user feedback over a longer period of time.
  </p>

  <p>
    The prototype tests were successful in discovering viable solutions to the pain of continuing to write across sessions. Implementation proved to be the biggest challenge as we had to pick a version we can build within the remaining time, rather than the ideal one. The 30 minute interval and general entry point to the UI still feel like untested hypotheses. Usability testing or even screen captures of longer sessions could begin to illuminate their effectiveness in the product.
  </p>

  <p>
    Production feels incomplete without the Prototype B implementation to close the loop on how to rebuild context by drawing attention to the note(s) to self from the previous session, after a reasonable interval of time.
  </p>

</details>

<a href="https://www.therightmargin.com/?ref=avkux" type="button" class="btn btn-success" target="_blank">&#10004; In Production</a>

{% include footer_case_study.md %}
