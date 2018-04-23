---
title: Google Analytics Checklist
label: Google Analytics Checklist
---
Here are the steps required to prepare a new product for Google Analytics

1. Product owner determines what they want tracked in the product
2. Analytics reviews and makes recommendations about how to track (page views, custom events, etc.)
3. Analytics determines a prefix for events/variables and adds to documentation
4. For custom events, either sprint team front-end developer or analytics can submit PR for adding custom events
5. Product owner determines what will represent a "Transaction", if anything on the site.
6. Based on custom events, transactions, etc. the analytics team adds:
  - Triggers to pick up events and variables
  - Tags to report out those triggers
  - A folder in GTM to hold those items together
  - Adding goals and funnels for any transactions
  - Custom dimensions to coverage usage of the site
  - Update custom dimensions for broad usage areas as needed
7. Analytics team performs verification in staging to ensure tags/triggers are firing correctly
