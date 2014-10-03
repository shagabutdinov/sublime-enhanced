# Installation

1. Open your "Packages" folder by "Preferences: Browse packages" command in
   command palette

2. Backup parent folder of "Packages" (it is "sublime-text-3" for linux,
   "Sublime Text 3" for OSX and windows); in case of troubles you should use
   this backup to restore original state of sublime.

3. Unzip "sublime-enhanced-packages.zip" to your "Packages" folder

4. Ensure that you have "Droid Sans Mono" font installed in your system

5. Append following contents to your "User/Preferences.sublime-settings":

  ```
  "theme": "DevastateMini.sublime-theme",
  "color_scheme": "Packages/DevastateMini/DevastateMini.tmTheme",
  ```

6. Append following contents to your "User/Default (*).sublime-keymap" file,
   "Preferences: Key Bindings - User" in command palette (alt+\):

  ```
  // KeymapEnhanced:
  // Should be in User/Default ().sublime-keymap to avoid conflicts with
  // Terminal plugin

  {
    "keys": ["ctrl+shift+t"],
    "command": "reopen_last_file"
  },

  // JointStatement:
  // Next two mappings should be in User/Default ().sublime-keymap to avoid
  // conflicts with Terminal plugin
  {
    "keys": ["ctrl+alt+shift+t"],
    "command": "unjoin_statement",
    "args": {
      "as_arguments": false
    },
    "context": [
      {"key": "in_arguments", "operator": "equal", "operand": false}
    ]
  },

  {
    "keys": ["ctrl+alt+shift+t"],
    "command": "unjoin_statement",
    "args": {
      "as_arguments": true
    },
    "context": [
      {"key": "in_arguments", "operator": "equal", "operand": true}
    ]
  },

  // Expression:
  // should be in User/Default ().sublime-keymap to avoid [ctrl+k, ...] calls
  {
    "keys": ["ctrl+k"],
    "command": "run_macro_file",
    "args": {
      "file": "res://Packages/Expression/macro/goto_block_down.sublime-macro"
    },
  },
  ```

7. (Optionally) For quick "dive in" you can disable arrows-navigation; to do it,
   copy your default keybindings ("Preferences: Key Bindings - Default" in
   command palette) into "Default/Default (**OS**).sublime-keymap" in "Packages"
   folder ("Preferences: Browse packages" in command palette) and comment
   following lines:

   ```
   { "keys": ["left"], "command": "move", "args": {"by": "characters", "forward": false} },
   { "keys": ["right"], "command": "move", "args": {"by": "characters", "forward": true} },
   { "keys": ["up"], "command": "move", "args": {"by": "lines", "forward": false} },
   { "keys": ["down"], "command": "move", "args": {"by": "lines", "forward": true} },
   { "keys": ["shift+left"], "command": "move", "args": {"by": "characters", "forward": false, "extend": true} },
   { "keys": ["shift+right"], "command": "move", "args": {"by": "characters", "forward": true, "extend": true} },
   { "keys": ["shift+up"], "command": "move", "args": {"by": "lines", "forward": false, "extend": true} },
   { "keys": ["shift+down"], "command": "move", "args": {"by": "lines", "forward": true, "extend": true} },

   { "keys": ["ctrl+left"], "command": "move", "args": {"by": "words", "forward": false} },
   { "keys": ["ctrl+right"], "command": "move", "args": {"by": "word_ends", "forward": true} },
   { "keys": ["ctrl+shift+left"], "command": "move", "args": {"by": "words", "forward": false, "extend": true} },
   { "keys": ["ctrl+shift+right"], "command": "move", "args": {"by": "word_ends", "forward": true, "extend": true} },

   { "keys": ["alt+left"], "command": "move", "args": {"by": "subwords", "forward": false} },
   { "keys": ["alt+right"], "command": "move", "args": {"by": "subword_ends", "forward": true} },
   { "keys": ["alt+shift+left"], "command": "move", "args": {"by": "subwords", "forward": false, "extend": true} },
   { "keys": ["alt+shift+right"], "command": "move", "args": {"by": "subword_ends", "forward": true, "extend": true} },

   { "keys": ["alt+shift+up"], "command": "select_lines", "args": {"forward": false} },
   { "keys": ["alt+shift+down"], "command": "select_lines", "args": {"forward": true} },

   { "keys": ["pageup"], "command": "move", "args": {"by": "pages", "forward": false} },
   { "keys": ["pagedown"], "command": "move", "args": {"by": "pages", "forward": true} },
   { "keys": ["shift+pageup"], "command": "move", "args": {"by": "pages", "forward": false, "extend": true} },
   { "keys": ["shift+pagedown"], "command": "move", "args": {"by": "pages", "forward": true, "extend": true} },

   { "keys": ["home"], "command": "move_to", "args": {"to": "bol", "extend": false} },
   { "keys": ["end"], "command": "move_to", "args": {"to": "eol", "extend": false} },
   { "keys": ["shift+home"], "command": "move_to", "args": {"to": "bol", "extend": true} },
   { "keys": ["shift+end"], "command": "move_to", "args": {"to": "eol", "extend": true} },
   { "keys": ["ctrl+home"], "command": "move_to", "args": {"to": "bof", "extend": false} },
   { "keys": ["ctrl+end"], "command": "move_to", "args": {"to": "eof", "extend": false} },
   { "keys": ["ctrl+shift+home"], "command": "move_to", "args": {"to": "bof", "extend": true} },
   { "keys": ["ctrl+shift+end"], "command": "move_to", "args": {"to": "eof", "extend": true} },

   { "keys": ["ctrl+up"], "command": "scroll_lines", "args": {"amount": 1.0 } },
   { "keys": ["ctrl+down"], "command": "scroll_lines", "args": {"amount": -1.0 } },

   { "keys": ["ctrl+pagedown"], "command": "next_view" },
   { "keys": ["ctrl+pageup"], "command": "prev_view" },
   ```

8. (Optionally) Install following very handy packages one by one:

  - OpenSearchResult (https://github.com/abrookins/OpenSearchResult)

  - Case Conversion (https://github.com/jdc0589/CaseConversion)

  - ColorSchemeSelector (https://github.com/jugyo/SublimeColorSchemeSelector)

  - Inc-Dec-Value (https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value)

  - Move Tab (https://github.com/FMCorz/MoveTab)

  - SublimeLinter family (https://github.com/SublimeLinter)

  And add keybindings to this packages:

  ```
  // Case Conversion

  {
    "keys": ["ctrl+u", "ctrl+-"],
    "command": "convert_to_snake"
  },

  {
    "keys": ["ctrl+u", "ctrl+="],
    "command": "convert_to_camel"
  },

  // Inc-Dec-Value

  {
    "keys": ["ctrl+="],
    "command": "inc_dec_value",
    "args": {
      "action": "inc_min"
    }
  },

  {
    "keys": ["ctrl+-"],
    "command": "inc_dec_value",
    "args": {
      "action": "dec_min"
    }
  },

  {
    "keys": ["ctrl+shift+="],
    "command": "inc_dec_value",
    "args": {
      "action": "inc_max"
    }
  },

  {
    "keys": ["ctrl+shift+-"],
    "command": "inc_dec_value",
    "args": {
      "action": "dec_max"
    }
  },

  {
    "keys": ["ctrl+alt+="],
    "command": "inc_dec_value",
    "args": {
      "action": "inc_all"
    }
  },

  {
    "keys": ["ctrl+alt+-"],
    "command": "inc_dec_value",
    "args": {
      "action": "dec_all"
    }
  },

  // MoveTab

  {
    "keys": ["ctrl+shift+,"],
    "command": "move_tab",
    "args": {
      "position": "-1"
    }
  },

  {
    "keys": ["ctrl+shift+."],
    "command": "move_tab",
    "args": {
      "position": "+1"
    }
  },

  // ColorSchemeSelector

  {
    "keys": ["ctrl+u", "ctrl+t"],
    "command": "select_color_scheme"
  },

  // Open Search Result

  {
    "keys": ["enter"],
    "command": "open_search_result",
    "context": [
      {"key": "selector", "operator": "equal", "operand": "text.find-in-files"}
    ]
  },

  ```

9. (Optionally) Restart sublime.