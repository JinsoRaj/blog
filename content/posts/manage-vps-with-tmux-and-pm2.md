---
title: "Run apps on VPS with tmux & pm2"
description: "Run apps on VPS with Tmux & Pm2"
date: 2023-03-25T12:48:20+05:30
draft: false

tags: ["test"]
categories: ["Tech"]
featuredImage: "/tmux.webp"
featuredImagePreview: "/tmux.webp"

toc:
  enable: true
  auto: true

---
---

## tmux


**What is tmux?**

Tmux is a terminal multiplexer an alternative to GNU Screen . In other words, it means that you can start a Tmux session and then open multiple windows inside that session. Each window occupies the entire screen and can be split into rectangular panes.

With Tmux you can easily switch between multiple programs in one terminal, detach them and reattach them to a different terminal.

**Tmux sessions are persistent, which means that programs running in Tmux will continue to run even if you get disconnected.**
All commands in Tmux start with a prefix, which by default is ctrl+b.

---



### Installing Tmux

On Ubuntu and Debian:

```bash
sudo apt install tmux
```

on macOS:

```bash
brew install tmux
```

### Creating Named Tmux Sessions

By default, Tmux sessions are named numerically. Named sessions are useful when you run multiple Tmux sessions. To create a new named session, run the tmux command with the following arguments:

tmux new -s session_name

### Detaching from Tmux Session

You can detach from the Tmux session and return to your normal shell by typing:

Ctrl+b d

The program running in the Tmux session will continue to run after you detach from the session.

### Re-attaching to Tmux Session

To attach to a session first, you need to find the name of the session. To get a list of the currently running sessions type:

tmux ls

The name of the session is the first column of the output.

0: 1 windows (created Sat Sep 15 09:38:43 2018) [158x35]
my_named_session: 1 windows (created Sat Sep 15 10:13:11 2018) [78x35]

As you can see from the output, there are two running Tmux sessions. The first one is named 0 and the second one my_named_session.

For example, to attach to session 0, you would type:

tmux attach-session -t 0


Credits: https://linuxize.com/post/getting-started-with-tmux/

## pm2

### test

hi
