---
layout: page
title: "Git"
description: ""
---
{% include JB/setup %}

# Полезные ресурсы

* [Main site about git](http://git-scm.com/)
* [github:help](https://help.github.com/)
* [A Visual Git Reference](http://marklodato.github.com/visual-git-guide/index-en.html)
* [Git Is Simpler Than You Think](http://nfarina.com/post/9868516270/git-is-simpler)
* [git - the simple guide](http://rogerdudler.github.com/git-guide/)
* [A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
* [Some more git tips — just one a time](http://gitready.com/)
* [GitCasts](http://gitcasts.com/)
* [Think Like (a) Git](http://think-like-a-git.net/)

# Issues

Мы активно используем github:issues. По любым вопросам по задаче можно и нужно писать в комментариях. На все репозитории включены хуки, которые на любой чих кидает оповещение в групповой чатег (hipchat).

# Cообщения к коммитам. 

Github позволяет легко подвязывать коммиты к задачам. Очень удобная тема. Для этого достаточно указывать номер задачи в сообщении коммита. Мы пишем "Update #52: ..." если код относится к задаче и "Fix #52: ...", если код завершает выполнение задачи, при этом на Fix github автоматом закроет задачу.

Сообщения в коммитах, как и любые комментарии в коде надо писать на английском языке.

# Workflow

Источник: [http://blog.evercodelab.com/git-workflow](http://blog.evercodelab.com/git-workflow)

## Simple

{% highlight bash %}
git pull

# http://programming-motherfucker.com/
Programming, Motherfucker!

# if some problems appear and you need to fix it and push
git stash

# Fix the bug, Motherfucker!

git commit -a -m "Sector clear. Problem resolved."
git push
git stash pop

# http://programming-motherfucker.com/
Programming again, Motherfucker!

git commit -a -m "Here I describe what I did"
git push
{% endhighlight %}


## General

{% highlight bash %}
git clone … # клонируем репо  
git checkout -b local # создаем локальную ветку с именем "local" от текущего состояния master и переключаемся на эту ветку  
…
programming mother fucker!!!  
…  
git status # проверяем, что мы в ветке local  
git add . # добавляем все новые файлы к коммиту  
git commit -m "Update #13: descriptive commit message" # коммитим новые файлы в local  
git checkout master # переключаемся на dev  
git pull # сливаем обновления с удаленного репо, если кто-то что-то там еще напрограммил  
git checkout local  
git rebase master # делаем так, чтобы локальные коммиты накатились поверх тех, что слили из master  
git checkout master  
git merge local # мерджим свои коммиты в master  
git push # отправляем код на github  
{% endhighlight %}

## Advanced

* http://nvie.com/posts/a-successful-git-branching-model/
* https://github.com/nvie/gitflow
* http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/

{% highlight bash %}
# Feature branches

git checkout -b myfeature develop

git checkout develop
git merge --no-ff myfeature
git branch -d myfeature
git push origin develop

# The --no-ff flag causes the merge to always create a new commit object, 
# even if the merge could be performed with a fast-forward. 
# This avoids losing information about the historical existence of a
# feature branch and groups together all commits that together added the feature. 


# Release branches

git checkout -b release-1.2 develop
# changes to bump the version
git commit -a -m "Bumped version number to 1.2"

git checkout master
git merge --no-ff release-1.2
git tag -a 1.2

git checkout develop
git merge --no-ff release-1.2

git branch -d release-1.2


# Hotfix branches

git checkout -b hotfix-1.2.1 master
# changes to bump the version
git commit -a -m "Bumped version number to 1.2.1"
# fix the bug
git commit -m "Fixed severe production problem"


git checkout master
git merge --no-ff hotfix-1.2.1
git tag -a 1.2.1

git checkout develop
git merge --no-ff hotfix-1.2.1

git branch -d hotfix-1.2.1
{% endhighlight %}

