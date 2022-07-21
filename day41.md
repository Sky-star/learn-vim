## 第四十一天

### iterm - zsh-vi-mode

#### 安装

```bash
brew install zsh-vi-mode
```

复制代码到`zshrc`中

```
vim ~/.zshrc
source /usr/local/opt/zsh-vi-mode/share/zsh-vi-mode/zsh-vi-mode.plugin.zsh
```

#### 返回 normal 模式

- esc
- ctrl + [
- 配置为 jj
  ```
  ZVM_VI_INSERT_ESCAPE_BINDKEY=jj
  ZVM_VI_VISUAL_ESCAPE_BINDKEY=jj
  ZVM_VI_OPPEND_ESCAPE_BINDKEY=jj
  ```

#### 历史记录

- insert 模式下
  - ctrl + p
  - ctrl + n
- normal 模式下
  - j/k : 翻动历史命令记录
  - / : 命令搜索 通过 `n`/`N` 进行上下查找

#### 进入 vi-mode 模式

normal 模式下输入: `vv`
