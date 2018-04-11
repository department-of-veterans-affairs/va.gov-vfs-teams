---
title: How to build and launch a form on [Name.gov]
label: How to build and launch a form on [Name.gov]
---

1. Perform preliminary user and policy research
2. [Put together form IA] (link to that chapter template thing we use)
3. Do project planning and documentation (link to that section of the Playbook)
4. Submit ATO documentation to Vets.gov Privacy and ATO Officers **Required**
  - If using an existing API, there’s a certain amount of ATO already in place. The additional things you’d need to get in place to be covered are:
    - Add new section to System Security Plan
      - [Examples / how to]
    - Add new fields to the PIA and PTA docs
      - [Examples / how to]
    - If there’s a new connection involved, then need an MOU (otherwise no MOU needed)
      - [Examples / how to]
  - [link to existing Vets.gov ATO docs]
5. Send email to the platform/devops team to kick off storage and connection configurations **Required**
  - There will likely be questions about architecture and data review needed at this point to set up infrastructure, so there’ll likely be an app walkthrough meeting that the Platform team will coordinate.
6. Refer to design system to see what UI elements you may want to use for different parts of the form
  - Radio buttons vs check-boxes
  - Free-text vs date-picker
  - Etc
7. [Form samples to look at before you get started - both schema, FE, any design system components that make sense]
8. Create your own branch off of vets-json-schema **Required**
9. Create your own branch off of vets-website **Required**
10. Create your own branch off of vets-api that takes in the form data and saves it  **Required**
11. Build your app by submitting PRs iteratively to have code merged to master **Required**
12. Schedule a demo and security review **Required**
13. When it’s robust enough, perform [usability testing](link)
14. When it’s fully built and ready for launch, submit your Launch Prep PR…
15. Perform 508 testing to make sure your application is accessible [link] **Required**
16. The Veteran-facing tools platform will provide:
  - QA testing
  - Load testing specs
  - Supplementary 508 reviews
  - [User Acceptance testing? Or should they do that?]
17. Coordinate with Call Center and Web Comms teams
18. Deploy to production behind a password
19. Remove password and add to navigation
20. Building the API to submit to (Maybe? Not sure how much backend documentation makes sense)
21. Implement form pre-fill feature (link to that component documentation?)
22. Production support for form
