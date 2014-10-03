# Default keymap

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

  // Duplicate Lines

  {
    "keys": ["ctrl+d"],
    "command": "duplicate_lines",
    "context": [
      {"key": "overlay_visible", "operator": "equal", "operand": false},
      {"key": "is_search_panel_enhanced_visible", "operator" : "equal", "operand": false}
    ],
  },

  // MarkdownPreview

  {
    "keys": ["ctrl+u", "m"],
    "command": "markdown_preview",
    "args": {
      "target": "browser",
      "parser":"github"
    }
  }