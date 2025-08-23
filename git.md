[Rebase forked repo with original repo](https://medium.com/@topspinj/how-to-git-rebase-into-a-forked-repo-c9f05e821c8a)
1. `git remote add upstream https://github.com/original-repo/goes-here.git`
1. `git fetch upstream`
1. `git rebase upstream/master`
1. `git push origin master [--force]`


Add ssh key to account  
1. `ssh-keygen -t ed25519 -C "your_email@example.com"`
2. `cat ~/.ssh/id_ed25519.pub`
3. Log in to your GitHub account, navigate to "Settings" -> "SSH and GPG keys", and add a new SSH key, pasting the copied public key content.
