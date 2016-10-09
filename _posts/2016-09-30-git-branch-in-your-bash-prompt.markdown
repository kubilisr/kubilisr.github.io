--- 
layout: post
title:  "Git branch in your bash prompt"
datetime:   2016-09-30 23:59:59
categories: git bash prompt branch
disqus: true
bio: false
---

Today while googling for answers to question 'How to check if Git is installed from bash' stumbled upon this stackoverflow question [How to check if Git is installed from .bashrc](http://stackoverflow.com/questions/7292584/how-to-check-if-git-is-installed-from-bashrc){:target="_blank"}. Having branch name in your bash prompt seems like a great idea especially if you are using git all the time. Recently I have been using git for my personal projects, from time to time I issue command  
```
git status
```  
just to check what branch I am on. I immediately started questioning myself where does this __git_ps1 come from, some more googling unearthed this article [Configuring Git](http://effectif.com/git/config){:target="_blank"}, which mentions that __git_ps1 becomes available after you install git. Kinda makes sense, but still does not answer where it is coming from. After more searching I came across this git related thread - [bash-completion now loads completions dynamically, so __git_ps1 is not defined when you open a shell](http://git.661346.n2.nabble.com/bash-completion-now-loads-completions-dynamically-so-git-ps1-is-not-defined-when-you-open-a-shell-td7415323.html){:target="_blank"}. After all __git_ps1 is an extension to bash completion that you can find here  
```
/usr/lib/git-core/git-sh-prompt
```  
found it while reading - [An introduction to bash completion: part 1](https://debian-administration.org/article/316/An_introduction_to_bash_completion_part_1){:target="_blank"} from [Debian Administration - Debian Administration Resources](https://debian-administration.org){:target="_blank"} which is a great resource on this topic and on Debian administration in general, for me bash completion is not completely new concept, but I have not ever thought about adding any extensions to be honest. 
