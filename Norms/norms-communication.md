# Norms for Communication

**Definitions for terms used in this document:**

* *"DSVA" refers to DSVA team members and DSVA detailees.*

* *"Internal Contractors" refers to DSVA's primary vendor contractor and its subcontractors.*

* *"External Contractors" refers to any other contractor team working on the Veteran-facing Services Platform.*

<hr>

* [Communicating "breaking changes"](#communicating-breaking-changes)
* [DSVA and Internal Contractor responsibilities](#dsva-and-internal-contractor-responsibilities)
* [External Contractor responsibilities](#external-contractor-responsibilities)
* [Background for these decisions](#background-for-these-decisions)

<hr>

## Communicating "breaking changes"

Breaking changes are changes to design, content, or code that have the potential to affect (break) the work of other teams currently working on the Veteran-facing Services Platform (VSP). For example:
* A new design pattern is added to the design system
* The Sketch file has been updated
* A change to how the feature flag works
* A change to how the website build process works
* A significant change to the content style guide

The problem: We have many Slack channels where team members are figuring out the changes that need to be made. When decisions are made in these channels, those decisions are not always communicated to all the teams working on the VSP, notably the External Contractors are left behind.

The solution: A Slack bot that automatically posts breaking change content from other channels to a central Slack channel (```#breaking-changes```) where all teams can see the content. This Slack channel should contain no other conversation, so that team members can easily scan the channel to see if a breaking change affects their work or not.

#### Announcing a "breaking change"
1. When a decision has been made about a breaking change, a team member posts about the change in any **public Slack channel**. Channel must be public for this process to work.
1. The post needs to provide enough information that a designer, developer, or content person can know what they need to do in order to accomodate the change in their work.
    * E.g., "Sketch file has been updated to include new treatment for X. Find the Sketch file here [link]" or "We changed how the feature flag works. Instead of doing [describe the old way], you need to do X [describe the new way].
1. If additional information is needed to communicate the change and its impact, the team member can write it in Slack or include a link to a **public-facing** document on Github.
1. After posting the message, the team member must react to it using the ```:breaking``` emoji.
1. Using the ```:breaking``` emoji triggers Slack to automatically post a copy of the team member's Slack post in the ```#breaking-changes``` channel where everyone can see it.
 
#### Learning about a "breaking change"

* Existing team members will join the ```#breaking-changes``` channel.
* New team members will be auto-subscribed to the ```#breaking-changes``` channel when they're invited to Slack. 
* Team members will pay attention to announcements in the ```#breaking-changes``` channel.
* Team members will not clutter the ```#breaking-changes``` with other content. If conversation is needed about a breaking change, team members will thread (the goal is to make this channel as easy as possible for everyone to scan).
* Team members agree not to use the ```:breaking``` emoji except for the purpose of breaking changes. E.g., don't use it to announce that new stuff is on the website (there's other channels for that).


## DSVA and Internal Contractor responsibilities

### DSVA authorizes access for External Contractors.

* To ensure we limit VA access to the right people, a DSVA person will add External Contractors.
  * If a new need arises (e.g., access to a new Github repo is needed), direct the request to the DSVA Product Manager, who will determine access and permissions.
  * Internal Contractors cannot add External Contractors to Slack channels or to Github repos.

### DSVA and Internal Contractors provide support.
* DSVA and Internal Contractor teams will monitor the "Product" Slack channel for product-focused questions/inquiries from External Contractors.
  * E.g., *#claimsmodern* for the External Contractor team working on 526 forms
* DSVA and Internal Contractor teams will monitor the "Support" Slack channel for development, deployment, and project management questions from External Contractors.


### Internal Contractors can answer "How do I?" questions.

For example,
* How to set up and run a local dev environment
* How to access and deploy code
* How to get answers to specific code-related questions

The answers to "How do I?" questions are not directions; they're instructions to properly set up and use DSVA tools.


### Internal Contractors cannot direct External Contractor roadmaps.

Contractors cannot direct the roadmaps of other contractors or tell them what project they should work on next. For example,
* What should I be working on?
* What task should I do next?

If these questions come up, Internal Contractors should tell External Contractors to contact their own Project Manager.

**We do want Internal/External Contractors to collaborate because their projects will have dependencies and connections.**
* For example, an Internal Contractor may provide guidance or feedback on an External Contractor's architecture so that adjustments can be made to allow dependent tools to work well together.


#### Gray areas

Questions are bound to come up that fall somewhere between "How do I?" and "What do I?" In these cases, Internal Contractors should direct External Contractors to the DSVA Product Manager, who will decide how to handle the question/request.

We will track these "gray areas," so we can document our responses to them and decrease the amount of time the DSVA Product Manager needs to spend on them in the future.


<hr>


## External Contractor responsibilities

### 1. Look for documentation before posting a question in Slack (or contacting DSVA).
* See your team's Github "Product" folder or the VA Digital Service Handbook.
* If you don't find an answer, post in a Slack channel.


### 2. Use the 2 Slack channels for different purposes.

* **For product questions** use your team's "product" Slack channel (e.g., *#claimsmodern*).
  * Example question: "Where can I find previous research?"
* **For process questions**, use the *#support-external* Slack channel.
  * Example questions: "I can't get the proxy to work" or "How do I integrate this into that?" or "How do I use Zenhub to do X?"
* If you don't get a response within a few hours, ping someone you know in the channel to look at your question.
* If you don't get a response within 1 business day, contact the DSVA Product Manager, who will make sure the right people address your question.


### 3. Use best communication method.

#### Slack - best communication method
* Slack channels allow us to do our work in the open so that others can learn from the questions asked and the answers provided. Please do the same.
* We discourage private Slack conversations (DMs) for the same reason.
* **External Contractors should use the 2 Slack channels as their first method for contacting anyone on the DSVA or Internal Contractor team.**


#### Meetings - slowest communication method
* If your team has a question about something, ask it in a Slack channel.
* Don't wait to organize a meeting to ask a question; this will slow your team down.


#### Email - least effective communication method
* Email communications are not easily searchable or archivable.
* Use this as a last resort for getting in touch with DSVA or the Internal Contractor team.


<hr>

## Background for these decisions

### Goals

We want the system/process for External Contractor communication to be

* Reliable - External Contractors should know where to go and who to ask for information and questions
* Expert - External Contractors should expect that people assigned to answer their questions have the expertise to do so (or, know how to get the information from others with expertise)
* Timely - External Contractors should expect timely responses to requests for information and answers to questions (so we don't become a blocker to their work)

<hr>

### Problems to solve

* Contractors can't direct the work of other contractors.
* Need to minimize disruption of Internal Contractors (who are doing other program work).
* Need to minimize the amount of time DSVA Product Managers spend with autonomous External Contractors.
