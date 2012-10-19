---
layout: page
title: "PHPstorm"
description: ""
---
{% include JB/setup %}


## Themes

* Monokai theme
* <http://cordoval.github.com/Symfony2Colors/>

## Hotkeys

* `⌘ + 1` - show/hide Project panel
* `⌘ + 7` - show/hide Structure panel
* `⌘ + Shift + V` - paste from history
* `⌘ + Shift + N` - go to file (can use wildcards; pre-filter by filetype)
* `⌘ + N` - go to class
* `⌘ + E` – recent files
* `⌘ + Shift + X` - Command Line Tools Console
* `⌘ + B` – go to declaration
* `⌘ + Alt + ←` - go back from declaration
* `⌘ + U` – go to super-method/super-class


## Settings

* Right margin (columns): 80
* PHP -> Blank Lines - After class header - 1
* Before '}' - 1
* Command Line Tool Support –> Symfony2 (path to app/console) -> `⌘ + Shift + X`
* Inspections
* PHP - Usage of Silence operator
* PHP - Interpreters
* Include Path (not preferable, composer dependancies are better)
* Transparent mode for floating windows
* PHP Class Diagrams
* Recent File Limits - 50
* Console command history size - 50
* Surround selection on typing quote or brace
* Use block caret
* Show line numbers/method separators/whitespaces
* Show tabs in single row
* Hide file extensions on editor tabs
* Show directory in editor tabs for non-unique filenames
* Mark modified tabs with asterisk
* Show tool window bars - uncheck
* File templates


## Auto-complete tip

{% highlight php5 linenos %}
$request = $this->get('request');

/** @var  \Symfony\Component\HttpFoundation\Request $request */ 
{% endhighlight %}


## Plugins

* [IdeaVIM](http://plugins.jetbrains.net/plugin/?webide&id=164)
* [TabSwitch](http://plugins.jetbrains.net/plugin/?webide&id=179)

## Reformatting code

`⌘ + Alt + L` – Очень удобное, когда приходится иметь дело с плохо форматированным кодом: <http://www.jetbrains.com/phpstorm/webhelp/reformatting-source-code.html>


## Links

* [PhpStorm Docs & Demos](http://www.jetbrains.com/phpstorm/documentation/index.html)
* [Exporting and Importing Settings](http://www.jetbrains.com/phpstorm/webhelp/exporting-and-importing-settings.html)
* [Project and IDE Settings](http://www.jetbrains.com/phpstorm/webhelp/project-and-ide-settings.html)
* [Programmer Productivity: Emacs versus IntelliJ IDEA](http://henrikwarne.com/2012/06/17/programmer-productivity-emacs-versus-intellij-idea/)
* [Полезные плагины для PhpStorm](http://rmcreative.ru/blog/post/poleznye-plaginy-dlja-phpstorm)

## Хранение настроек на GitHub

* <https://github.com/search?q=phpstorm+config&type=Everything&repo=&langOverride=&start_value=1>
* <https://github.com/search?q=phpstorm+settings&repo=&langOverride=&start_value=1&type=Everything&language=>
* <https://github.com/memphys/phpstorm-settings>
