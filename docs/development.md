## Getting started with Fractal

These instructions assume you're using Terminal, and that you're starting from scratch as far as a development environment is concerned. If you've already got dependencies installed, move on to **Install Fractal**.

> If you're on a VA laptop and you don't have Administrator privileges, you may not be able to install and run platform-docs locally. You can still use platform-docs as a reference by visiting the [stable URL](https://department-of-veterans-affairs.github.io/va-digital-services-platform-docs).

### Installation

**Install Homebrew**
* To install Homebrew, [follow these instructions](https://www.howtogeek.com/211541/homebrew-for-os-x-easily-installs-desktop-apps-and-terminal-utilities/).
* **If you don't have Administrator privileges,** run the following steps in Terminal at the command line prompt (`$`).
  1. `cd ~`
  2. `git clone https://github.com/Homebrew/homebrew.git ~/.homebrew`
      > Note: If xCode Command Line Tools are not yet installed, you'll be asked to install them before you can install Homebrew. Just say "yes" to everything. Then do Step *ii* again.
  3. `echo "export PATH=~/.homebrew/bin:\$PATH" >> ~/.bash_profile`
  4. `source ~/.bash_profile`
  5. `brew update`

**Install Yarn**
* Install Yarn with Homebrew. In Terminal, run `brew install yarn`.

**Clone the va-digital-services-platform-docs repo**

If you're familiar with cloning repos from Github using Terminal, skip ahead to **Install Fractal**.

You can put the repo anywhere on your computer, but as a suggestion:
- In Terminal, navigate to your desktop: `cd ~/desktop`
- Clone the Github repo by running: `git clone https://github.com/department-of-veterans-affairs/va-digital-services-platform-docs.git`
- Then: `cd va-digital-services-platform-docs`

**Install Fractal**

Still in Terminal, run `yarn install`. This will download and install all the dependencies that Fractal needs to run on your local machine. It might take a minute to complete the process.

### Viewing the site locally
Start server by running `npm run start`.
  * If `npm run start` fails, run `$ npm i`. Then do `$ npm run start` again.
  * If the `fractal watch` task fails, remove the `dist` directory and try running `npm run start` again.

Stop server by pressing *CTRL + c* keys while you're in Terminal.

View the site by navigating to `localhost:3002` in your favorite browser.

## Deployment

Jenkins automatically publishes the content to GitHub Pages (the `gh-pages` branch on this repository) on pushes to master.

To make changes:

- create a branch off master
- make changes
- create a PR
- ensure PR is approved and Jenkins tests pass (GitHub will not let you merge without these two)
- merge to master and Jenkins will automatically deploy.

## Choosing a design system for Vets.gov

This has been migrated to [another file](research.md) in order to keep the README instructional.
