# Git

**Create Branch and push to Remote**
```
$git checkout -b test origin/test
$git push -u origin <BRANCH>
```
**Set upstream**
```
$git branch --set-upstream-to=origin/<BRANCH> <BRANCH>
```


**Change remote**
```
git remote rm origin

$ git remote add origin https://github.com/user/repo.git
# Set a new remote

$ git remote -v
# Verify new remote
> origin  https://github.com/user/repo.git (fetch)
> origin  https://github.com/user/repo.git (push)
```




