---
title: Docs Setup
parent: Setup
---

Here is the setup required to locally run the docs if you want to modify it.

> We are using github actions and github pages to automatically update and publish docs after each merge to main.

## Run Locally

1. Make sure you have [Ruby](/docs/setup/docs-setup/ruby) installed.
1. Install the bundle: `bundle` or `bundle install`
1. Run the server: `bundle exec jekyll serve`
1. Check it out in: [http://127.0.0.1:4000/](http://127.0.0.1:4000/)