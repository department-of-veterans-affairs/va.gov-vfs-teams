# Github Primer

* Github introduction materials
* You can use this folder to practice in

### Agenda

<hr>

* [What is Github?](#what-is-github)
* [Your product folder](#your-product-folder)
* [Github web interface tour](#github-web-interface-tour)
* [Basic Github workflow](#basic-github-workflow)
* [Common activities](#common-activities)
  * [Edit a file](#edit-a-file)
  * [Create a file](#create-a-file)
  * [Create a folder](#create-a-folder)
  * [Delete a file](#delete-a-file)
  * [Upload files](#upload-files)
  * [Delete a folder](#delete-a-folder)

<hr>

### What is Github?

* Github is a version control system for files and documents, notably for code. But we also use it store and share other project documents. And we use it to manage our agile workflow.


### Your product folder

Your product folder is part of the vets.gov-team Githubrepository. It's here: [Vets.gov-team repo > Products > Disability Compensation > BAH-526](https://github.com/department-of-veterans-affairs/vets.gov-team/tree/master/Products/Disability%20Compensation/BAH-526)

* Use this folder to store documents and share amongst your team.
* Other Veteran Tools Platform teams can also see your content and learn from it.
* At a minimum, post your Discovery, Design, and Engineering documents.


### Github web interface tour

* **Branch**
  * The master branch is always the source of truth for your product folder.
  * Make sure you're on the master branch. Switch if you're not.
* **Create a file** - add a new file (we'll come back to this)
* **Upload files** - (we'll come back to this)
* **Find file** + **History** - you shouldn't worry about these
* **Folders**
  * Folders have to contain at least one file.
  * README.md files are automatically displayed at the root of each folder. If you don't have a README.md file in a folder, the screen will just show the list of files.
* **Navigation**


### Basic Github workflow

1. You make a commit - adding, editing, or deleting a file
1. Github creates a new branch for you
1. You make a pull request (PR) to merge your new branch into the master branch
1. DSVA person reviews and approves your PR
1. Your commit is merged into the master branch and is visible to everyone else

    * A **commit** is a set of changes from the previous version of the repository.
    * A **branch** is a way to isolate a set of commits you want to make to the repository.
    * A **pull request** allows for review and approval of a branch before it is merged into the master branch of the repository.


### Common activities

#### Edit a file

1. Select the file
1. Click the pencil icon to start editing.
1. Make a change using [Markdown](https://guides.github.com/features/mastering-markdown/).
    * Click **Preview** to see what the content will look like
1. Scroll to bottom to start creating your pull request - note the new branch created for you.
1. Add a title and comment to describe your change
1. Click **Propose file change**
1. Make sure you're comparing the master branch to your new branch
1. If the changes look good, click **Create pull request**
1. Click **Create pull request** again
1. Request review from ehuntdsva or AZSchneider
1. Github checks that the file can be merged and notifies your reviewer
1. Your reviewer merges your PR
1. Your page will show the merge - please delete the branch now - it's no longer needed !


#### Create a file

1. If you like writing on your computer, do it there and go to [Upload files](#upload-files)
1. Click **Create new file**
1. Name your file - use lowercase names and we recommend using hyphens for white space
1. Add your content using [Markdown](https://guides.github.com/features/mastering-markdown/)
1. Follow the steps in **[edit a file](#edit-a-file) beginning with *Step 4***.


#### Create a folder

Let's say you want to create a new subfolder called "mynewfolder" inside the "BAH-526" folder. To create the folder, you'll create a README.md file in that new folder first.

1. Navigate to the "BAH-526" folder.
1. Click **Create new file**
1. In the name field, type
```mynewfolder/README.md```
1. Add some content using [Markdown](https://guides.github.com/features/mastering-markdown/).
    * You can later delete this file if you don't need it (or modify it).
1. Follow the steps in **[edit a file](#edit-a-file) beginning with *Step 4***.


#### Delete a file

1. Navigate to the file you want to delete.
1. Click the **trash can icon**
1. Scroll to bottom to start creating your pull request - note the new branch created for you.
1. Add a title and comment to describe your change
1. Click **Commit changes**
1. Follow the steps in **[edit a file](#edit-a-file) beginning with *Step 7***.


#### Upload files

1. Click **Upload files**
1. Drag files into the box (or click **choose your files**)
    * **Note**: be sure the files are named correctly before uploading them.
1. Scroll to bottom to start creating your pull request - note the new branch created for you.
1. Add a title and comment to describe your change
1. Click **Commit changes**
1. Follow the steps in **[edit a file](#edit-a-file) beginning with *Step 7***.


#### Delete a folder

To delete a folder, you first need to delete all the documents in it. Once you do that, the folder will disappear.
