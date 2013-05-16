# Sublime Text Configuration #

This is my personal sublime text configuration.

## Package Control - Sublime Text 2

**All** packages should be installed via [Package Control](http://wbond.net/sublime_packages/package_control). To install Package Control open Sublime Text 2 and press **ctrl + `** to open the console. Then enter the following command:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
```

Restart Sublime Text 2.

Now you can install packages by opening up the command palette with `ctrl/super + shift + p` and typing `inst` or something similar to find the `Package Control: Install Package` command.

## Package Control - Sublime Text 3

Check out the instructions on [this](http://wbond.net/sublime_packages/package_control/installation#ST3) page.

## Packages
**[Must-have Packages](#must_have_packages)**

i. [AdvancedNewFile](#advancednewfile)

ii. [Alignment](#alignment)

iii. [DocBlockr](#docblockr)

iv. [EasyMotion](#easymotion)

v. [Git](#git)

vi. [GitGutter](#gitgutter)

vii. [PlainTasks](#plaintasks)

viii. [SFTP](#sftp)

ix. [SideBarEnhancements](#sidebarenhancements)

x. [Solarized Color Scheme](#solarized_color_scheme)

xi. [SublimeLinter](#sublimelinter)

xii. [Theme - Phoenix](#theme_phoenix)

xiii. [VintageEX](#vintageex)

**[Web Design Packages](#webdesign_packages)**

i. [Color Highlighter](#color_highlighter)

ii. [ColorPicker](#colorpicker)

iii. [Emmet](#emmet)

iv. [Nettuts+ Fetch](#nettuts_fetch)

**[Optional / Language-specific Packages](#optional_language_specific_packages)**

i. [DashDoc](#dashdoc)

ii. [laravel-blade](#laravel_blade)

iii. [LaTeXTools](#latextools)

iv. [Markdown Preview](#markdown_preview)

v. [Rust](#rust)

vi. [Sass](#sass)

# <a name="must_have_packages"></a> Must-have Packages

These are the packages I consider to be essential for my development work.

## i. <a name="advancednewfile"></a> [AdvancedNewFile](https://github.com/skuroda/Sublime-AdvancedNewFile)

Easier file creation. Provides the shortcuts:

`super + alt +n`: create a new file at the specified path. You can autocomplete foldernames.

`super + shift + alt +n`: same as above but also creates an `__init__.py` file in new directories.

## ii. <a name="alignment"></a> [Alignment](https://github.com/wbond/sublime_alignment)

Attempts to align selected text with `super + alt + a`.

## iii. <a name="docblockr"></a> [DocBlockr](https://github.com/spadgos/sublime-jsdocs)

Makes it easy to create comment blocks for documentation.

Type `/**<enter>` or `/*<enter>`. Provides type hinting in PHP if it precedes a function declaration.

## iv. <a name="easymotion"></a> [EasyMotion](https://github.com/tednaleid/sublime-EasyMotion)

My favorite vim plugin recreated for Sublime Text.

`super + ;` followed by the character you want your cursor to jump to: type the corresponding label-character to move the cursor to that position.

## v. <a name="git"></a> [Git](https://github.com/kemayo/sublime-text-2-git)

Adds support for Git. You can optionally create keybindings to control the plugin but I find that using the command palette works well enough.

Examples:

`super + shift + p` and type `gad<enter>` to add the current file.

`super + shift + p` and type `gc<enter>` to commit.

Obviously requires a git repository to work.

## vi. <a name="gitgutter"></a> [GitGutter](https://github.com/jisaacks/GitGutter)

Adds a gutter to the editor which provides information about added/modified/removed lines.

Obviously requires a git repository to work.

## vii. <a name="plaintasks"></a> [PlainTasks](https://github.com/aziz/PlainTasks)

Formats your TODO files as checklists.

Adding a colon to words (like so `Front-end:`) creates headers.

`super + enter`: create a new task.

`super + d`: finish/unfinish a task.

You can add tags like so: `@tag`

## viii. <a name="sftp"></a> [SFTP](http://wbond.net/sublime_packages/sftp)

Manage FTP connections. Map local to remote folders. Allows for a [Coda](http://panic.com/coda)-like workflow. Extremely useful! It's usable without purchasing a license but I encourage you to support the author and buy one if you find that you're using this a lot.

## ix. <a name="sidebarenhancements"></a> [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements)

Expands sidebar options which are _very_ limited by default. Essential plugin.

## x. <a name="solarized_color_scheme"></a> [Solarized Color Scheme](https://github.com/SublimeColors/Solarized)

I've used a _lot_ of different color schemes in many different editors, but this one has stuck with me for almost a year now. Easy on the eyes and subtle colors. It has been [recreated](http://ethanschoonover.com/solarized) for lots of different text editors.

## xi. <a name="sublimelinter"></a> [SublimeLinter](https://github.com/SublimeLinter/SublimeLinter)

Adds syntax checking. Just install this and forget about it.

## xii. <a name="theme_phoenix"></a> [Theme - Phoenix](https://github.com/netatoo/phoenix-theme)

This plugin is optional but it makes the UI even more pleasing to look at. Changes tabs to look like [Coda](http://panic.com/coda)-tabs.

Add the following to your preferences if you're using a light colorscheme:

`"theme": "Phoenix Light.sublime-theme"`

or a dark colorscheme:

`"theme": "Phoenix Dark.sublime-theme"`

Additional color settings can be set e.g.:

`"phoenix_color_blue": true`

`"phoenix_highlight_current_tab": true`

and more.

## xiii. <a name="vintageex"></a> [VintageEX](https://github.com/SublimeText/VintageEx)

Allows you to enter EX commands like you would do in vim.

Some examples:

`:10m20`: move line 10 to line 20

`:10,30d`: delete line 10 to 30

`:10t20`: copy line 10 to 20

`:10t.`: copy line 10 to the current cursor position

`:10`: go to line 10

`:only`: close all other tabs

`:%s/foo/bar/g`: find and replace all instances of _foo_ with _bar_

And many more.

You need to have the Vintage package enabled and you need to be in command mode.

# <a name="web_design_packages"></a> Web Design Packages

These packages are useful for web design.

## i. <a name="color_highlighter"> [Color Highlighter](https://github.com/Monnoroch/ColorHighlighter)

Highlights hex code colors. Useful in CSS files.

## ii. <a name="colorpicker"> [ColorPicker](https://github.com/weslly/ColorPicker)

Pops up a handy color picker with `super + shift + c`.

## iii. <a name="emmet"> [Emmet](https://github.com/sergeche/emmet-sublime)

A toolkit for web developers. Evolved from Zen Coding. It is advised to disable all of the keybindings because some of them clash with default keybindings like `super + d/ctrl + d` (Expand selection to word) and `ctrl + e` (Move to EOL).

This is done by putting the following in your `Emmet.sublime-settings` file:

`"disabled_keymap_actions": "all"`

Then remap the keys you need to your own keybindings. For instance, I remapped the expand abbreviation keybinding to `ctrl + x` as follows (put this in your keybindings settings):

    {
        "keys": [
            "ctrl+x"
        ],
        "args": {
            "action": "expand_abbreviation"
        },
        "command": "run_emmet_action"
    }

Some examples of commands I often use:

`ul#nav>li*4>a<expand abbreviation>`

expands to

    <ul id="nav">
        <li><a href=""></a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
    </ul>

And intuitive CSS completions:

`p20<tab>` expands to `padding: 20px`

`db<tab>` expands to `display: block`

`fz<tab>` expands to `font-size:`

There's so much more Emmet can do; you should check out the [documentation](http://docs.emmet.io/) to learn about all of the features.

## iv. [Nettuts+ Fetch](https://github.com/weslly/Nettuts-Fetch)

Fetches packages or single files. Useful to quickly grab the latest version of [WordPress](http://www.wordpress.org), the [H5B](http://html5boilerplate.com/) etc.

# <a name="optional_language_specific_packages"></a> Optional / Language-specific Packages

These packages add functionality such as syntax highlighting, snippets and build systems for specific languages or tools.

## i. <a name="dashdoc"></a> [DashDoc](https://github.com/Kapeli/DashDoc)

Adds support for [DashDoc](http://kapeli.com/), a snippet manager and documentation browser.

Select text and press `ctrl + h` to search for it in DashDoc. Enable syntax sensitivy to search the appropriate documentation set.

## ii. <a name="laravel_blade"></a> [laravel-blade](https://github.com/Medalink/laravel-blade)

Syntax highlighting and some snippets for Laravel's Blade templating engine.

## iii. [LaTeXTools](https://github.com/SublimeText/LaTeXTools)

Snippets, build system, previewing. Essential if you use Sublime Text 2 for LaTeX.

## iv. [Markdown Preview](https://github.com/revolunet/sublimetext-markdown-preview)

Self-explanatory. Allows you to preview Markdown files. I'm using it right now to preview this file :)

For instance, `super + shift + p` and type `mpb<enter>` to preview in the browser.

## v. [Rust](https://github.com/dbp/sublime-rust)

Syntax highlighting, snippets, build system for Mozilla's programming language Rust.

## vi. [Sass](https://github.com/nathos/sass-textmate-bundle)

Syntax highlighting and snippets for SASS.
