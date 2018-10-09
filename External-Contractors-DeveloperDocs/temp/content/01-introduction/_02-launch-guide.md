---
title: Step-by-Step Guide to Creating and Launching an App on Vets.gov
label: Vets.gov Launch Guide
---
##### Keep this guide someplace handy so you can track your progress through your product’s lifecycle - checking in with stakeholders and the platform team along the way.
---
## 1. Roadmap Planning
### Expected timeframe: a couple of days
VA will need some initial information about your project to collaborate with you on prioritization. Put together a couple of sentences on your project idea and the problem it's solving, document your Project Manager and/or Business Owner and any other teammates that will be a part of this work, and what APIs and/or other services you anticipate you may want to use.

**You'll know you're done with this phase when:**
- [ ] This project information has been emailed to [Marvo Dolor](mailto:marvourneen.dolor@va.gov)

---
## 2. Discovery
### Expected timeframe: 2 - 6 weeks
Once Marvo has connected you to a DSVA Coordinator, your full implementation team is ready, and you have VA’s green light to get started, kick your project off by onboarding and starting discovery.

1. Send all teammate names, email addresses, and GitHub usernames to your DSVA Coordinator
1. Work through all steps to [discover user and business challenges and needs](../discovery/discovery-introduction)  
1. For engineers, familiarize yourself with the [Vets.gov Developer Documentation](../vets-developer-docs/getting-started)

**You'll know you're done when:**
- [ ] You've gone over the Product Outline and Discovery Findings with your DSVA Coordinator
- [ ] You've gone over your Technical Review with the Vets.gov Platform Team
- [ ] You've presented findings and proposed direction to your Content POC, your IA POC, and your stakeholders

---
## 3. Definition and Design
### Expected timeframe: 2 - 6 weeks
Iterate on your solution ideas, and keep testing. Eventually, you'll have the experience fully fleshed out and validated with users, stakeholders, and engineers.

1. Work through all steps to [design and define the user experience](../define-and-design/define-and-design-introduction)

**You'll know you're done when:**
- [ ] The Product Outline is complete
- [ ] You've done a plain language review of your experience with your Content POC
- [ ] You've gone over the end-to-end flow with your DSVA Coordinator, the Vets.gov Platform team, and your stakeholders
- [ ] You've gone over epics and user stories with your engineering team

---
## 4. Build and Test
### Expected timeframe: 2 - 6 weeks
This is all about getting your application built and online! You’ll have the platform team’s support at this stage to help you work through any technical roadblocks, perform code reviews, and provide guidance if you have questions as you go.

1. Send engineer names and contact info to your Platform POC to get added to pager duty
1. Work through all steps to [build and test your application](../building-and-testing/building-and-testing-intro)
1. Work with your Platform POC to:
  - add supporting static content pages to the ignore list
  - get your URL added to the server config
  - spin up storage and connection configurations
  - ensure the production:false flag is applied to prevent apps from going pre-maturely into production
1. Work with your Analytics POC to coordinate Google Analytics tracking

**You'll know you're done phase when:**
- [ ] Your application works end-to-end in the Staging environment
- [ ] You've reviewed your end-to-end staging experience with your DSVA Coordinator, the Platform team, and your stakeholders
- [ ] There are no launch-blocking bugs remaining from QA testing

## 5. Deploying
### Expected timeframe: 1 - 4 weeks
Make sure everything is functioning as intended in production and that you're ready for real users to find and interact with your application. Then work with the platform team to get it live!

1. Work through all steps to [deploy and market your application to live users](../deploy-your-app/deploy-intro)
1. Work with VA's 508 Office to get your application reviewed
1. Work with your Web Comms POC and DSVA Coordinator to plan how you'll let users know about the new product
1. Work with your Platform POC to:
  - do a pre-launch walkthrough, security review, and code review
  - update global site menus with navigation to your app
  - remove supporting static content pages from the ignore list
  - remove the production:false flag
  - remove password from production application
  - merge soft launch PRs to production

**You'll know you're ready to go live when:**
- [ ] All launch-blocking bugs have been resolved
- [ ] Necessary ATO updates are complete
- [ ] Call Center has confirmed they are prepared to handle calls that may come in about this product
- [ ] Business Owner, Platform Team, and DSVA Coordinator have all given "Go" responses in Go/No-Go meeting

## 6. Monitor and support
Now that your product is live, monitor analytics, error rates, and call center feedback to understand what features or changes are highest priority to work on in the next iteration. If an unexpected critical error occurs, the engineer slated for pager duty will be notified to coordinate resolution.

1. Work with the Platform POC to get any hard launch PRs merged to production
1. Execute your Web Comms plan

When you're ready to get to work on the next iteration of the product, start this process over again with Step 1!

<!-- Next Button -->
<a href='./browse-resources'><div class="next-button"><h5 class="next-text">Next: Browse Resources</h5></div></a>
