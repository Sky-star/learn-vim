## 第九天

### 单文件内更高效的移动 

## easyMotion

开启easyMotion

```json
"vim.leader": "<Space>",
"vim.useSystemClipboard": true,
```

### 常用命令
```
// 常用命令
<leader><leader> + w: 从当前光标开始向下查找所有单词的开头
<leader><leader> + b: 从当前光标开始向上查找所有单词的开头
<leader><leader> + e: 从当前光标开始向下查找所有单词的尾部
<leader><leader> + ge: 从当前光标开始向上查找所有单词的尾部

// 基于行的条状
<leader><leader> + j: 从当前光标开始以行为基准向下查找所有单词的开头
<leader><leader> + k: 从当前光标开始以行为基准向上查找所有单词的开头


<leader><leader> + h: 向上查找所有匹配驼峰,_,#格式的单词
<leader><leader> + l: 向下查找所有匹配驼峰,_,#格式的单词
// 全局的查找
<leader><leader><leader> + j: 全局查找所有匹配驼峰,_,#格式的单词
```

## sneak

`f`功能的扩展,利用`sneak`代替`f`功能
功能其实类似于/功能,但是用`sneak`会省一步回车的操作

**配置完成后会将搜索操作在各个模式下进行统一**

### 开启以及配置

```json
"vim.sneak": true,
"vim.visualModeKeyBindingsNonRecursive": [
    {
        "before": ["f"],
        "after" : ["s"]
    },
],
"vim.operatorPendingModeKeyBindingsNonRecursive": [
    {
        "before": ["f"],
        "after" : ["z"]
    },
    {
        "before": ["F"],
        "after" : ["Z"]
    },
],
"vim.normalModeKeyBindingsNonRecursive": [
    {
        "before": ["f"],
        "after" : ["s"]
    },
    {
        "before": ["F"],
        "after" : ["S"]
    },
    {
        "before": ["s"],
        "after" : ["c", "l"]
    },
    {
        "before": ["S"],
        "after" : ["^", "C"]
    }
]
```

语法: f + 2个字符

```
f + 字符: 向下查找匹配的字符
F + 字符: 向上查找匹配的字符
;/,: 向后/向前查找
```