---
layout:     post
title:      A simple configuration
date:       2014-12-04 22:11:00
summary:    
categories: 
published : true
---

I would like to have my PC used as a type-writer. It should be tough, simple and instrument for expression. However, ten years with Windows, I had a feeling I had spend more time fixing the computer rather than actually use it. At the end of spring 2013, I installed Linux on my Thinkpad Edge to be able to take advantage of high-speed LaTex compilation for my Actuary thesis. And it was a great experience. There are a lot of things to learn but without frustations. Since then, my way of using computer has radically changed. Today, I would like to mark down this way as a milestone for myself.

In this moment, I use Manjaro OS, a GNU-Linux distribution based on Arch Linux. My PCs are series T or S of the Thinkpad family since they're built to last. These can be easily found on the Ebay proposed by refurbish sellers for very reasonable price. Often have I occasion to setup Manjaro on my family members and friends. For them, I chose XFCE as the desktop environment because of its good balance of aesthetic and ressource. For my own, I would prefer a even simpler setup.

Manjaro Net Minimal Edition with :

* Windows manager : i3 
* Text editor : Vim
* File manager : Ranger
* Media player : mplayer, cmus, mpsyt 
* Web-browser : dwb
* Email : nmh or mutt. Mutt is easier to configurate
* Terminal : tmux with tmuximator, xfce4-terminal
* PDF reader : mupdf, evince

A list of minimalist programs could be found on suckless.org

For blogging, I use Jekyll to handle my blog on github. The posts are written in markdown format inside Vim

For Data analysis, I use R with Sublime Text 3 or Vim (with R plugin) within tmux.

# Basic PC controls within i3

Shutdown, sleep and hibernate via Terminal

* PC Shutdown : sudo poweroff
* PC reboot : sudo reboot
* Sleep : systemctl suspend
* Hibernate : systemctl hibernate

Basic i3 windows and panes controls: (I defined mod = Win touch)

* Vertial/Horizontal panes splits : mod + (v, h)
* Control panes layouts : mod + (w, s, e) 
* Move between panes : mod + (j, k)
* Switch windows : mod + [1..9]

# Email with nmh

Extra packages :

* For retrieving mails : getmail
* For sendmail : use msmtp

## Configurate mh_profile

'''
Path: Mail
Inbox : inbox
Editor: /usr/bin/vim
'''

## Configurate getmail
Nmh uses the mh mail format, which is different from the maildir and mbox. Setting your Path to a preexisting maildir folder, for example, will not work. We need to use rcvstore function of nmh.  Inside getmailrc file, modify [destination] part this way 

'''
[destination]
type = MDA_external
path = /usr/lib/nmh/rcvstore
arguments = ("+inbox",)
'''

To do: even set read_all=False, getmail redownload all the mails again. Maybe this command doesn't play well with rcvstore.

## Configurate mh_profile

'''
Path: Mail
Inbox : inbox
Editor: /usr/bin/vim
'''

## Configurate getmail
Nmh uses the mh mail format, which is different from the maildir and mbox. Setting your Path to a preexisting maildir folder, for example, will not work. We need to use rcvstore function of nmh.  Inside getmailrc file, modify [destination] part this way 

'''
[destination]
type = MDA_external
path = /usr/lib/nmh/rcvstore
arguments = ("+inbox",)
'''

To do: even set read_all=False, getmail redownload all the mails again. Maybe this command doesn't play well with rcvstore.

# Programming workflow 

Tools I use:

* Support : termite, tmux and tmuxinator
* Text editor : Vim
* Version control : Git





