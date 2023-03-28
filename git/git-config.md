## My Git Config file

```sh
[alias]
	lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
	cm = commit -m
	co = checkout
	st = status
	hard = reset --hard
	amend = commit --amend
        cc = shortlog -sn --all
[user]
	email = alvaro.freirea@udc.es
	name = Álvaro Freire
[commit]
	gpgSign = true
[pull]
        rebase = true
[init]
        defaultBranch = main
```
