## 第四十天

### iterm - zellij 高级使用技巧

#### session

类似一个快照机制，使用会将当前状态保存

- 创建: `ctrl + o + d` 随机创建 session 名称 `zj attach -c <session name>` 指定 session 名称

- 使用: `zj attach <session name>`

- 查看: `zj list-session` 或 `zj ls`

- 清空: `zj kill-session` 或 `zj k <session-name>`
  - 清空全部: `zj kill-all-sessions` 或 `zj ka`

#### sync

同步模式， 在多个窗口同步输入

#### 滚动

与 chrome 中的 vim 插件上下翻动相同, jk ud
