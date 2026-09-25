# GitHub Upload Guide

## Repository

Create a public repository named `business-analyst-portfolio` under https://github.com/olalekanajimoti and upload the contents of this folder (not the folder itself), so this README sits at the top level.

## Option 1: GitHub website

1. Select **New repository**, name it `business-analyst-portfolio`, set it to **Public** and leave "Add a README" unticked.
2. On the empty repository page, choose **uploading an existing file**.
3. Drag in everything inside this folder. GitHub accepts up to 100 files per upload, so upload one top-level folder at a time.
4. Commit message: `Publish Business Analyst portfolio`.

## Option 2: Git command line

```bash
git init
git add .
git commit -m "Publish Business Analyst portfolio"
git branch -M main
git remote add origin https://github.com/olalekanajimoti/business-analyst-portfolio.git
git push -u origin main
```

## Profile page

The `github-profile-readme` folder in the download contains a README for your profile page. Create a repository named exactly `olalekanajimoti`, add that README, and it will appear on https://github.com/olalekanajimoti. Then pin `business-analyst-portfolio` from your profile.

## Before making it public

- Confirm you are happy to name each client or brand shown.
- Keep only anonymised data and approved screenshots.
- Be ready to explain every metric in an interview.
