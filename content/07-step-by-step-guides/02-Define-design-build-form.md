---
title: Define, Design, and Build the form
label: Define, Design, and Build the form
---

1. [Define the project and requirements](jump link to Define section)
2. **Email Angela Gantt-Curtis and Marvoureen Dolor to get the green light to start building *Required***
3. [Design the form](jump link to Design section), referring to the various [design components](jump link) to see what you may want to use for the various form interactions.
  - [Form samples to look at before you get started - both schema, FE, any design system components that make sense]
4. **Email ATO documentation to Vets.gov Privacy and ATO Officers *Required***
  - If using an existing API, there’s a certain amount of ATO already in place. The additional things you’d need to get in place to be covered are:
    - Add a new section to [System Security Plan](link?)
      - [Examples / how to]
    - Add new fields to the [PIA and PTA docs](link?)
      - [Examples / how to]
    - If there’s a new connection involved, then you’ll need an MOU
      - [Examples / how to]
5. **Email the Platform team to kick off storage and connection configurations *Required***
  - There will likely be questions about architecture and data review needed at this point to set up infrastructure, so there’ll likely be an app walkthrough meeting that the Platform team will coordinate.
  - **NOTE: at this time, any features that require direct database access within vets-api are not supported.**
6. **Create your own branch off of vets-json-schema *Required***
  - [Reference this schema development guide to ensure your PR will pass the various merge requirements](link to doc enumerating schema details...)
  - This is for the back-end: set up the form schema there to incorporate into your form
  - This is for the basic structure for submission to the API and contains some required fields and some basic validation
  - Use common definitions for schema elements
7. **Create your own branch off of vets-website *Required***
  - [Reference this front-end development guide to ensure your PR will pass the various merge requirements](link to doc enumerating details from Jeff)
  - This is where you’ll build the front-end of the form
  - This is where you’ll incorporate most of the validation and conditional fields
  - **Use this [Yeoman form generator](https://github.com/department-of-veterans-affairs/generator-vets-website) to create a React skeleton for the form on your new vets-website branch *Required***
8. **Create your own branch off of vets-api that takes in the form data and saves it *Required***
  - Reference this [back-end development guide](need link from James) to ensure your PR will pass the various merge requirements
  - This normally will happen in parallel with the vets-website build
9. **Build your app by submitting PRs iteratively to have code merged to master *Required***
  - Submit PRs for vets-json-schema, vets-website, and vets-api when you’ve completed enough code that you’re ready to start verifying your progress in staging.
    - If the PRs are related to or dependent on each other, make sure they reference each other
    - Use [WIP] in your PR titles if you have a PR open but aren’t ready for it to be reviewed and merged to master.
    - Request a Review from [who? how?]
    - [Naming convention or label needed]
    - **RISK: since other teams don’t use our same tracking system (Rational vs GitHub), we won’t be able to have context for code reviews. We’ll be limited to checking architecture, regression testing, and code cleanliness.**
  - You’ll get a code review from the digital service team for each PR you merge
    - Reviewer will perform a code review: https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Engineering/Code%20Review%20Norms.md#specific-questions-to-ask-when-code-reviewing) including things like regression testing, checking code style, unit test coverage, etc.
    - Expect some collaborative conversation with the Reviewer as this is underway
  - Once approved, your PRs will be merged into master, and your app will be deployed to the Dev and Staging environments
    - Note: by default, all forms built using the Form Generator will have a gate on them to prevent the application from appearing in production
    - **RISK: right now, the team building this could remove the production:false flag on their own if they wanted to (i.e. without the app going through the proper reviews etc). Do we want to prevent that systematically, or not?**
    - NOTE: may want to consider moving to a fork model long term, while just putting a cap on the volume of app builds in the short term so that it can be handled in the manner described here.
    - QUESTION: do we want to set up GitHub roles for non-DS teams such that they don’t have Review or Approve access? Not sure if it’s possible…
10. When it’s robust enough, perform [usability testing](jump link)
11. Send a product guide to the Call Center and chat with them so they can prepare their scripts and train their teams
