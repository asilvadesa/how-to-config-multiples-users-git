Create three files

- .gitconfig
- .gitconfig-personal
- .gitconfig-work


1) .gitconfig file
[includeIf "gitdir:~/IdeaProjects/personal/"]
  path = ~/.gitconfig-personal
[includeIf "gitdir:~/IdeaProjects/renner/"]
  path = ~/.gitconfig-work


2) .gitconfig-personal
[user]
	name = User Name
	email = User Email

[core]
  sshCommand = "ssh -i ~/.ssh/personal_id_rsa"


3) .gitconfig-work

[user]
	name = User Name
	email = User Email

[core]
  sshCommand = "ssh -i ~/.ssh/work_id_rsa"


Create SSH Key

1) Personal 

ssh-key -f personal_id_rsa

2) Work

ssh-key -f work_id_rsa
