# vscode_extensions_settings

## Extensions Summary

- Markdown/Foam
- XML
- C#
- C++
- Rust
- CSV
- Git
- Themes
- Others

## Install

1. Open this directory in VSCode, view .vscode/extensions.json.
2. Press Ctrl/Cmd+Shift+P, Show Recommended Extensions, then click download icon in WORKSPACE RECOMMENDATIONS panel title
3. Press Ctrl/Cmd+Shift+P, Open User Settings (JSON), then copy .vscode/settings.json content to your settings.json, and save it.
4. Press Ctrl/Cmd+Shift+P, Open Keyboard Shortcuts (JSON), then copy .vscode/keybindings.json content to your keybindings.json, and save it.
5. Copy file from snippets to %appdata%\Code\User\snippets or Press Ctrl/Cmd+Shift+P, Snippets: Configure User Snippets to custom.

### markdown-pdf.executablePath

If you want to use your own Chromium, you can set the path to the Chromium executable file.

```json
"markdown-pdf.executablePath": "C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe",
```
