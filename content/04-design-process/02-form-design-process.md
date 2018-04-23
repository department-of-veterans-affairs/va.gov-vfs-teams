---
title: Form Design Process
label: Form Design Tips
---

## Seek deep understanding of process
VA benefits can have complex processes and requirements, and as an outsider it can take time to peel back all the layers. In our experience it can be helpful for all parties to take a step back and walk through the sequence with as fresh eyes as possible.
- How do people find out about this benefit?
- Who is elegible?
- What is required to apply?
- What happens next?

### Audit the form
All these questions can reveal hidden complexity and communication challenges. Schedule a field by field review of the existing paper forms (and digital if they exist) with your business owner, and front line staff if possible. Every discipline should be involved at this point.
- How does this field impact the decision process?
- Is it required? If not, could it be removed?
- Are there any other questions that are related? Does it only apply to a subset of applicants?
- Does the label use familiar language?
- Do applicants make any common errors with this field?
- Does this field require one of a list of specific answers?
- Is there any way we can get the answer from a VA system?
  - If not, could we infer the answer from another response?
- Is there any helpful context that would make the question easier to answer?

Document this in a format that is readable and sharable with your team.
- CSV files will render in GitHub and can be edited with a spreadsheet app, regardless of platform. Limited formatting. [Template]()
- Outlining the form in a (markdown) text file can give you more formatting and is more easily editable _in_ GitHub. [Template]()

If you reach decisions about removing questions, or altering them. Write the decisions down in a [Significant Decisions]() file within your project directory. This will come in handy during later (why did we do this) discussions.

### Talk to users of the form
Interview people who have gone through the process before.
- What parts of the process were painful?
- What do you wish you’d known before you applied?

### Discuss What happens next
Talk through what happens after an application is submitted. Discuss both the VA, and applicant side. This will often reveal information that could be communicated to the applicant to prepare them and head off questions.
- How does an applicant know that they have done all they need to do?
- How do they find out if something is wrong?
- How are they notified that the benefit is awarded?
- How long does it take?

### What are the technical constraints?
What systems are available to improve the application process? What are the complicating factors?
- Is there a place to submit structured data?
- Do we need to make a PDF to submit?
- Are any critical services unavailable frequently?
  - How long are the outages?
    - Are there useful status codes?
  - Are they only available during specific hours?

## Document your solution
Find what works best for your team! But we have had good success with lightweight text based docs for screen documentation, backed by diagrams to describe flow. We try to only go to high fidelity comps in the case of new patterns. We lean heavily on our design system.

1. Break the form into screens, grouped by chapter.
2. Identify field types
  - List possible answers where applicable
  - Mark required (or not)
  - Describe conditional relationships
3. Create a punchlist for any copy needs
4. Think about entry and exit points for the form
  - Does your form require changes to navigation?
  - Is related static content up to date?
  - Are there any other places you should be able to get to the form from?

### Examples
- [Example form outline]()
- [Example flow diagram]()

## Other things we have run into
- Is the form currently being revised by the owner?
- Are there any workarounds employed in the processing of applications that we might break with changes?
- Outdated conventions in form questions
  - Inflexible labels like husband and wife
  - Gender questions asked solely for salutation purposes
- Forms are much easier to test in live code than image based prototypes
  - Participants can entering data will reveal problems that mocked in data won’t.
  - Branching logic in image based prototypes is tedious and brittle

## People to involve
Not all of these will apply in every situation, but it's good to check.

### Stakeholders
- Benefit business owner
- Subject matter experts
- Front line staff who process the form
- VA or VSO folks helping applicant to complete the form

### Users
- Veterans
- Family members
- VA employees that help Veterans to complete the form
- Servicemembers
