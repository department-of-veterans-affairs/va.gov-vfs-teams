# Google Analytics

### General

* **All teams working on the Veteran-facing Services Platform are required to integrate VA's Google Analytics into their services.**
* **VFS teams should request Google Analytics when:**
  * The complete and final build is on staging and you're confident it's ready to launch.
  * At least 4 weeks before planned launch date
    - coordination with FE team needed
    - validation in staging needed
    - further clarification with PM is also helpful (Wireframes, intro meeting, etc)

### Prepare for Google Analytics

Answer the following questions in a Word document:

* What is the final step a user will take in their user experience?
* What steps in the user experience would you like to measure to understand progress and abandonment?
* What other user interactions, like Print or Save, are key to understanding the behavior of your users?
* What other navigation elements on the site will help you understand how your users navigate to, and use, your service?
* What success metrics have you identified for your service?
* What user interaction or behavior do you want to count as a "transaction" to track? What are your goals for each of these transactions?
* What custom dimensions (if any) would you like to collect? These can be user, session, or product traits.
* What are other events, interactions, behavior you want to track that aren't covered by the above questions?

### Request Google Analytics

1. File an issue in ```vets-team repo```.
    * Title: ```Request Google Analytics```
    * Labels:
      * ```analytics```
      * ```external-request```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Comment:
      * **Context**: Provide some context for your team's project.
        * e.g., ```Functionality adds a new dataset to the Facility Locator so users can search for and view non-VA health providers on the map, as well as in list and detail views.```
      * **Tracking information**: Upload the Word document you prepared above.
      * **URL**: ```link to your project on staging```
1. **Within 4 business days**, DSVA will create an implementation approach for Google Analytics in your project and will triage the analytics request to the appropriate Analytics Team member for implementation.
    * If you don't hear anything after 4 business days, reach out to your DSVA Contact.
    * There may be some back-and-forth in the Github issue comments as DSVA gathers the information needed to set up GA for your project and there may be additional analytics items created to support the original analytics request
1. When this is done, DSVA will update the Github issue.
    * *If custom events are required, DSVA will*
      1. Update the issue with a description of how to implement the custom events in the code.
      1. Your team will make the necessary code changes and push them to staging.
      1. Your team will update the issue with this comment: ```Custom events are set up```
    * *If custom events are not required*, DSVA will continue to the next step.
1. DSVA will verify that Google Analytics is working properly in your project on staging.
    * DSVA will update the Github issue with a preview link for your team.
    * During verification, DSVA may discover problems that require your team to update the code. If this happens, DSVA will update the Github issue with instructions on how to do that.
      * Once your team has fixed these problems, update the Github issue to ask DSVA to re-verify.
    * During verification, DSVA may discover problems that need to be fixed via Google Tag Manager. If this happens, DSVA will fix the problems and re-verify.
1. When DSVA is confident Google Analytics is working properly for your project, DSVA will
    * Add a comment to the Github issue: ```GA ready to go```
    * Close the issue.
1. When the issue is closed, Github will send a notification to the issue creator. This is your team's signal that this pre-launch activity is complete.


### Using Google Analytics

If your team will be continuously improving (or maintaining) the service **after launch,** you'll need to create a Google Analytics account using your VA email address. This will give you access to Google Analytics for VA web properties.

* Each person who will use Google Analytics will need to create a new Google Analytics account.
* Each person should create a **new Google Analytics account** using their VA email address.

Once your team has created new Google Analytics accounts:

1. File an issue in ```vets-team repo```.
    * Title: ```Provision Google Analytics```
    * Labels:
      * ```analytics```
      * ```external-request```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Comment:
      * **Context**: Provision the following Google Analytics accounts.
        * ```Provide a list of the Google Analytics accounts including full names and VA email addresses```
1. **Within 4 business days**, DSVA will provision these accounts so your team can start using Google Analytics.
    * If you don't hear anything after 4 business days, reach out to your DSVA Contact.
1. When DSVA has provisioned the accounts, DSVA will:
    * Add a comment to the Github issue: ```Google Analytics accounts provisioned```
    * Close the issue.
1. When the issue is closed, Github will send a notification to the issue creator. This is your team's signal that you can start using Google Analytics.
1. If the team will be continuing to monitor the Google Analytics, they should create new Github issues for addressing any changes to the GA implementation
