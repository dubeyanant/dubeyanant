### How to delete all old commits in a repo
[Original post Link](https://gist.github.com/stephenhardy/5470814?permalink_comment_id=3671126#gistcomment-3671126)
```git checkout --orphan newBranch
git add -A  # Stage all files
git commit -m "commit message" # Commit
git branch -D master  # Deletes the master branch
git branch -m master  # Rename the current branch to master
git push -f origin master  # Force push master branch to github
git gc --aggressive --prune=all     # remove the old files
