# SublimeEnhanced

**Deprecation notice: I've migrated to the vscode a while ago (due to better support of the language servers) and dropped the support for sublime packages. It was a good time spent with sublime but unfortunately, it's over. Feel free to reach out if you want to take over the maintenance of one (or more) of the plugins. Thanks!**

Set of plugins for beloved sublime text editor.

This set of plugins were designed for 3 purposes:

  1. Mouseless usage of sublime
  2. Navigation (in code and files) improvement
  2. Common micro-tasks automation

For most people it will be convinient to cherry-pick one or two packages of
sublime-enhanced that will be useful for them. If you feel like hacker and have
a free day you can try full installation.


### Quick demos


##### [sublime-method](https://github.com/shagabutdinov/sublime-method)

![Demo](https://github.com/shagabutdinov/sublime-enhanced-demos/raw/master/method.gif "Demo")


##### [sublime-local-variable](https://github.com/shagabutdinov/sublime-local-variable)

![Demo](https://github.com/shagabutdinov/sublime-enhanced-demos/raw/master/local_variable.gif "Demo")


##### [sublime-join-assignment](https://github.com/shagabutdinov/sublime-join-assignment)

![Demo](https://github.com/shagabutdinov/sublime-enhanced-demos/raw/master/join_assignment.gif "Demo")


### Default keybinding activation

Keymaps listed in readmes are disabled by default. You should add next line to your
"User/Preferences.sublime-settings" file ("Preferences: Settings - User" in command
palette) to enable those keybindings.

```
"sublime_enhanced_keybindings": true,
```


### WARNING

Please read [readme-warning.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-warning.md),
[readme-usage.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-usage.md),
and [readme-keymap.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-keymap.md)
before full installation. Sublime-enhanced has a lot of unobvious behavior and
keyboard shortcuts that replace default sublime's behavior which is partially covered by these files.


You also can help the project by opening pull requests or issues, or by watching/staring plugins you like.


### Installation

* for full installation read [readme-installation.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-installation.md)
  file

* for cherry-pick installation:
  * install package dependencies (listed in each package in "Dependencies
    sections") if any
  * open command palette
  * type "install package"
  * enter package name
  * hit "enter"
  * wait


### Usage

In order to find out how to use sublime after sublime-enhanced installation
refer to [readme-usage.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-usage.md)
and [readme-keymap.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-keymap.md)


### Plugins to start with

* [Autocompletion](https://github.com/shagabutdinov/sublime-autocompletion)
* [DevastateMini](https://github.com/shagabutdinov/sublime-devastate-mini)
* [Expression](https://github.com/shagabutdinov/sublime-expression)
* [FileDialog](https://github.com/shagabutdinov/sublime-file-dialog)
* [GotoCharacter](https://github.com/shagabutdinov/sublime-goto-character)
* [GotoLastEditEnhanced](https://github.com/shagabutdinov/sublime-goto-last-edit-enhanced)
* [GotoLineEnhanced](https://github.com/shagabutdinov/sublime-goto-line-enhanced)
* [IndentationNavigation](https://github.com/shagabutdinov/sublime-indentation-navigation)
* [KeymapEnhanced](https://github.com/shagabutdinov/sublime-keymap-enhanced)
* [Keyword](https://github.com/shagabutdinov/sublime-keyword)
* [LocalVariable](https://github.com/shagabutdinov/sublime-local-variable)
* [Method](https://github.com/shagabutdinov/sublime-method)
* [ProjectFiles](https://github.com/shagabutdinov/sublime-project-files)
* [SearchPanelEnhanced](https://github.com/shagabutdinov/sublime-search-panel-enhanced)
* [SnippetCaller](https://github.com/shagabutdinov/sublime-snippet-caller) and
  [SnippetManager](https://github.com/shagabutdinov/sublime-snippet-manager)
* [Statement](https://github.com/shagabutdinov/sublime-statement)
* [StatusMessage](https://github.com/shagabutdinov/sublime-status-message) and
  [ShellStatus](https://github.com/shagabutdinov/sublime-shell-status)
* [ToggleWrap](https://github.com/shagabutdinov/sublime-toggle-wrap)


### Information reference

* Warnings that should be read before installation: [readme-warning.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-warning.md)

* Complete plugins list: [readme-list.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-list.md)

* A bit of explanations of sublime-enhanced: [readme-philosophy.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-philosophy.md)

* Main usecases overview: [readme-usage.md](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-usage.md)

* Full keymap (in order to read it, clone this repo and open file
  "readme-keymap.html" in browser - full keymap was too large to put it in
  markdown): [readme-keymap.html](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-keymap.html)


### License

[The MIT license](https://github.com/shagabutdinov/sublime-enhanced/blob/master/readme-license.md)


### Todo

Packages that I want todo in future:

* KeymapConverter (convert your keymap to different locale to use keybindings
  when keyboard are switched to different locale)

* InsertSnippetEnhanced (snippets with multicursors)

* HtmlNavigation (goto into/out/over tag, append/detach tag to selection, select
  in tag or tag definition)
