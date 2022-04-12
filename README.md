# how-to-config-multiples-users-git

How to configure multiples user git in the same computer


Create three files

.gitconfig
.gitconfig-personal
.gitconfig-work
.gitconfig file [includeIf "gitdir:~/IdeaProjects/personal/"] path = /.gitconfig-personal [includeIf "gitdir:/IdeaProjects/renner/"] path = ~/.gitconfig-work

.gitconfig-personal [user] name = User Name email = User Email

[core] sshCommand = "ssh -i ~/.ssh/personal_id_rsa"

.gitconfig-work
[user] name = User Name email = User Email

[core] sshCommand = "ssh -i ~/.ssh/work_id_rsa"

Create SSH Key

Personal
ssh-key -f personal_id_rsa

Work
ssh-key -f work_id_rsa
