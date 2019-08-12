# README

https://devhints.io/jekyll

## How do I run the site locally?

`bundle exec jekyll serve`

## How do I deploy changes?

Commit & push to master.

# Maintenance

## Updating gems

1. Make a branch 

  `git checkout -b 2019-08-12-gem-update`

1. Ensure site runs locally **before any updates**

1. Check for outdated gems
  
  `gem stale`

1. Update all outdated gems

  `bundle update --all`

1. Ensure site still runs locally 

1. Merge to master

1. Push master to deploy
