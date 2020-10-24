# title slide

I'm going to provide a high-level overview of the workflow for creating and publishing our workshop website.

# the requirements

## Setup
The requirements for our workflow are relatively simple. GitHub is the only platform that's a must. Each person who will contriubute to or manage the content should have their own GitHub account.

We gather all those individual accounts under a GitHub organization, which makes it relatively easy to add or revoke rights as collaborators come and go. All our repositories are "owned" by the organization, not by individual acconts.

## Material
The workshop source material is written in Markdown. Many workshop sites include the presentation slides - these can be added to the repository in any format, but doing them in reveal.js provides more flexibility for presenting them within the workshop site.

## Skills
The skills required for authoring content are familiarity with Markdown and GitHub. That's a relatively low barrier but those skills aren't universal and getting the whole team comfortable with these tools can take some work.
In additon to the basic authoring skills, someone on the team will need to understand how Jekyll works, but that can be just one person to handle the theme and configuration options.

Let me give you a better idea of what this looks like at the research commons...

# Markdown example
Here's an example of a Markdown file for the front page of a workshop about Docker...

# Docker site
... that looks like this onthe published site. This Introduction to Docker workshop created by Research Commons GAA Chelsea Palmer. The layout is simple and the content is presented across multiple pages with a navigation menu on the left.

#Each workshop
Each workshop we publish in this way has its own GitHub repository in the Research Commons GitHub organization.

## next
Here's a snapshot of what the repository looks like for that Docker workshop. At the top level is the index.md file corresponding to the page we just saw, as well as the config yaml file, which we'll look at in more detail soon.

## next
In the "content" folder are multiple markdown files; each becomes its own page on the workshop site. This folder organization is useful but not required: your markdown files can be anywhere in the repo: how they're presented on the site is governed by a yaml header in each file, not by the structure of the repository.

Those of you familiar with Jekyll will notice that there aren't many Jekyll-related files in this repo.

# theme
That's because in our setup, the workshop Jekyll theme lives in a separate repository. This helps keep display consistency across our workshop sites and makes updates and upgrades easier.

## Next
The Jekyll theme we use in the Research Commons is based on the Just the Docs theme, with some local changes to the layout and css files to meet our requirements. This repository is the central theme and is called upon whenever one of the workshop sites is built (whether by GitHub pages or in a local Jekyll environment).

# config
The link between the content repository and the template or theme repsitory is established in the config yaml file you may remember from earlier.

## remote themes
Here's a standard config yaml file from a Research Commons workshop. You'll find something like this in each of our workshop respositories. The highlighted remote theme line points to our theme repo and is all that's needed to stitch the content to the theme.

The config file also establishes a few variables that change from site to site, like the title, the link to the respository on GitHub,

## copyright
and this section with workshop-specific copyright information. All of our content is under some form of open license, but we give authors the flexibility here to choose which they prefer.

## Jekyll
Last on this page is a section that applies to those who run Jekyll locally to test the site before pushing to GitHub. Other settings you'd expect to find in a config file are covered by the config file associated with the theme repository.

# documentation
The trick with any workflow applied in a team environment is to get everyone on board, doing things in roughly the same way. To help with this, our theme repository is itself rendered as a GitHub pages site with step-by-step instructions for workshp authors.

# doc site
Show menu. It's a growing site, etc.
