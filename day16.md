## 第十六天

### 删除函数

- %: 会匹配当前光标所在符号，类似`()` `{}`

- vii: 会选中函数体内部代码

- vai: 会选中整个函数体代码, 这个会导致函数体末尾的`}`不会被选中

- vaI: 会选中整个函数体代码，但是光标需要在函数体内部

#### 删除函数的方案

- dap: 基于空格为一个段落的删除，不怎么用，函数基本会用空格分割逻辑

- daI: 基于缩进的函数体删除，光标需要在函数体内

- sapce + d + f: V$%d =基于行的选中，进入到行尾，匹配`{`, 但是光标需要在函数签名所在的行数, 改建后用