# Sublime Text Configuration #

This is my personal sublime text configuration.

## Package Control

**All** packages should be installed via [Package Control](http://wbond.net/sublime_packages/package_control).

Check out the instructions on [this](https://sublime.wbond.net/installation) page.

## Packages
**[Must-have Packages](#must_have_packages)**

i. [AdvancedNewFile](#advancednewfile)

ii. [BracketHighlighter](#brackethighlighter)

iii. [FTPSync](#ftpsync)

iv. [Git](#git)

v. [GitGutter](#gitgutter)

vi. [PlainTasks](#plaintasks)

vii. [SideBarEnhancements](#sidebarenhancements)

viii. [Theme - Spacegray](#theme_spacegray)

ix. [Vintageous](#vintageous)

**[Web Design Packages](#webdesign_packages)**

i. [ColorPicker](#colorpicker)

ii. [Emmet](#emmet)

**[Optional / Language-specific Packages](#optional_language_specific_packages)**

i. [laravel-blade](#laravel_blade)

ii. [LaTeXTools](#latextools)

iii. [Markdown Preview](#markdown_preview)

iv. [Sass](#sass)

# <a name="must_have_packages"></a> Must-have Packages

These are the packages I consider to be essential for my development work.

## i. <a name="advancednewfile"></a> [AdvancedNewFile](https://github.com/skuroda/Sublime-AdvancedNewFile)

Easier file creation. Provides the shortcuts:

`super + alt +n`: create a new file at the specified path. You can autocomplete foldernames.

`super + shift + alt +n`: same as above but also creates an `__init__.py` file in new directories.

## ii. <a name="brackethighlighter"></a> [BracketHighlighter](https://github.com/facelessuser/BracketHighlighter)

Better bracket highlighting. Has come a long way since its first release. Install and forget.

## iii. <a name="ftpsync"></a> [FTPSync](https://github.com/NoxArt/SublimeText2-FTPSync)

Manage FTP connections. Map local to remote folders. Allows for a [Coda](http://panic.com/coda)-like workflow. Extremely useful!

## iv. <a name="git"></a> [Git](https://github.com/kemayo/sublime-text-2-git)

Adds support for Git. You can optionally create keybindings to control the plugin but I find that using the command palette works well enough.

Examples:

`super + shift + p` and type `gad<enter>` to add the current file.

`super + shift + p` and type `gc<enter>` to commit.

Obviously requires a git repository to work.

## v. <a name="gitgutter"></a> [GitGutter](https://github.com/jisaacks/GitGutter)

Adds a gutter to the editor which provides information about added/modified/removed lines.

Obviously requires a git repository to work.

## vi. <a name="plaintasks"></a> [PlainTasks](https://github.com/aziz/PlainTasks)

Formats your TODO files as checklists.

Adding a colon to words (like so `Front-end:`) creates headers.

`super + enter`: create a new task.

`super + d`: finish/unfinish a task.

You can add tags like so: `@tag`

## vii. <a name="sidebarenhancements"></a> [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements)

Expands sidebar options which are _very_ limited by default. Essential plugin.

## viii. <a name="theme_spacegray"></a> [Spacegray Theme](https://github.com/kkga/spacegray)

Optional; but this is my favorite theme of the moment. I use the dark variant with the dark ocean colorscheme.

## ix. <a name="vintageous"></a> [Vintageous](https://github.com/guillermooo/Vintageous)

Awesome plugin. Makes the already powerful vintage mode even better. Adds support for EX commands.

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

## i. <a name="colorpicker"> [ColorPicker](https://github.com/weslly/ColorPicker)

Pops up a handy color picker with `super + shift + c`.

## ii. <a name="emmet"> [Emmet](https://github.com/sergeche/emmet-sublime)

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

# <a name="optional_language_specific_packages"></a> Optional / Language-specific Packages

These packages add functionality such as syntax highlighting, snippets and build systems for specific languages or tools.

## i. <a name="laravel_blade"></a> [laravel-blade](https://github.com/Medalink/laravel-blade)

Syntax highlighting and some snippets for Laravel's Blade templating engine.

## ii. [LaTeXTools](https://github.com/SublimeText/LaTeXTools)

Snippets, build system, previewing. Essential if you use Sublime Text for LaTeX.

## iii. [Markdown Preview](https://github.com/revolunet/sublimetext-markdown-preview)

Self-explanatory. Allows you to preview Markdown files. I'm using it right now to preview this file :)

For instance, `super + shift + p` and type `mpb<enter>` to preview in the browser.

## iv. [Sass](https://github.com/nathos/sass-textmate-bundle)

Syntax highlighting and snippets for SASS.
