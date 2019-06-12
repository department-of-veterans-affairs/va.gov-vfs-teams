# Engineering Best Practices

Here is a brief list of Veteran Services Platform (VSP) recommended engineering best practices when working to add new features to the VSP.  

### Tickets/Issues/User stories

- refine tickets until they are atomic (possible guideline: nothing larger than an 8)
- use epics to tether together common bodies of atomic work
- include a background section providing context, resources, links, images, and/or POCs
- identify clear, concise, achievable acceptance criteria
- when applicable, identify risks that could impact delivery, resources, quality, etc.
- use tickets as a forum to discuss and capture implementation ideas, questions, patterns, access, etc.
  - in particular when implementation path is not clear, favor discussion prior to submitting a PR 
- when applicable, use tickets to collaborate and gain consensus on API contracts
- subscribe relevant VSP team members for visibility and agile support
- maintain accurate ticket status details (i.e. pipelines, assignees, blockers, etc.)

### Pull requests

- do not go longer than a week without pushing a WIP PR
- should there be scope creep, favor multiple, smaller, focused PR's over large PR's 
- include a background section providing context and a summary of why the PR is necessary, and what you've done in the PR
  - if applicable, include resources, links, images, and/or POCs
- include a _Definition of Done_ section that parallels what was completed in the PR to the originating issue's _Acceptance Criteria_
- when applicable, include screenshots (i.e. new API endpoint docs, new UI, etc.)
- feel free to request reviews for a WIP PR, and then use GitHub's [re-request review feature](https://github.blog/changelog/2019-02-21-re-request-review-on-a-pull-request/) to get final PR approvals
- identify WIP PR's by adding _WIP_ to the title, or using GitHub's [draft pull request feature](https://github.blog/2019-02-14-introducing-draft-pull-requests/)

### Backend development

- discuss your implementation ideas with VSP backend team members early and often; there are many common patterns and classes that are in place in Vets-API that should be leveraged, that we can point you to
- use [VCR cassettes](https://github.com/vcr/vcr) for recording external API responses
- if integrating a new external API, at the onset, request VPS DevOps team to make connections between respective Vets-API & external API environments (i.e. staging to staging, etc.)


### Frontend development
