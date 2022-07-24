## 第四十四天

### zsh 自定义快捷键

#### bindkey

输入 bindkey 可以查看已经绑定的 widgets

使用^表示 ctrl，使用\e 表示 alt

#### 添加

`bindkey 快捷键 widgets` 可以设置快捷键

`bindkey -s 快捷键 快捷键` 可以将前一个快捷键映射到后一个快捷键

`bindkey -M 模式 快捷键 widgets` 将快捷键绑定到具体的模式上，模式包括：

- emacs 默认模式
- viins vim insert 模式
- vicmd vim normal 模式
- viopp vim operator pending 模式
- visual vim visual 模式

#### 删除

`bindkey -r 快捷键` 可以删除快捷键

### widgets

可以使用`zle -la`查看所有快捷键

### 帮助文档

`man zshzle`查看帮助文档
