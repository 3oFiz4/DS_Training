# Collaboration Guide

Project uses Pull Requests (PR). **DO NOT PUSH DIRECTLY TO `main` UNLESS INSTRUCtRED**.

## Workflow

notebooks/
├── notebook.ipynb ← Main/shared notebook (shared artifacts, do not modify)
├── yo.notebook.ipynb ← Jordan's copy, only Jordan may modify, everybody should not.
|-- yo/ ← Jordan's only folder, no one can modify (shared artifact, owner Jordan)

Please follow this regulation. Do not directly modify main branch or main files, even if it is `I only run it!`.

The Workflow in short becomes like this:

1. Pull from latest `main`
2. Work ONLY your OWN notebook, not other notebook. If you want to modify theirs, copy theirs and paste them in your newly created OWN notebook.
3. Commit and push changes to your own branch
4. If you feel like pushing changes that everybody should have, consider `yo/analisa_parent_education_terhadap_fitur_yang_lain.ipynb`, which is available to everybody to inspect (NOT TO MODIFY ONCE AGAIN). You can do PR. In your title, add "Merge request: ", and explain why it deserves to be merged into main, and for everybody to see?

## Conventional Commit

Please read more about conventional commit standard in here (https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13):

Mostly used scopes:
feat (feature): Commit that add/remove/change something
fix (fix): Commit that fix something
refactor (refactor): Commit that rewrite without altering functionality
perf (performance): Commit that improve performance
style (style): Commit that address code style, formatting, comments

Usage:

> `[type]([scope]): <changes but in imperative>`
> Example:
> fix(df_info): add complementary validator for df

## First time setup

1. Do `pip install nbstripout`
2. On this repo, do `nbstripout --install`
3. Do `git config --get filter.nbstripout.clean`
4. `git clone https://github.com/3oFiz4/DS_Training` (clone the repo)
5. `cd DS_Training` (go to repo dir)
6. `git branch` (check your branch, should be `main`)
7. `git switch <assigned_branch_name>` (switch to the branch you are assigned to, either [ru, yo, ar])
8. `git remote add origin https://github.com/3oFiz4/DS_Training.git` (add remote)
9. Create a file named: `<assigned_branch_name>.notebook.ipynb` (this will be your branch file)

## Pulling

Always download latest change from `main` before making any changes.

1. `git switch <assigned_branch_name>` (switch to the branch you are assigned to, either [ru, yo, ar])
2. `git pull origin main` (download latest changes from `main`) or `git pull` (if `remote` is set)

## See what changes have been made

1. git status (check files that is modified/removed/created)
2. git diff (check changes)

## Save your work

1. `git add .` (add all changes)
2. `git commit -m "message"` (commit changes, message should be meaning full, follow conventional format!)

## Upload your work (to your own branch, in github)

1. `git push origin <assigned_branch_name>` (push changes to your branch)

## Create a PR

PLEASE PLEASE PLEASE NEVER EVER `git push origin main`!!!

1. Do this (install `gh` first):

```bash
gh pr create \
  --base main \
  --head <assigned_branch_name> \
  --title "<changes_title>" \
  --body "<changes_description>"
```
