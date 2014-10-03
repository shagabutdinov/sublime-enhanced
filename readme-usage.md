# Usage

This section covers major usecases and gives overview of sublime-enhanced.
However it is better to read documentation to each plugin.


### Usage: Quick start

This section describes basic keyboard rebindings.

1. Move cursor by character: "alt+i/j/k/l" (up/left/down/right), "+shift" for select
2. Move cursor by word: "alt+ctrl+i/j/k/l", "+shift" for select
3. Delete forward: "alt+/" (character), "alt+ctrl+/" (word)
4. Goto start/end of line: "alt+'"", "+shift" for select
5. Goto start/end of file: "alt+ctrl+'"", "+shift" for select
6. Scroll: "cltr+alt+i/j"
7. Undo/redo: "ctrl+z" (default), "ctrl+r" (rebinded)
8. Save/save as: "ctrl+s", "ctrl+shift+s;", enter name of file, hit "tab";
   "ctrl+u, ctrl+s" (save), "ctrl+u, s" (save as) for default dialog.
9. Open file: "ctrl+u, ctrl+o" (enhanced), "ctrl+u, o" (default)
10. Goto line: "ctrl+g" (default), enter line number (you can use "nm,.jkluio"
    key for entering numbers from 0 to 9 accordingly), hit "tab"
11. Next/previous tab: "ctrl+.,"
12. Command palette: "alt+\"
13. Goto anything: "f1"
14. Goto method: "f2"
15. Search: ctrl+f (default), alt+f/alt+shift+f (next, previous result)
16. Search in files: "ctrl+u, ctrl+f"
17. Open terminal: "f12" (project folder), "ctrl+f12" (current folder) if you
    have "Terminal" plugin installed
18. New file: "ctrl+shift+n"
19. New window: "ctrl+u, ctrl+n"
20. Comment: "ctrl+q" (line), "ctrl+shift+q" (block)
21. Paste: "ctrl+v" (smart), "ctrl+shift+v" (default)

While opening or saving files in quick search panel:

- "enter" for opening folders
- "ctrl+alt+ik" - goto folder up/down;
- "cltr+n" for new folder
- "tab" for explicit open of file

For other keyboard shortcuts refer to "readme-keymap.html".


### Usage: Files navigation

This section contains a description of ways to open a file. Each way of opening
file are required to certain situation so it is advised to study all ways to
open file and use the right one according to situation.


##### Projects

To quickly access files it is highly recommended to use sublime's default
projects features.

- To setup a project, open folder ("ctrl+u, \" keyboard shortcut).

- Then save opened folder as project ("ctrl+u, a" keyboard shortcut).

- Then you can switch between project using fuzzy search ("ctrl+u, ctrl+p"
  keyboard shortcut)


##### Project setup

You should explicitly tell sublime which files are as part of your project and
which are not. To do it, hit "ctrl+u, p" then add "file_exclude_patterns" and
"folder_exclude_patterns" to each folder under "folders" key. Example project
configuration:

  ```
  {
    "folders": [
      {
        "follow_symlinks": true,
        "path": "/home/leo/projects/myproject",
        "file_exclude_patterns": [
          "*.data",
          "*.min.js"
        ],
        "folder_exclude_patterns": [
          "vendor/",
          "assets/"
        ]
      }
    ]
  }
  ```


##### Goto anything

Primary file navigation tool is "goto anything..." that are mapped under "f1".
It's default sublime's tool that are extended a bit by "goto-anything-enhanced"
plugin. This tool provides ability to quickly open any file using fuzzy search.
This feature should be used in the case if file name is known prior to manual
file system navigation.


##### Goto anything by predefined regexp

It allows to predefine sets of files that can be later accessed by keyboard
shortcuts. For example, it allows use (/controller/|_controller.\w+$) to access
all controllers in project using fuzzy search (mapped under "ctrl+n, ctrl+c").
This functionality are provided by "sublime-project-files" plugin.

When accessing a file that belongs to set that could be specified with regexp,
this functionality should be used prior to "goto anything" because it makes
fuzzy search more deterministic (e.g. it is easier to use fuzzy search over 30
controllers then over 3000 files of project).

By default there a lot of mappings to accessing different file sets. Refer to
"sublime-project-files" documentation to be able to use this plugin.


##### Goto definition

It allows you to jump to the definition of class or method (mapped under
"ctrl+e"). This is extremely useful when studying source code of libraries or
colleagues commits. This is default sublime functionality that changed a bit by
"sublime-goto-definition-enhanced". Refer to this plugin documentation to be
able to use it correctly.


##### Search in files

Default sublime feature that are mapped under ("ctrl+u, ctrl+f"). Allows to find
file that contains entered text or regexp. Extremely useful when you don't know
file name but know a text that this file contains.

Sublime-enhanced provides ability to navigate thorugh search results using
"goto search next result" (alt+enter), "goto previous search result"
(alt+shift+enter) features of glorious "sublime-expression" plugin and
"open search result" (ctrl+enter) of "OpenSearchResult" plugin.


##### Filesystem browsing

With sublime-enhanced there are two ways to open a folder using file system
browsing:

- Default's sublime "promt open file" (mapped under "ctrl+u, o") which use OS's
  default "open file" dialog. It allows to open several files at once.

- Plugin-driven navigation provided by "sublime-file-dialog" (mapped under
  "ctrl+u, cltr+o") which allows to use fuzzy completions and keyboard shortcuts
  to navigate through files. Refer to "sublime-file-dialog" documentation to
  be able to use this tool.

This feature should be used if you want to open a file in directory of currently
opened file. In other cases use this feature as last resort when opening files.


##### Using terminal

You can fallback to command line (mapped under "f12" or "ctrl+f12") to open
file using terminal features and "subl" command (e.g. "subl readme.md"). This is
handy when your are shell ninja.


##### Accessing opened files

"ctrl+,", "ctrl+." ("ctrl+tab", "ctrl+shift+tab" is also can be used) is for goto
previous/next tab. "ctrl+&lt;number&gt;" is for accessing tab by number (number
from 1 to 5). Tab can be moved backward/forward with "ctrl+shift+.",
"ctrl+shift+,".


##### Closing tabs

Basic "close tab" mapped under "ctrl+u, ctrl+l" and "ctrl+f4" hotkeys (double
mapping). "Close other files except current" mapped under "ctrl+u, l". "Close
all to right", "Close all" mapped under "ctrl+u, ctrl+;" and "ctrl+u, ;"
accordigly.


##### Important note

Note that according to sublime-enhanced philosophy, mouse should not be used to
open files under any circumstances. So sidebar file opening or main menu file
opening are highly unadvisable but still avaiable under "toggle sidebar"
(ctrl+u, ctrl+a) and "toggle menu" (ctrl+u, ctrl+m).


### Usage: Block navigation

This section describes the ways to quickly jump over parts of file
(blocks of code) when jumping over more than 5 lines needed. Each way of block
navigation should be studied carefully and used according to situation.


##### Goto start/end of file

Defaults sublimes functionality, mapped under "alt+ctrl+'", "alt+ctrl+;". Select
to start/end of file mapped under "alt+ctrl+shift+'", "alt+ctrl+shift+;".


##### Goto method

Goto method is primary navigation tool (mapped under "f2") when working with
source files that contains lists of functions/methods. This is default sublime
feature.

Sublime-enhanced also adds "goto next method" ("alt+n"), "goto previous method"
("alt+shift+n") and "toggle method start/end" ("ctrl+alt+n") features that are
provided by glorious "sublime-method" plugin.


##### Goto line

Provided by "sublime-goto-line-enhanced" and differs a bit from default "goto
line" feature. Mapped under "ctrl+g". Very useful when working with exception
or in pair programming when the number of line referred by somebody else. Refer
to plugin documentation to be able to use it.


##### Scroll lines

Primary scrolling tool (mapped under "ctrl+alt+k", "ctrl+alt+i") instead of
default page up/page down (that are not mapped at all in sublime-enhanced). This
funtionality provided by "sublime-scroll-lines-enhanced" and differs a bit from
sublime's default "scroll lines". Referer to plugin documentation to be see the
difference.


##### Search

Sublime-enhanced replaces default sublime search with "sublime-search-enhanced"
plugin to provide navigation abilities of searching throgh files. Mapped under
ctrl+f ("fuzzy search"), ctrl+shift+f ("fuzzy search backward"), ctrl+alt+f
("search"), ctrl+alt+shift+f  ("search backward"). Plugin also contains bunch
of useful shortcuts that can be found in plugin documentation.


##### Jump by block

Extremely handy feature which allows to jump/select by empty lines. Mapped under
"ctrl+i" (up), "ctrl+k" (down) and "ctrl+shift+i" (select up), "ctrl+shift+k"
(select down). Provided by glorious "sublime-expression" plugin.


##### Indentation navigation

Good way to goto/select start/end of "if", "for", "while" and other blocks that
are indented with spaces or tabs. Provided by "sublime-indentation-navigation"
plugin. This plugin also provides "select indentation" that works a bit
different from sublime's default "select indentation".


##### Goto last edit location

Goto last edit location is really handy feature, mapped under "alt+z" (next),
"alt+shift+z" (previous) and provided by "sublime-goto-last-edit-enhanced".


##### Marks

Default sublime feature that are extended with "sublime-named-mark" plugin.
Mapped under "cltr+shift+q" (insert mark) and "ctrl+q" (goto mark). Plugin
itself contains some handy features, refer documentation of plugin to study it.


##### Automatic marks

Marks that are inserted automatically when issuing specified commands. Provided
by "sublime-incremental-mark" plugin and binded under "alt+r" (next mark),
"alt+shift+r" (previous mark) and "alt+ctrl+r" (clean incremental marks). This
feature is handy when used with "goto definition", "goto begin/end of file" -
you can quickly come back to previous location.


### Usage: Line navigation

This section describes the ways to move cursor in line or several lines of
code to desired positon. Each way of line should be studied carefully and used
according to situation.


##### Goto character

Move cursor to character in the line. Mapped under "alt+a, &lt;char&gt;" and
provided by "sublime-goto-character". Usually used with "repeat last command"
(alt+x) provided by "sublime-repeat-command" plugin. Plugin also provides
various types of "goto character", refer to its documentation to study all
types of "goto character".


##### Goto brackets (various types)

Allows to quickly navigate by various type of brackets (), {}, []: primary
hotkey is "alt+enter" (goto into brackets), "alt+shift+enter" (goto out of
brackets) provided by glorious "sublime-expression" plugin. There also hotkeys
to select in brackets, select in string, goto brackets backward and skip
brackets. Refer to "sublime-expression" documentation to study brackets/string
navigation.


##### Goto previous/next line, word, subword or character

This is default sublime features but it remapped under "alt+ijkl", "ctrl+jl" and
"alt+ctrl+jl" (+shift works as selection) by "sublime-keymap-enhanced" plugin.
Refer to plugin documentation to see all bindings.


##### Search

Search also can be used to line navigation. Refer to "sublime-search-enhanced"
documentation.


##### Statement/token navigation

Primary actions: goto previous/next token/argument ("alt+,", "alt+.", +shift is
for arguments), goto start/end of token ("alt+m"), goto/select argument by
number (alt+&lt;number&gt;, alt+shift+&lt;number&gt;; number is from 1 to 5),
select token/argument/statement (alt+s, alt+shift+s). This features are part of
"sublime-statement" plugin, refer to plugin documentation to study it behaviour.


### Usage: Multicursors

Multicursors it is one of most powerful sublime's features that should be
carefully studied and abudantly used while solving tasks. This section
describes ways to manipulate cursors (spawn and destroy it).


##### Spawning multicursors

Sublime by default have four ways of spawning multicursors:

- Select all occurences of text under cursor/selection (alt+f3)

- Select next occurence of text under cursor/selection

- Find all occurences using search

- Snippets (when snippet have two placeholders with same number)

- Mouse selection (ctrl+mouseclick)

Sublime-enhanced adds some enhancements over cursors spawning: select
next/previous occurence of text/word under cursor/selection that are provided
by "sublime-append-selection" plugin. Primary shortcuts are "alt+c",
"alt+ctrl+c". Refer to plugin documentation to see all shortcuts.

Multicursors also can be spawned using "rename local variable"
(sublime-local-variable plugin) feature or similar.


##### Destroying cursors

Sublime by default have two ways to destroy cursors:

- Destroy all except first (esc)

- Destroy with mouse selection (alt+mouseclick+drag)

Sublime-enhanced adds new features: destroy by number ("ctrl+u,
ctrl+&lt;number&gt;" where number is from 1 to 5), remove last cursor
(cltr+alt+shift+x) and leave only first cursor (ctrl+esc).


##### Note about mouse usage

In some really rare cases mouse can be used to spawn or destroy multicursors as
sublime-enhanced does not provides necessary features to do it with keyboard
yet. This is only exception on mouse usage and will be fixed with new plugins
that will be released in future.


### Usage: Modifying source code


##### Autocompletion

This is glorious plugin that allows to reduce plain typing drastically. It
provides different types of autocompletion. Primary shortcuts is "ctrl+o"
(complete backward), "ctrl+p" (complete forward). There is more shortcuts, refer
to "sublime-utocompletion" plugin documentation.


##### Snippets

Snippets is very handy tool to write source code. It is highly recommended to
study snippet system and use snippets abudantly if you are not snippet-user yet.
Sublime-enhanced snippet system built on top of default sublime's snippets to
fix various issues and to provide more features. Along with
"sublime-autocompletion" it reduce  plain typing drastically. Read
"sublime-snippet-caller" documentation to study sublime-enhanced snippet system.


##### Method manipulation

Glorious "sublime-method" contains a bunch of useful features like "create new
method" (ctrl+alt+shift+n), "delete method" (ctrl+m, ctrl+d), "move method
up/down" ("alt+-", "alt+=") and etc. Refer to it documentation to see how to use
it.


##### Local variables manipulation

Glorious extract/detach variable from cursor/selection by hotkey ("ctrl+alt+x",
"ctrl+shift+x" hotkeys). Also provides rename local variable feature
("alt+shift+x"). Refer to "sublime-local-variable" documentation to see how it
works.


##### Clone file

It is possible to clone file with "ctrl+alt+shift+d" hotkey. Provided by
"sublime-clone-file" plugin.


##### Various optimizations

There are some tasks automated by plugins. Refer to "sublime-formatter",
"sublime-join-assignment", "sublime-join-chain-call", "sublime-join-statement",
"sublime-keyword", "join-lines-enhanced", "sublime-semicolon",
"sublime-wrap-statement" plugins documentation.
