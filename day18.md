## 第十八天

### vim 调用 vscode 的命令

### 技巧

- 格式化文档: Leader + f + d

配置文件如下：

```json
{
	"before": ["<Leader>", "f", "d"],
	"commands": ["editor.action.formatDocument"]
}
```

- 重命名: Leader + r + n

配置文件如下：

```json
{
	"before": ["<Leader>", "r", "n"],
	"commands": ["editor.action.rename"]
}
```

- 折叠代码: Leader + [

配置文件如下：

```json
{
	"before": ["<Leader>", "["],
	"commands": [
		{
			"command": "editor.fold"
		},
		{
			"command": "vim.remap",
			"args": {
				"after": ["$", "%"]
			}
		}
	]
}
```
