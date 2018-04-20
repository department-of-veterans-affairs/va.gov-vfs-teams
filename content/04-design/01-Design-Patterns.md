---
title: Vets.gov Design Conventions
label: Design Conventions
---


Vets.gov’s design is based on the [United States Web Design System](https://designsystem.digital.gov/) (USWDS) with some additional specifications to meet the needs of VA’s particular audience: Veterans and their families.

## The Design System
The Vets.gov Design System documents these design patterns and the React code to express them. Using a design system can radically simplify the process of getting to a first draft. In many cases, it allows you to skip high fidelity prototypes and go directly to code, based on text outlines of the form structure. But in cases where you may need to figure out a new pattern, you can also use a [Sketch template file](/assets/design/templates/vets-gov-pattern-library.sketch) as a starting point. It will allow you to quickly build screens using common static content and form patterns. From there you can link images together in InVision or another prototyping tool of choice.

## Design Conventions
### Keep it simple
There is a lot of unavoidable complexity in VA policy and proceedure, we endeavor not to add to it. This manifests in a few ways:
- Limit the number of decisions that a Veteran needs to make in one screen. We usually try to keep the number of questions under five. Two or three is even better.
- Find out what questions we need to ask. Sometimes we will “add” a question to simplfy things. Where a paper form might have a multicolumn table to ask questions about dependents, we will ask if they have any dependents. If the answer is no, we skip the table entirely. Similar for any fields that match an “if yes, please explain” pattern.
- Prefer simplicity over flexibility. It can feel helpful to give Veterans multiple ways or places to enter data. But this increases complexity and can end up being more confusing (and brittle) than reassuring.
- Minimize the number of fields. Social Security numbers and phone numbers are one field. We deal with dashes and other formatting on the back end.
- Minimize obfuscation. We don’t do the •••••••••• thing with SSN. Let people see the data they are entering.

### Reduce data entry
- Prefill data. We get as much data from VA systems as we can. If VA already knows it, we try not to ask for it again.
- Embed small forms. If there is a second form involved, we only ask the unique questions from that form. We fill the common stuff (name, date of birth, etc.) in from the data we’ve already collected.
- Save in progress. Any Vets.gov form can save progress so that a Veteran who is interrupted can pick up again later, right where they left off.

### Limit required fields
- We work with stakeholders to make sure that we are only collecting data that we _need_ to be able to deliver a benefit.
