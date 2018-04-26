---
title: Rudimentary Technical Review
label: Rudimentary Technical Review
---
## Overall philosophy
Use an existing API if it's available and will provide what's needed to meet core product functionality and performance standards. If the experience (both user experience and business process experience) for the product in question would be significantly deprecated with any of our existing options, then we need more technical discovery to determine how to create a new service: i.e. should someone build a middle service, or should it be a direct connection?

*(Note: "significantly deprecated" is a judgement call to be made by the Product Manager in consultation with their implementation team.)*

## How to find out what services exist that we could explore
- Dig around [vets-api](../vets-developer-docs/vets-api/vets-api-readme) to see what APIs are already available to use
- Ask around to see if there are other APIs out there that we might not yet know of

## How to determine if an existing service meets our functionality and performance needs
- What kinds of simplifications would​ be​ required when building against this service?
- Do we anticipate needing additional branch logic or conditions?
- What data is available in the service beyond what we would likely need (i.e. is it too bloated or complex for what we need)?
- Is there data we think we'll need that's not included in the service?
- How reliable is it?
- Are there decent routes available for resolving issues between sources?

## How to determine who should create a new service if needed?
- Is the data underneath changing frequently?
- For Getting or Posting data, will it have to communicate with more than one system?
- Is there a lot of logic needed to transform the data into what we need for the product?

<!-- Next Button -->
<a href='../define-and-design/define-and-design-introduction'><div class="next-button"><h5 class="next-text">Next: Define and Design Your User Experience</h5></div></a>
