### common git workflow to make a new feature

1. go to main or master branch `git checkout main`
2. pull latest changes `git pull`
3. create a new branch `git checkout -b <new_branch>`
4. make your changes
5. list the files that have been changed `git status`
6. add files to include in a commit `git add <path_to_file>` or add all files `git add .`
7. commit the added files `git commit -m "<commit_message>"`
8. push your new branch to remote `git push –set-upstream origin <new_branch>`

### resolve conflict with a rebase

1. got to main or master branch `git checkout main`
2. pull latest changes `git pull`
3. go to the branch with conflicts `git checkout <your_branch>`
4. start a rebase again main or master branche `git rebase main`
5. resolve conflicts
6. add all files to be commited `git add .`
7. continue rebase `git rebase --continue`
8. you may have to do multiple conflicts resolution, so just repeat step 5, 6 and 7
9. push your changes to remote `git push --force`

### revert a commit from remote

1. get commit hash `git log`
2. go to wanted commit `git checkout <commit_hash>`
3. reverte wanted commit `git revert <commit_hash>` this will create a new commit hash with changes reverted
4. push new commit to your branch `git branch <your_branch> <new_commit_hash>`
5. push your changes to remote `git push origin <your_branch>`
