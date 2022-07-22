## 第四十二天

### iterm - zsh-vi-mode 高级使用

#### surround

- S": 进入 visual 模式选中单词输入`S"`
- ys": 与上相同
- cs"': 更改包裹的符号
- ds"': 删除包裹的符号

#### s-prefix

在`zshrc`下添加:

```
ZVM_VI_SURROUND_ESCAPE_BINDKEY = s-prefix
```

- sa": 添加包裹符号
- sd": 删除包裹的符号
- sr"': 替换包裹符号

#### 改键

```
cd opt/zsh-vi-mode/share/zsh-vi-mode/
vim zsh-vi-mode-zsh
```

```bash
# Your custom widget
function jump_end_of_line() {
    zvm_navigation_handler $
}

function jump_start_of_line() {
    zvm_navigation_handler ^
}

# The plugin will auto execute this zvm_after_lazy_keybindings function
function zvm_after_lazy_keybindings() {
  # Here we define the custom widget
  zvm_define_widget jump_end_of_line
  zvm_define_widget jump_start_of_line

  # In normal mode, press Ctrl-E to invoke this widget
  zvm_bindkey vicmd 'L' jump_end_of_line
  zvm_bindkey visual 'L' jump_end_of_line
  zvm_bindkey vicmd 'H' jump_start_of_line
  zvm_bindkey visual 'H' jump_start_of_line
}
```

#### 复制

修改`zvm_vi_yank`函数

```bash
function zvm_vi_yank() {
    zvm_yank
    echo ${CUTBUFFER} | pbcopy
    zvm_exit_visual_mode
}
```

#### setup

zsh-vi-mode 存在一个配置文件，启动时会自动调用， 可将之前配置的环境变量添加到配置文件中

```
cd opt/zsh-vi-mode/share/zsh-vi-mode/
vim zsh-vi-mode-zsh
```
