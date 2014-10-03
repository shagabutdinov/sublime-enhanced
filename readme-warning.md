# Warnings

Please, read this section carefully before installation; otherwise you likely
won't be able to use sublime normally after installation.

Sublime enhanced provides replacements for default sublime actions (e.g.
navigation, search, goto line, save and other). Some of that replacements can
work in really unobvious way. Please read "warnings" sections in "readme" for
each package listed below carefully to avoid problems after installation:

- [FileDialog](http://github.com/shagabutdinov/sublime-file-dialog)
- [GotoLineEnhanced](http://github.com/shagabutdinov/sublime-goto-line-enhanced)
- [KeymapEnhanced](http://github.com/shagabutdinov/sublime-keymap-enhanced)
- [SearchPanelEnhanced](http://github.com/shagabutdinov/sublime-search-panel-enhanced)
- [SnippetCaller](http://github.com/shagabutdinov/sublime-snippet-caller)
- [StatusMessage](http://github.com/shagabutdinov/sublime-status-message)

Sublime enhanced remaps most of keyboard shortcuts so it will not play well if
you have custom keyboard shortcuts in your "User/Default ().sublime-keymap". It
will also not work properly if you have any plugins installed that bind
keyboard shortcuts. In this cases you have to manually resolve hotkeys conflicts
after installation by adding those hotkeys to "User/Default ().sublime-keymap".

Sublime enhanced is designed to improve code writing process but without getting
used to it keybinding it will be probably harder to write code at first. I
expect that time of adaptation to the replaced functions will be not more than
2-3 weeks.

Sublime enhanced is still in beta. That means that you can experience unexpected
behaviors of any plugin included to this package.