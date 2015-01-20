---
layout:     post
title:      Bash - personal memo
date:       2014-12-22 12:32:18
summary:    
categories: 
published : true
---

# Configurations

## Vi binding
There two steps to enable Vi binding inside the terminal

* Inside .bashrc, add this line : *set -o vi*
* Inside .inputrc, add this line : *set show-mode-in-prompt on*. If the file doesn't exist, create it with *touch* 

## Add PATH

use *export PATH ="[directory-name]:$PATH"*. 

For example, we add ruby compiler rbenv into PATH

{% highlight sh %} 
export PATH="home/.rbenv/bin:$PATH"
{% endhighlight  %} 

We can view the variable $PATH by *echo $PATH*

# Basic PC controls 

## With systemd 

PC shutdown/ sleep operations :

* Shutdown : systemctl poweroff 
* Reboot : systemctl reboot
* Sleep : systemctl suspend
* Hibernate : systemctl hibernate

At boot, several services are lauched automatically, to check this point 

{% highlight sh %} 
systemd-analyze
systemd-analyze blame
{% endhighlight  %} 

In my case, three services : **updatedb.service**, **man-db.service** and **bluetooth.service** took my x200s pretty much time so I deactivate them
  
{% highlight sh %} 
systemd-analyze disable updatedb.service man-db.service  bluetooth.service
{% highlight sh %} 

