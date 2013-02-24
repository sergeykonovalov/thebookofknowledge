---
layout: page
title: "Sublime Text 2"
description: ""
---
{% include JB/setup %}

## Hotkeys

**Select**

* `⌘ + D` – Select word
* `⌘ + L` – Select string
* `⌘ + Shift + A` – Select tag content
* `Control + Shift + M` – Select content between brackets or parentheses

**View**

* `⌘ + K, ⌘ + B` – Show-Hide sidebar
* `Shift + ⌘ + F` - Fullscreen
* `Control + Shift + ⌘ + F` - Distraction Free Mode

**Edit**

* `⌘ + Shift + D` — Duplicate line
* `⌘ + Shift + K` - Delete line
* `⌘ + ]` - Indent selection, `⌘ + [` - Unindent selection
* `⌘ + J` – Join lines
* `⌘ + Option + [` - Fold
* `⌘ + Option + ]` - Unfold
* `⌘ + K, ⌘ + T` - Fold tag attributes
* `⌘ + K, ⌘ + J` - Unfold all

**Tools**

* `Shift + ⌘ + P` – Sublime’s command palette
* ``Control + ` `` – Console
* `⌘ + Option + P` - Show source type

**Navigation**

* `⌘ + P` – Lightning-Fast File Switching
* `⌘ + P, #` – Go to word
* `⌘ + R` – Go to symbol (function or class)
* `Control + G` = `⌘ + P, :` - Go to line 
* `⌘ + F2` – Add bookmarks and use F2 to jump to the next one
* `⌘ + I` - Incremental find
* `⌘ + G` - Find next
* `⌘ + Shift + G` - Find previous

**Preferences**

* `⌘ + ,` – Settings - User

### Column Selection (OS X)

* Left Mouse Button + Option
* OR: Middle Mouse Button
* Add to selection: `⌘`
* Subtract from selection: `⌘ + Shift`


Using the Keyboard

* `Ctrl + Shift + Up`
* `Ctrl + Shift + Down`


To enable multi-selection, you have several options:

* Press `⌘` and then click in each region where you require a cursor.
* Select a block of lines, and then press `Shift + ⌘ + L`.
* Place the cursor over a particular word, and press `⌘ + D` repeatedly to select additional occurrences of that word.
* Alternatively, add an additional cursor at all occurrences of a word by typing `Alt + F3` on Windows, or `Ctrl + ⌘ + G` on the Mac.

## Packages

[Package Control](http://wbond.net/sublime_packages/package_control)

**Interface**

* [EvercodeSnippetPack](https://github.com/EvercodeLab/sublime2-snippets)
* [AllAutocomplete](https://github.com/alienhard/SublimeAllAutocomplete) 
* [BracketHighlighter](https://github.com/facelessuser/BracketHighlighter) [ Tip: [How to customize color](https://gist.github.com/JazzJackrabbit/5024243) ]
* [DetectSyntax](https://github.com/phillipkoebbe/DetectSyntax)
* [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements)
* [Theme - Aqua](https://github.com/cafarm/aqua-theme)

**Ruby**

* [RubyTest](https://github.com/maltize/sublime-text-2-ruby-tests)
* [RubyMarkers](https://github.com/mmims/sublime-text-2-ruby-markers)

**Web**

* [Emmet](https://github.com/sergeche/emmet-sublime)
* [CoffeeScript](https://github.com/Xavura/CoffeeScript-Sublime-Plugin)
* [js2coffee](https://github.com/nibblebot/sublime-js2coffee)
* [LiveReload](https://github.com/dz0ny/LiveReload-sublimetext2/tree/devel) [ Tip: Better use the version from `devel` branch. ]
* [Sass](https://github.com/nathos/sass-textmate-bundle)
* [SASS Build](https://github.com/jaumefontal/SASS-Build-SublimeText2)

**Utility**

* [Git](https://github.com/kemayo/sublime-text-2-git)

## Console

* view.settings().get('font_face') – get current value of setting using console
* Sublime Text 2 [includes a command line tool](http://www.sublimetext.com/docs/2/osx_command_line.html), subl, to work with files on the command line. 
* `ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl`


## Views

View > Layout – Different views

The most common are 
* `⌘ + Option + 1` - Single view
* `⌘ + Option + 2` - 2-column view

## Snippets

* [EvercodeSnippetPack](https://github.com/EvercodeLab/sublime2-snippets)
* [Initial snippet screencast](http://screencast.com/t/kBHOJFSoVmX8)
* [Sublime Text 2 Snippet for PHP getter and setter generation](http://akrabat.com/software/sublime-text-2-snippet-for-php-getter-and-setter-generation/)

## Links and Sources

* [Sublime Text 2 Documentation](http://www.sublimetext.com/docs/2/)
* [Sublime Text 2 Tips and Tricks (Updated)](http://net.tutsplus.com/tutorials/tools-and-tips/sublime-text-2-tips-and-tricks/)
* [The Definitive Guide: Sublime Text 2, a Code Editor to Love](http://designmodo.com/sublime-text-2/)
* <http://www.screencast.com/t/wXFuTAvDRg>
* [Sublime Text 2 – Useful Shortcuts (Mac OS X)](https://gist.github.com/1207002)
* [9 REASONS WHY SUBLIME TEXT 2 SHOULD BE YOUR NEXT IDE](http://www.trymbill.is/9-reasons-why-sublime-text-2-should-be-your-next-ide/)
* [Some things beginners might not know about Sublime Text](http://blog.alainmeier.com/post/27255145114/some-things-beginners-might-not-know-about-sublime-text)
* [Configuring Sublime Text 2](http://www.mutuallyhuman.com/blog/2012/10/18/configuring-sublime-text-2/)


## How to store config, packages and setting on github:

* <https://github.com/search?langOverride=&q=sublime+config&repo=&start_value=1&type=Repositories>
* <https://github.com/andres-torres-marroquin/my-sublime-config>
* <https://github.com/pahko/sublime-text-2-personal-config>
* <https://github.com/davidsansome/sublime-text-config/blob/master/.gitignore>


## Vintage mode

<http://www.sublimetext.com/docs/2/vintage.html>

