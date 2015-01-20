---
layout:     post
title:      tmux - personal memo
date:       2014-12-22 12:32:18
summary:    
categories: 
published : true
---

# Configure tmux after installation

* Download .tmux.conf from https://pragprog.com/titles/bhtmux/source-code, choose the version inside the folder *code/config/*
* tmux doesn't recognize vim colorsheme, because it call just *xterm*. To solve this, add *alias tmux="TERM=screen-256color-bce tmux"* and *alias mux="TERM=screen-256color-bce mux"* insi de .bashrc
* Install tmuxinator from AUR or from gem to set up preconfigurate layout 

# Basic commands

Create new session : mux new  [session-name]

Open a session : mux [session-name]

Kill a session : tmux kill-session -t [session-name]

# Work with tmux

* Switch windows : Ctrl+a then (n, p, [1..9])
* Swith panes : Ctrl+q then hjkl


 
 
