## Some Git Commands

#### To delete all old commits in a repo -> [OP](https://gist.github.com/stephenhardy/5470814?permalink_comment_id=3671126#gistcomment-3671126)

```
git add -A  # Stage all files
git commit -m "commit message" # Commit
git branch -D master  # Deletes the master branch
git branch -m master  # Rename the current branch to master
git push -f origin master  # Force push master branch to github
git gc --aggressive --prune=all     # remove the old files
```
#### To change commit author by preserving dates -> [OP](https://stackoverflow.com/a/61217637)

`git rebase -i --root` OR `git rebase -i -p 0ad14fa5`

And then repeat this command for all the commits
`export GIT_COMMITTER_DATE=$(git show --no-patch --format=%aD) && git commit --amend --author="Anant Dubey <anantkumar312@gmail.com>" --no-edit --date="$GIT_COMMITTER_DATE" && git rebase --continue`

#### To change commit date and time -> [OP](https://stackoverflow.com/a/5017265)

`GIT_COMMITTER_DATE="Wed Mar 26 12:15:00 2024 +0530"  git commit --amend --date="Wed Mar 26 12:15:00 2024 +0530" --no-edit`
