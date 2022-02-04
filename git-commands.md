## Git Commands
### Here I'm going to be writing git commands

For reference "-" is an abreviation flag, "--" is a words flag

<strong>Display logs in a short manner</strong>
```
git log --oneline
```

<strong>To check difference between to files:</strong>
```
git diff
```

<strong>Check diferences even after adding files to staging status</strong>
```
git diff --staged
added more
```

<strong>Ammend git message</strong>
```
git commit --amend -m "new message"
```


<strong>Ammend git message in vim</strong>
```
git commit --ammend
```

<strong>Resert commit SOFT by one </strong>
```
git reset --soft HEAD^
```

<strong>Reset commit SOFT by hash commit</strong>
```
git reset —soft <commit_hash>
```

<strong>Reset commit MIXED by hash commit</strong>
```
git restet —mixed <commit_hash>
// this makes the commits after that one commit, to disappear
```

<strong>Reset commit HARD by hash commit</strong>
```
git reset —hard <commit_hash>
```

<strong>Check all the history even after deleting files</strong>
```
git reflog 
```
after reflog you could do: 
```
git reset —hard <commit_hash>
```

<strong>rename file in git repo</strong>
```
git mv ./file_name new_file_name
```

<strong>delete file from repo</strong>
```
git rm file_name
```

<strong>merge other branch to main</strong>
```
git merge main <branch_to_bring>
```

<strong>delete branch</strong>
```
git branch -d <branch_name>
```

<strong>delete branch force</strong>
```
git  branch -d <branch_name> -f
```

<strong>show logs</strong>
```
git log —oneline —graph --reflog
```

<strong>Add Tags in current branch and commit</strong>
```
git tag -a v0.0.0 -m “message tag”
```

<strong>Add Tag in other commit</strong>
```
git tag -a v1.1.0 a234sdf -m “tag on that commit hash”
```

<strong>Show information of the tag</strong>
```
git tag show v0.0.0
```

<strong>Add stash (stash code)</strong>
```
git stash
```

<strong>implement code from stash</strong>
```
git stash pop 
```

<strong>Add stash with message</strong>
```
git stash save “message for the stash”
```

<strong>IMPORTANT: Only use rebase if you haven’t pushed your code to a git provider</strong>

<strong>To “Squash” two commits into one</strong>
```
git rebase -i HEAD~3
squash 08asdf234 message of commit
```
<strong>git rebase reword (change name) number of heads</strong>

```
git rebase -i HEAD~3
```

<strong>git rebase edit (make two commits from one</strong>
```
git rebase -i HEAD~2
edit 12asd1234xscf1234
git add file1, git commit -m “message file1”
git add file2, git commit -m “message file2”git reset HEAD^
git rebase —continue
```
```
git push -u origin main
```
<br/>
"-u" sets the origin as default for later not have to do git push origin main 
git push knows that you are pushing to "origin" but still it's good practice
"origin" is the name of the repo ON GITHUB (**it's a standar but doesn't necesarily have to be origin**)
