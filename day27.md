## 第二十七天

### vscode-VSpacecode

VSpacecode 实际上是对 vim 和 vscode 操作一种封装，提供了一套可视化或快捷键的操作

#### 安装

在插件商店搜索`VSpacecode` 进行安装即可，具体配置项可从[官方文档](https://vspacecode.github.io/docs/)中查询

#### 配置

settings.json

```json
"vim.normalModeKeyBindingsNonRecursive": [
    {
        "before": ["<space>", ";"],
        "commands": ["vspacecode.space"]
    },
]
```

keybindings.json

```json
// Trigger vspacecode in empty editor group
{
    "key": "space",
    "command": "vspacecode.space",
    "when": "activeEditorGroupEmpty && focusedView == '' && !whichkeyActive && !inputFocus"
},
// Trigger vspacecode when sidebar is in focus
{
    "key": "space",
    "command": "vspacecode.space",
    "when": "sideBarFocus && !inputFocus && !whichkeyActive"
}

```
