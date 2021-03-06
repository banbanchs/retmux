**retmux** README file

				  __
	   ________  / /_____ ___  __  ___  __
	  / ___/ _ \/ __/ __ `__ \/ / / / |/_/
	 / /  /  __/ /_/ / / / / / /_/ />  <  
	/_/   \___/\__/_/ /_/ /_/\__,_/_/|_|

		- A tmux session backup/reload tool

##Introduction
Tmux is very handy tool. However we cannot persist the sessions and reload them later. We want to restore our sessions in some situations. E.g. when we have to reboot the machine or we want to "clone" all sessions from a machine to another.

**retmux** comes to try to solve this problem. It makes tmux backup and restore easily to be done. You can manage your tmux backups with **retmux** and get your sessions back.

**retmux** was written and tested with:
- python 2.7.6
- tmux 1.8

##Features

- configurable options for (logging, ANSI escapes)
- (non- or) interactive operations (list/delete/restore/backup)
- highlighted output
- most important: tmux sessions backup and restore :) 

###What can be backuped/restored?
- **sessions** : with names, terminal-size
- **windows** : with name, order, pane split and split layout
- **panes**  : with path and content(up to 100000 line history content) with same look and feel (ANSI escapes)

###What would NOT be backuped/restored?
- the processes/programs running in window or pane at backup time
- the logined user, if the user is not same as the user who started tmux.(e.g. after `su`)
- command history in each window
- buffer stacks (could be done, but didn't see the need)

##Example & Screenshots & Demo

- `retmux -h` output
![help view](https://raw.github.com/sk1418/sharedResources/master/retmux/retmux_help.png)

- show detail of a tmux backup
![detail view](https://raw.github.com/sk1418/sharedResources/master/retmux/retmux_details.png)

##Installation

- for Archlinux user, `retmux` is available in AUR.
- for other users:

	sudo python setup.py install

##Usage

see the first screenshot in the `screenshots` section


% vim: nofoldenable

