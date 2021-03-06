# Sublime Text Configuration #

This is my sublime text configuration.

## Package Control

**All** packages should be installed via [Package Control](https://packagecontrol.io/).

Check out the instructions on [this](https://packagecontrol.io/installation) page.

## Packages
**[My packages](#my_packages)**

i. [AdvancedNewFile](#advancednewfile)

ii. [Babel](#babel)

iii. [BracketHighlighter](#brackethighlighter)

iv. [BufferScroll](#bufferscroll)

v. [Color Highlighter](#color_highlighter)

vi. [ColorPicker](#colorpicker)

vii. [DocBlockr](#docblockr)

viii. [EasyMotion](#easymotion)

ix. [Emmet](#emmet)

x. [Git](#git)

xi. [GitGutter](#gitgutter)

xii. [Laravel Blade Highlighter](#laravel_blade_highlighter)

xiii. [Markdown Preview](#markdown_preview)

xiv. [Material Theme](#material_theme)

xv. [Material Theme - Appbar](#material_theme_appbar)

xvi. [PHP Companion](#php_companion)

xvii. [phpfmt](#phpfmt)

xviii. [PlainTasks](#plaintasks)

xix. [rsub](#rsub)

xx. [Sass](#sass)

xxi. [SFTP](#sftp)

xxii. [SideBarEnhancements](#sidebarenhancements)

xxiii. [SublimeLinter](#sublimelinter)

xxiv. [SublimeLinter-php](#sublimelinter_php)

xxv. [Vintageous](#vintageous)

# <a name="my_packages"></a> My packages

These are the packages I consider to be essential for my development work.

## i. <a name="advancednewfile"></a> [AdvancedNewFile](https://github.com/skuroda/Sublime-AdvancedNewFile)

Easier file creation. Provides the shortcuts:

`super + alt +n`: create a new file at the specified path. You can autocomplete foldernames.

`super + shift + alt +n`: same as above but also creates an `__init__.py` file in new directories.

## ii. <a name="babel"></a> [Babel](https://github.com/babel/babel-sublime)

Adds support for ES6.

## iii. <a name="brackethighlighter"></a> [BracketHighlighter](https://github.com/facelessuser/BracketHighlighter)

Better bracket highlighting. Has come a long way since its first release. Install and forget.

## iv. <a name="bufferscroll"></a> [BufferScroll](https://github.com/SublimeText/BufferScroll)

Nifty little plug-in that remembers code foldings and cursor positions.

## v. <a name="color_highlighter"></a> [Color Highlighter](https://github.com/Monnoroch/ColorHighlighter)

Highlights colorcodes (e.g. #fff or rgba(0, 0, 0, 1)) with its actual color. Useful when writing CSS or Sass. Also includes a color picker.

## vi. <a name="colorpicker"></a> [Color Picker](https://github.com/weslly/ColorPicker)

Allows you to pick a color (`super + shift + c`) and insert the corresponding hex code.

## vii. <a name="docblockr"></a> [DocBlockr](https://github.com/spadgos/sublime-jsdocs)

Generate docblocks for various languages.

## viii. <a name="easymotion"></a> [EasyMotion](https://github.com/tednaleid/sublime-EasyMotion)

Sublime Text version of [Vim's EasyMotion](http://www.vim.org/scripts/script.php?script_id=3526). Press `super + ;` followed by the character you want to jump to then press the corresponding character to jump there.

## ix. <a name="emmet"></a> [Emmet](https://github.com/sergeche/emmet-sublime)

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

## x. <a name="git"></a> [Git](https://github.com/kemayo/sublime-text-2-git)

Adds support for Git. You can optionally create keybindings to control the plugin but I find that using the command palette works well enough.

Examples:

`super + shift + p` and type `gad<enter>` to add the current file.

`super + shift + p` and type `gc<enter>` to commit.

Obviously requires a git repository to work.

## xi. <a name="gitgutter"></a> [GitGutter](https://github.com/jisaacks/GitGutter)

Adds a gutter to the editor which provides information about added/modified/removed lines.

Obviously requires a git repository to work.

## xii. <a name="laravel_blade_highlighter"></a> [Laravel Blade Highlighter](https://github.com/Medalink/laravel-blade)

Syntax highlighting and some snippets for Laravel's Blade templating engine.

## xiii. <a name="markdown_preview"></a> [Markdown Preview](https://github.com/revolunet/sublimetext-markdown-preview)

Self-explanatory. Allows you to preview Markdown files. I'm using it right now to preview this file :)

For instance, `super + shift + p` and type `mpb<enter>` to preview in the browser.

## xiv. <a name="material_theme"></a> [Material Theme](https://github.com/equinusocio/material-theme)

Best theme available.

## xv. <a name="material_theme_appbar"></a> [Material Theme - Appbar](https://github.com/equinusocio/material-theme-appbar)

Nice colored appbar for the material theme.

## xvi. <a name="php_companion"></a> [PHP Companion](https://github.com/erichard/SublimePHPCompanion)

Adds useful functionality when working with PHP files.

For example, automatic use statements, auto implement, full class expansion and more.

## xvii. <a name="phpfmt"></a> [phpfmt](https://packagecontrol.io/packages/phpfmt)

Formats PHP code to PSR-2 (there are a lot more features, but this is mainly what I use it for).

## xviii. <a name="plaintasks"></a> [PlainTasks](https://github.com/aziz/PlainTasks)

Formats your TODO files as checklists.

Adding a colon to words (like so `Front-end:`) creates headers.

`super + enter`: create a new task.

`super + d`: finish/unfinish a task.

You can add tags like so: `@tag`

## xix. <a name="rsub"></a> [rsub](https://github.com/henrikpersson/rsub)

Allows you to edit remote files (needs [rmate](https://github.com/textmate/rmate) as well).

## xx. <a name="sass"></a> [Sass](https://github.com/nathos/sass-textmate-bundle)

Syntax highlighting and snippets for [Sass](http://sass-lang.com/).

## xxi. <a name="sftp"></a> [SFTP](http://wbond.net/sublime_packages/sftp)

Manage FTP connections. Map local to remote folders. Allows for a [Coda](http://panic.com/coda)-like workflow. Extremely useful! You are required to buy a license if you want to get rid of the popups, but it's worth it in my opinion. Alternatively you can look at [FTPSync](https://github.com/NoxArt/SublimeText2-FTPSync), (doesn't support SFTP).

## xxii. <a name="sidebarenhancements"></a> [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements)

Expands sidebar options which are _very_ limited by default. Essential plugin.

## xxiii. <a name="sublimelinter"></a> [Sublime Linter](https://github.com/SublimeLinter/SublimeLinter3)

Framework that allows you to install linters for various languages.

## xxiv. <a name="sublimelinter_php"></a> [Sublime Linter PHP](https://github.com/SublimeLinter/SublimeLinter-php)

PHP linter.

## xxv. <a name="vintageous"></a> [Vintageous](https://github.com/guillermooo/Vintageous)

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
