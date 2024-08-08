# GitCommands


Checkout a new branch named bugfix:
git checkout -b bugfix

Commit once:
git commit

Go back to main and commit again:
git checkout main

Check out bugFix again and rebase onto main:
git checkout bugFix\n
git rebase main

detach HEAD from main and attach it to the commit instead:
HEAD -> main -> C1\n
git checkout C1\n
HEAD -> C1\n

detach HEAD from bugFix and attach it to the commit instead:
git checkout C4

check out the parent commit of bugFix. This will detach HEAD:
git checkout C3

move HEAD, main, and bugFix to their goal destinations shown:
git branch -f main HEAD\n
git checkout bugFix\n
git checkout C1\n
git branch -f bugFix HEAD~3\n

reverse the most recent commit on both local and pushed. You will revert two commits total (one per branch).
git reset HEAD~1
git checkout pushed
git revert HEAD

