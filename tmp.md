# Code Reviews

> Definitions for terms used in this file:
> * "Veteran-facing Services Team" refers to a combined group of engineers from the DSVA team and its primary vendor contractor (e.g., AdHoc).
> * "External Contractors" refers to any other contractor team working on the Veteran-facing Services Platform.

<hr>

## Overview

Code Reviews are a crucial part of how we work. Understanding why they are important and how we do them is an important part of working on the Veteran-facing Services Platform. *Any code going into a `master` branch needs a Code Review before it can be merged in.* 

With a few exceptions, requesting a Code Review is the same for both External Contractors and the Veteran-facing Services Team. Review the section for [Everyone](), then review the section for your team ([External Contractors]() or [Veteran-facing Services Team]()).

* [For Everyone](#for-everyone)
* [Request a Code Review](#request-a-code-review)
* [How to do a Code Review](#how-to-do-a-code-review)


## For Everyone

### Prerequisites

1. Understand how we use [Continuous Integration](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Continuous%20Integration%20Process.md) to develop and deploy code using GitHub.

1. Organize your work so that **each Code Review covers no more than 400-500 lines of code**. 
    * ***External contractors:*** See [Development Workflow](link-here) for more information on how to break your work into small Code Review Pull Requests (PRs).


### Code Review Norms

#### Why should I request a Code Review?

* Social pressures work. Knowing someone else is going to thoroughly examine your code incentivizes you to make better, more purposeful decisions.

* Code reviews share knowledge. They reduce single points of failure and share responsibility among the team. A code review should be a conversation about the why, and learning of the how.

* Code reviews stimulate conversations around code structure, style, and architecture as a natural part of our process everyday.

* The master branch is a place for stable code (even if it's not initially deployed to production). Code reviews are the last line of defense for catching bugs, stopping bad architectural changes, and making sure that things being added are in sync with team priorities.

#### When should I request a Code Review?

* You must request a code review any time you're putting new code into `master` or any other long-lived branch that multiple people are working off of.

* Even if the code isn't yet ready to be merged, a work in progress (WIP) code review can be helpful if you're solving a new problem, want to validate an approach, or are stuck and want another set of eyes. 
  * Be sure to prepend the PR title with "[WIP]" if you're seeking a WIP Code Review.
  * Be sure to use the `feature flag` if your code should not be visible in production.

#### Who should do my Code Review?

* Another developer who works on the same stuff from your team.
  * E.g. you're a back end developer requesting a review from another back end developer on your team.

* If the PR is purely for content, it can probably just be reviewed by a product person. Use your best judgement and be mindful of everybody's workload.

* If there are UX or copy changes, a designer or content writer should review the screenshots included in your PR.

* If there are product changes, a product strategist or designer should review your change before it goes to production
  * This doesn't necessarily have to happen during the PR phase. Some teams have product owners review feature changes in staging. Your team should have a process that you can follow.
  * **Note:** The easiest way for product people to review changes is the [review instances](Review%20Instances.md), accessible from the PR in Github.
  * This is important so we don't deploy beautiful, functional, elegant, technically brilliant but wrong products

#### What makes a good Code Review Pull Request (PR)?

* If a PR touches multiple content or application types (static, React applications, hybrid), split it along those lines and treat each content type as a separate feature with separate Code Review PRs.

* Keep your Code Review PRs small, i.e., **400-500 lines**.
  - If your PR becomes larger than 400-500 lines of code, you'll be asked to break the PR into parts.

* All Code Review PRs should include corresponding automated testing.
  * If you're creating new React/JSX components (or significantly modifying existing ones), update the existing unit tests and create new tests for new functionality.
  * If your code change affects more than one or two sections, create additional end-to-end tests to assert proper behavior. Examples might include elements that respond to `window.scroll` or `window.resize` events, or elements that dynamically show or hide content.

* Always describe the purpose of the change in the PR description.

* If you want feedback about a specific area, or if you're unsure about something in the code, include that in the PR description (or in annotations).

* If the PR changes anything about the design or user interface, include screenshots in the PR description.

* Be sure to allow time for following up on code review comments, as well as refactoring.

#### Code Review Guidelines
   
* Nothing related to the code is off limits or taboo. Code reviews can and should be about the nit-picky ("should there be a semi-colon there?"), the big picture ("why are we using a global variable?"), and everything in between.

* Giving a LGTM with no comments should be the exception, not the norm. The expectation is that every PR could be better with another set of eyes.

* Ask questions; don't make demands.

* Don't assume anything. If there's something weird or if you don't understand why the developer made the choice they did, ask about it!

* Learning by either talking to the author or Googling is expected. If someone implements something you don't understand or haven't seen before, look it up!

* If you still don't understand, ask for clarification.

* Don't use sarcasm.

* Talk in person if there are too many "I don't understand" or "Alternative solution" comments. Post a follow-up comment summarizing offline discussion.

* Review code in-line instead of in general PR comments. This makes it easier to see what you're referring to.

* It is expected that the assignee role gets alternated between creator and reviewer during the lifetime of a PR. Whoever's turn it is to review comments or take an action should be the present holder of the assignee role.

* If the only changes you have are small "nits", such as removing a semi-colon, the reviewer can give a "LGTM with nits" and assign back to the author. This tells the author that once they make those small changes, they can merge the PR themselves without further review. This should only be used when there are few, trivial changes.

* The phrase In My Humble Opinion (IMHO) does not belong in code reviews. Code review is about learning together and supporting each other, not about one person's personal opinion vs. another's.

<hr>

## Request a Code Review

### For Everyone

1. Create a PR by filling in the template: 
    * It asks for PR title, which should be preappended with [Project/Feature Name] follow by a one line description. For example "[Facility Locator Update] Adding choice locations data." 
    * The PR description should include a description of the change to give the code reviewer enough context to do an effective reivew.
    * The PR description should also describe the local testing you've done.

1. Pay attention to the codeclimate results of your PR, and fix any issues before requesting a review of your PR.

1. A PR's first review should be completed in **2 business days**. 
    * Turn around time is dependent on the number of PRs in the queue and the overall size and complexity of your code changes. 
    * The PR author is responsible for the PR; it is not sufficient to create a PR, assign someone, and not follow up. If you aren't getting a review in a timely manner, it's up to you to follow up until you do. *See the notes about this for External Contractors and Veteran-facing Services Team below*.  

* *Further notes on Code Review turnaround time*    

  * Code reviews are a high priority. They generally are not higher priority than the immediate thing a reviewer is in the middle of when the PR is created, but they bump up the priority queue every hour that passes.

  * Code reviews should be done as soon as possible without interrupting a reviewer's flow on what they are currently working on.

  * As a general rule, PRs put in before lunch should have a first review completed before the end of the day. 
    * PRs put in after lunch, if not able to be reviewed that day, should be the reviewer's first task the next morning.
    * This primarily applies to PRs that follow good PR practices for size and code quality. If you have a PR that's very complex, coordinate with reviewers to figure out when a PR can be reviewed.

  * Some code reviews take multiple rounds of review. It is expected that any minor reviews after the first round will go quickly. 

  * Some PRs are higher priority than others. These include active bugs in production and PRs that touch many files, as all other branches are likely to be out of date if the PR sits long without being merged ("bit rot" is the term often used for this). 
    * If a PR is high priority, it is the PR author's job to communicate how quickly they need a review and why this should be prioritized above other work.


### For External Contractors

1. Request a code review from someone on your team.
    * Click the gears icon under "Reviewers" to request someone on your team to review your code.
    * Make sure it's someone who can review your code and provide good feedback on it. Your teammate should review the [Specific Questions to Ask When Code Reviewing](#specific-questions-to-ask-when-code-reviewing) before reviewing your code.
    * **Your teammate must approve your code before you can go to the next step.**

1. After your teammate has approved your code, add the following comment to your PR:
    * ```Requesting a code review from @department-of-veterans-affairs/code-reviewers-for-external-teams-group```
    * **The Veteran-facing Services Team will only review your PR after someone on your team has approved your PR.**

1. Code quality is important. Expect code review comments and followup until your changes meet the code quality bar. 
    * It may take multiple rounds of comments and followup to fully review a PR. 
      * In that case, it's the responsibility of the PR author to make sure the reviewers know another round of reviews is required.
      * One good way of doing this is to clear the previous reviews and re-request reviews.
    * If a PR changes substantially in scope over time or changes and suggestions become hard to follow, consider closing it and opening a new one.
  
1.  If two days have gone by with no response to your PR, post a message in the #support-external Slack channel with a link to your PR and ask someone to review your PR. A Project Manager will work to get your PR prioritized for Code Review.
    * For high-priority PRs, such as active bugs in production, work with your DSVA point of contact to get this prioritized for Code Review.

1. **Your PR must be approved by two Veteran-facing Services Team code reviewers before it can be merged to master.**
    * Approval can come from any combination of engineers from DSVA or its primary vendor contractor teams.
    * Your PR needs a `LGTM` before it can be merged [see What acronyms mean](#what-aronyms-mean)).


### For Veteran-facing Services Team

1. Request a Code Review by using the **Request reviews** feature to request reviews from others.
    * If you need reviews from everyone you've requested, rather than just one, note that in the PR somewhere. Overcommunicating about what you need is ok!

1. It can be valuable to get someone experienced with the code to do a review (for example, the individual who wrote the initial code you're refactoring). It can also be valuable, however, to have someone unfamiliar with the code review it, both as a sanity check and to make sure multiple people on the team understand the code. Use your best judgment to appropriately balance team member's work loads, skill sets, and code base familiarity and remember that multiple people can review a PR (or portions of a PR) if necessary or desired.

1. If you have no idea who to get a review from, ask your team's tech lead or post the PR link in the #vetsgov-engineers Slack channel and ask "who is the best person to review this?"

<hr>

## How to do a Code Review

#### Review responsibilities

* If you're assigned to a PR, take responsibility and **review it as soon as you can.** Don't assume someone else will.
  * Don't make someone wait 24 hours for you to review a few lines of code; doing so does not create a positive, courteous code review culture.


#### Questions to ask when doing a Code Review
  * Are there logic errors in the code?
  * Are all cases (including edge cases and error cases) fully implemented?
  - Are the automated tests sufficient for the new code? Do existing automated tests need to be rewritten to account for changes in the code?
  * Does the new code conform to existing [style guidelines](https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Work%20Practices/Engineering/Style%20Guides)?
  * Does the new code conform to language and framework best practices?
  * Is the code readable and consistent?
  * Are variables and methods names self describing?
  * Is there a simpler way to solve this problem or implement this feature?
  * Should there be documentation included that would be useful to future developers?
  * How does this change impact the overall architecture of the application?
  * Does this align with an existing need (i.e. a GitHub Issue, business requirement, etc.)
  * Does this change impact the [threat model](/Work%20Practices/Engineering/Threat%20Model%20In%20Practice.md) (assets, attackers, attack vector)?
  * Is this the kind of change that might impact a dependent system (i.e. API URL change, etc.)
  * Were unit tests, linters, security scans, and accessibility scanners run?
  * Is there something that should be tracked in Google Analytics that isn't being done?
  * Is there any sensitive information in the commits? (If so, please remove it from Git history immediately and/or kill the remote branch until you can remove it locally)
    * Hardcoded PHI/PII from tests
    * Internal VA URLs and IPs (it doesn't make sense, but the VA OI&T goes berserk about this)
    * Authentication credentials or keys
  * Are database schema changes or other updates affecting global state hot-compatibility (the change must be compatible with existing running versions of the application)? (If so, use a multi-phase process introducing the migrations one step at a time - https://blog.codeship.com/rails-migrations-zero-downtime/).
  * Are data migration tasks side by side with schema updates? (If so, use a separate rake task to introduce data migrations and if necessary schedule that task manually during off hours).


#### Code Review acronyms

* LGTM - Looks Good to Me. A PR always needs one of these before it can be merged (with the exception of TBR explained below).

* TBR - To Be Reviewed. This means that the code author needs to get this PR in immediately and is merging the code without a review. The person the TBR is directed at should do a review ASAP. TBRs should be used sparingly and the reason for doing so needs to be explained in the PR. A conversation should occur about what can be done in the future to avoid TBRs in similar situations. Example: "TBR = @xyz. Production outage and everyone else is sleeping."

* PTAL - Please Take a Look. Tells when a review is ready to be reviewed or re-reviewed. Example: "Good catches! Edits made. PTAL @xyz"
