1. make it able to run containers, not only images with --rm option.
I think this should be done in the following way:
• + option for a docker image: a container name
• + option for a settings section: whether to A) save a container and launch exitsing one on run; or B) create a new container with --rm key every time (is currently by default)

2. Fix a bug: when i execute `$p kek`, if the conf file is absent, it outputs an error, as it is intended. But if it is present but no "kek" entry in a config, then instead of an error it invokes a terminal that terminates immediately.

3. make a config file sections for docker images be like in git config:
```
[remote "heroku"]
	url = https://git.heroku.com/aqueous-plains-66613.git
	fetch = +refs/heads/*:refs/remotes/heroku/*
[remote "origin"]
	url = git@github.com:Kukuster/kukinterviewer.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
```

