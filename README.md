# Atomic Assessment Template for Sinatra Projects

The purpose of an atomic is to assess _just one thing_.

This is a template repo for creating atomic assessments. The idea is that you define a feature to build, and then set up everything _except one thing_. The student then needs to complete the feature.

The repo that a student starts with should not have any distractions from the atomic's core learning objective. E.g. don't include a tests folder at all, unless the purpose of the atomic is to go over testing. Or don't include the files for the database at all, unless the atomic deals with persistent data.

## Setup Guide

### Copying the template

Don't fork the repo. Instead:

1. Clone the repo locally.
2. Rename the folder it created. Use the naming convention: **web-toy__dash-separated-name**
3. From your cloned copy's folder...
  1. `rm -rf .git`
  2. `git init`
  3. `git add .`
  4. `git commit -m "First commit"`
  5. `hub create omahacodeschool/web-toy__dash-separated-name`
    - Use the real name!
  6. `git push -u origin master`

Now you can work on this repo as you would normally work on anything else.

### Setting up the atomic

- Update _README.md
   - Set title
   - Update description
- Database
  - **config/database.yml** - Change for both development and testing.
  - **config/environments.rb** - Change the value in `postgres://localhost...`
  - **db/define_schema.rb** - Create tables/columns as needed.
- Set up any models/controllers/views

Also, empty folders don't get pushed with Git. If you want a student to have a starter folder of some kind, add a README.md to the folder.

### Final Steps

- Make sure `bin/setup` works.
- Delete folders/files that aren't relevant to the atomic.
  - If you're removing database-related configuration files, make sure to remove dependent lines from other files.
- Make sure you can solve the atomic yourself.
- Delete this file and rename _README.md to README.md.