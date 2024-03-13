# Configuracion del VSCode para Web

Archivo Settings.json 

```json
// Configuracion de AJRA
// al 04/03/2024
{
  "editor.formatOnSave": true,
  "editor.suggest.insertMode": "replace",
  "terminal.integrated.fontFamily": "MesloLGS NF",
  "editor.linkedEditing": true,
  "javascript.updateImportsOnFileMove.enabled": "always",
  //"window.zoomLevel": 0.5,
  "launch": {},
  "[json]": {},
  "editor.minimap.enabled": false,
  "breadcrumbs.enabled": false,
  //"workbench.iconTheme": "material-icon-theme",
  "update.showReleaseNotes": false,
  "zenMode.hideLineNumbers": false,
  "editor.lineNumbers": "relative",

  "vim.leader": "<Space>",
  "vim.hlsearch": true,
  "vim.normalModeKeyBindingsNonRecursive": [
    // NAVIGATION
    // switch b/w buffers
    { "before": ["<S-h>"], "commands": [":bprevious"] },
    { "before": ["<S-l>"], "commands": [":bnext"] },

    // splits
    { "before": ["leader", "v"], "commands": [":vsplit"] },
    { "before": ["leader", "s"], "commands": [":split"] },

    // panes
    {
      "before": ["leader", "h"],
      "commands": ["workbench.action.focusLeftGroup"]
    },
    {
      "before": ["leader", "j"],
      "commands": ["workbench.action.focusBelowGroup"]
    },
    {
      "before": ["leader", "k"],
      "commands": ["workbench.action.focusAboveGroup"]
    },
    {
      "before": ["leader", "l"],
      "commands": ["workbench.action.focusRightGroup"]
    },
    // NICE TO HAVE
    { "before": ["leader", "w"], "commands": [":w!"] },
    { "before": ["leader", "q"], "commands": [":q!"] },
    { "before": ["leader", "x"], "commands": [":x!"] },
    {
      "before": ["[", "d"],
      "commands": ["editor.action.marker.prev"]
    },
    {
      "before": ["]", "d"],
      "commands": ["editor.action.marker.next"]
    },
    {
      "before": ["<leader>", "c", "a"],
      "commands": ["editor.action.quickFix"]
    },
    { "before": ["leader", "f"], "commands": ["workbench.action.quickOpen"] },
    { "before": ["leader", "p"], "commands": ["editor.action.formatDocument"] },
    {
      "before": ["g", "h"],
      "commands": ["editor.action.showDefinitionPreviewHover"]
    }
  ],
  "vim.visualModeKeyBindings": [
    // Stay in visual mode while indenting
    { "before": ["<"], "commands": ["editor.action.outdentLines"] },
    { "before": [">"], "commands": ["editor.action.indentLines"] },
    // Move selected lines while staying in visual mode
    { "before": ["J"], "commands": ["editor.action.moveLinesDownAction"] },
    { "before": ["K"], "commands": ["editor.action.moveLinesUpAction"] },
    // toggle comment selection
    { "before": ["leader", "c"], "commands": ["editor.action.commentLine"] }
  ],
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "go.toolsManagement.autoUpdate": true,
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.fontSize": 12,
  "workbench.activityBar.location": "hidden"
}

```

Archivo keybidings.json

```json
// AJRA
// 04/03/2004
[
    // NAVIGATION
    {
      "key": "ctrl+shift+a",
      "command": "workbench.action.terminal.focusNext",
      "when": "terminalFocus"
    },
    {
      "key": "ctrl+shift+b",
      "command": "workbench.action.terminal.focusPrevious",
      "when": "terminalFocus"
    },
    {
      "key": "ctrl+shift+j",
      "command": "workbench.action.togglePanel"
    },
    {
      "key": "ctrl+shift+n",
      "command": "workbench.action.terminal.new",
      "when": "terminalFocus"
    },
    {
      "key": "ctrl+shift+w",
      "command": "workbench.action.terminal.kill",
      "when": "terminalFocus"
    },
    // FILE TREE
    {
      "command": "workbench.action.toggleSidebarVisibility",
      "key": "ctrl+e"
    },
    {
      "command": "workbench.files.action.focusFilesExplorer",
      "key": "ctrl+e",
      "when": "editorTextFocus"
    },
    {
      "key": "n",
      "command": "explorer.newFile",
      "when": "filesExplorerFocus && !inputFocus"
    },
    {
      "command": "renameFile",
      "key": "r",
      "when": "filesExplorerFocus && !inputFocus"
    },
    {
      "key": "shift+n",
      "command": "explorer.newFolder",
      "when": "explorerViewletFocus"
    },
    {
      "key": "shift+n",
      "command": "workbench.action.newWindow",
      "when": "!explorerViewletFocus"
    },
    {
      "command": "deleteFile",
      "key": "d",
      "when": "filesExplorerFocus && !inputFocus"
    },
  
    // EXTRA
    {
      "key": "ctrl+shift+5",
      "command": "editor.emmet.action.matchTag"
    },
    {
      "key": "ctrl+z",
      "command": "workbench.action.toggleZenMode"
    }
  ]
```
