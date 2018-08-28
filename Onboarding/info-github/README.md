# Github Information

<hr>

* [Background](#background)
* [Tips for creating a Github account](#tips-for-creating-a-github-account)
* [Using Github](#using-github)
  * [Store and share documents](#store-and-share-documents)
  * [Create, edit, and delete files](#create-edit-and-delete-files)
  * [Tips for managing files and folders](#tips-for-managing-files-and-folders)
  * [Manage agile workflow](#manage-agile-workflow)
* [Get help with Github](#get-help-with-github)

<hr>

## Background

Teams working on the Veteran Tools Platform use [Github](https://github.com/department-of-veterans-affairs) to

1. Store and share project documents. We do this to keep a record of project work and so all teams can learn from what other teams are doing.
2. Store and share Work Practices &#8212; our best practices for how we do things.
3. Use Github Issues to track progress throughout the agile delivery process.
4. Manage code and related version history.


## Tips for creating a Github account

1. Everyone working on the Veteran Tools Platform must set up a Github account.
1. Github accounts are subject to FOIA.
    * Set up a **new Github account for VA work.**
    * Do not use a personal Github account for VA work.
    * Do not use a previous employer Github account for VA work.
1. Github requires two-factor authentication (2FA) for new accounts.
    * If you use a Github account without enabling 2FA, you're likely to have problems pushing code.

## Using Github

### Store and share documents

GitHub is a system that stores documents and keeps a revision history of those files. It's divided into "repositories" (or "repos") which are groups of related files or documents. For example, this file lives in the ```vets-work-practices``` repo.

For non-developers, most of their Github work happens in the ```vets.gov-team``` repo where they store and share files.

Github makes it easy to "style" text-based documents using Markdown syntax. Learn how to use [Github Flavored Markdown](https://guides.github.com/features/mastering-markdown/).


### Create, edit, and delete files

You can use Github by visiting the repo URL in your browser and editing files from there. Or you can use the command line to interact with files.

If you're not familiar with Github, use the web interface to learn how Github works and what you can do with it.

* Review the [Github primer to learn how to do basic tasks like creating a file or submitting a pull request](github-primer).
* See [tips for managing Github folders](#tips-for-managing-files-and-folders).


### Tips for managing files and folders

1. Always use a dash (-) between words in file and folder names.
    * If a folder (or a file) name has white space in it, Github fills each white space with ```%20```. E.g., ```https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Work%20Practices/Accessibility%20and%20508```
    * This makes it hard for people to read Github URLs and even harder to type them (e.g., if you're on your mobile device).
1. Use meaningful descriptive titles for files (and folders).
    * Give files (and folders) descriptive names to help people understand what's in them **before they click into them**.
    * Avoid acronyms in titles. Characters are cheap. Use them!
    * Descriptive titles make it much easier to find things using Github's Search function.
1. Include a useful README.md file at the root of your folder structure, e.g., inside your "Product/Design" folder.
    * Useful READMEs tell people what's in the sub-folders and files **before they click into them**.
    * Consider a TOC approach - [here's an example](https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Work%20Practices/Research)
1. Use a predictable folder structure.
    * Follow examples set by people/teams who came before you. Browse around in ```vets.gov-team``` repo to see what other teams have done.
    * Don't make a bunch of sub-folders that each only contain a few files. This makes it much harder for people to find things.
1. When a folder contains 12 or more files, start thinking about grouping files into sub-folders to make it easier for people to find stuff.


### Manage agile workflow

Each Github repo has a section called "Issues." [Learn about issues](https://guides.github.com/features/issues/).

We use [Zenhub](https://www.zenhub.com) with Github to turn the "Issues" section into an [scrum board](https://en.wikipedia.org/wiki/Scrum_(software_development)).

The "Issues" section of the ```vets.gov-team``` repo is where all teams manage their Epics, User Stories, and agile workflow.

* Learn how to [get started using Zenhub](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Onboarding%20and%20Offboarding/zenhub_onboarding.pdf).
* See [how we use Zenhub for product/agile management](https://github.com/department-of-veterans-affairs/vets.gov-team/blob/master/Work%20Practices/Product%20Management/zenhub_product_management.pdf).


## Get help with Github

1. If you have problems using Github, [check the Github FAQs for potential solutions](../faqs.md#github).
2. Ask in a Slack channel.
