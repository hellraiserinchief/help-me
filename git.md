[Rebase forked repo with original repo](https://medium.com/@topspinj/how-to-git-rebase-into-a-forked-repo-c9f05e821c8a)
1. `git remote add upstream https://github.com/original-repo/goes-here.git`
1. `git fetch upstream`
1. `git rebase upstream/master`
1. `git push origin master [--force]`
