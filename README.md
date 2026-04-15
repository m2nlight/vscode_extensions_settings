# vscode_extensions_settings

[TOC]

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

1. Open this directory in VSCode, open `.vscode/extensions.json`
2. Press <kbd>Ctrl/Cmd+Shift+P</kbd>, Show Recommended Extensions, then click download icon in WORKSPACE RECOMMENDATIONS panel title
3. Press <kbd>Ctrl/Cmd+Shift+P</kbd>, input and execute `Open User Settings (JSON)` command, then copy `.vscode/settings.json` content to your `settings.json`, and save it.
4. Press <kbd>Ctrl/Cmd+Shift+P</kbd>, input and execute `Open Keyboard Shortcuts (JSON)` command, then copy `.vscode/keybindings.json` content to your `keybindings.json`, and save it.
5. Copy files from `snippets` folder to `%appdata%\Code\User\snippets` or Press <kbd>Ctrl/Cmd+Shift+P</kbd>, input and execute `Snippets: Configure User Snippets to custom`.

## Markdown Preview Enhanced (MPE) FontFamily

Edit `~/.crossnote/style.less` or `%USERPROFILE%\.crossnote\style.less` file and add the following code:

```css
.markdown-preview.markdown-preview {
  font-family: 'Hack Nerd Font Propo', Menlo, Monaco, Consolas, 'Courier New', 'LXGW WenKai', monospace;
}
```

## MPE Code Chunk

<https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/code-chunk>

This feature requried settings:

```json
{
  "markdown-preview-enhanced.enableScriptExecution": true
}
```

### Code Chunk Parameters

- cmd: `cmd=true` or `cmd="path/to/execute-file"`
- args: `args=["-i","$input_file"]`
- stdin: `stdin=true`
- output: `output="text"`
  one of: html, markdown, text, png, none
- hide: `hide=true`
- class: `class="line-numbers otherClass2 otherClass3"` or `.line-numbers`
- highlight: `highlight="1-3,5"` (Some block themes not supported)
- id: `id="izdlk700"`
- continue: `continue=true` or `continue="izdlk700"`
  before run last or id chunk

> [!TIP]
> `some=true` same to `some`


### Example

#### Shell

##### sh

On Windows, add `C:\Program Files\Git\bin` and `C:\Program Files\Git\mingw64\bin` to environment variable `PATH`

```sh {cmd stdin class="line-numbers"}
pwd && ls
```

##### PowerShell

```powershell {cmd="pwsh" args=["-Nologo"] stdin}
dotnet --info
```

##### CMD

```cmd {cmd stdin}
dotnet --list-sdks
```

#### CSharp

##### There is a hidden chunk

```cs {cmd hide}
#:package Figgle.Fonts@*
```

##### There is `continue=true`

```cs {cmd="dotnet" args=["run", "--file", "$input_file", "-p:PublishAot=false"] stdin continue .line-numbers highlight="1-3"}
using Figgle.Fonts;

var s = FiggleFonts.Slant.Render("Hello world!");
Console.WriteLine(s);
```

#### javaScript

```js {cmd="node" stdin class="line-numbers"}
const date = Date.now()
console.log(date.toString())
```
