# GitCommands


Checkout a new branch named bugfix:
git checkout -b bugfix

Commit once:
git commit

Go back to main and commit again:
git checkout main

Check out bugFix again and rebase onto main:
git checkout bugFix
git rebase main

detach HEAD from main and attach it to the commit instead:
HEAD -> main -> C1
git checkout C1
HEAD -> C1

detach HEAD from bugFix and attach it to the commit instead:
git checkout C4

check out the parent commit of bugFix. This will detach HEAD:
git checkout C3

move HEAD, main, and bugFix to their goal destinations shown:
git branch -f main HEAD
git checkout bugFix
git checkout C1
git branch -f bugFix HEAD~3

reverse the most recent commit on both local and pushed. You will revert two commits total (one per branch).
git reset HEAD~1
git checkout pushed
git revert HEAD

