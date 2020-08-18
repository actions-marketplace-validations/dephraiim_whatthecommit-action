# What the Commit

**GitHub Action for committing messages from whatthecommit.com**

This is a GitHub Action that changes the last commit and replaces it with a commit message from https://whatthecommit.com

> _Risky for already forked repos_

### Setup

1. **Add a workflow file** to your project (e.g. `.github/workflows/commit.yml`) with this:

   ```yml
   name: New Commit

   on:
     push:
       branches:
         - main
         - master
     pull_request:
       branches:
         - main
         - master

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v2
         - name: Use Node.js
           uses: actions/setup-node@v1
           with:
             node-version: '12.x'
         - name: Change Commit
           uses: dephraiim/whatthecommit-action@v1
   ```

### Commiting

Using the workflow above, GitHub will modify the last commit with a commit message from https://whatthecommit.com

### Development

Contributions and Suggestions are always welcome!

### LICENSE

[MIT](./license)
