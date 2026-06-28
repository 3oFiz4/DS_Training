# Panduan Kolaborasi

Proyek ini menggunakan _Pull Request_ (PR). **JANGAN MELAKUKAN PUSH LANGSUNG KE `main` KECUALI DIINSTRUKSIKAN**.

Silakan baca lebih lanjut mengenai standar _conventional commit_ di sini (https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13):

Tipe yang paling sering digunakan:
feat (fitur): Commit that add/remove/change something
fix (perbaikan): Commit that fix something
refactor (perubahan): Commit that rewrite without altering functionality
perf (performa): Commit that improve performance
style (gaya): Commit that address code style, formatting, comments

Pengunaan

> `[tipe]([scope]): <Perubahan dalam kata perintah>`
> Contoh:
> fix(df_info): add complementary validator for df

## First time setup

1. `git clone https://github.com/3oFiz4/DS_Training` (clone the repo)
2. `cd DS_Training` (go to repo dir)
3. `git branch` (check your branch, should be `main`)
4. `git switch <assigned_branch_name>` (switch to the branch you are assigned to, either [ru, yo, ar])
5. `git remote add origin https://github.com/3oFiz4/DS_Training.git` (add remote)
6. Create a file named: `<assigned_branch_name>.notebook.ipynb` (this will be your branch file)

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
