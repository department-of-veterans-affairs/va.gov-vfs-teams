# Security and ATO


<hr>

**This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal contractors" refers to DSVA's primary vendor contractor (e.g., AdHoc) and its subcontractors.*

  * *"External contractors" refers to any other contractor team working on the Veteran Tools Platform.*

<hr>

* [Request a preliminary ATO review](#request-a-preliminary-ato-review)
* [Request a Pre-launch ATO review](#request-a-pre-launch-ato-review)

<hr>

### What is an Authority to Operate (ATO)?

The purpose of an Authority To Operate (ATO) is to ensure the risks to VA (operations, assets, or individuals) are acceptable. If the risks are low, VA issues an ATO for the system involved.

The Veteran Tools Platform has **a platform-wide ATO from VA** (dated March 2, 2017). The DSVA team is responsible for maintaining that ATO. DSVA updates the ATO (and any related RiskVision items) when new applications are added to the platform (or when new features are added to existing applications).


### Request a preliminary ATO review

**Connect with the DSVA team as early as possible to start this process.**

1. File an issue in the <a href="https://github.com/department-of-veterans-affairs/vets.gov-team" target="_blank">vets.gov-team</a> repository. *When you've completed the onboarding steps, you'll be able to view that repo.*
    * Title: ```Request preliminary ATO review```
    * Labels:
      * ```external-request```
      * ```devops```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Provide the following information in the Comment field: 
      * What data are you collecting? For example, what data are you requesting from users?
      * What data are you using? For example, what data are you requesting from some VA service?
      * Where does that data come from? For example, what API endpoint are you getting the data from?
      * See [an example issue](https://github.com/department-of-veterans-affairs/vets.gov-ato/issues/318) to illustrate the kinds of information we need for this preliminary assessment.
1. DSVA will examine the existing ATO documents and determine if they need to be updated based on the information you've provided.
    * Plan for some back and forth conversation in the Github issue to get all the information DSVA needs.

1. DSVA will provide a preliminary ATO assessment of whether or not the ATO needs to be updated.


### Request a Pre-launch ATO review

You'll need a **Pre-launch ATO review** before you can launch your tool or service. Complete this step when you know that your tool/service **will not** change before launch.

1. File an issue in the <a href="https://github.com/department-of-veterans-affairs/vets.gov-team" target="_blank">vets.gov-team</a> repository. *When you've completed the onboarding steps, you'll be able to view that repo.*
    * Title: ```Request Pre-launch ATO review```
    * Labels:
      * ```external-request```
      * ```devops```
      * ```[your Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your team's DSVA contact]```
    * Provide the following information in the Comment field: 
      * What data are you collecting? For example, what data are you requesting from users?
      * What data are you using? For example, what data are you requesting from some VA service?
      * Where does that data come from? For example, what API endpoint are you getting the data from?

1. DSVA will examine the existing ATO documents and determine if they need to be updated based on the information you've provided.
    * Plan for some back and forth conversation in the Github issue to get all the information DSVA needs.

1. If the ATO needs to be updated:
    * DSVA will update the relevant ATO documents.
    * DSVA will make all necessary updates in RiskVision.
    * DSVA will let you know the ATO has been updated.

1. If the ATO does not need to be updated:
    * DSVA will let you know that the current ATO still applies.
