## 第十三天

### 替换字符串

语法： `:[range]s/要替换的字符串/partten/替换成的字符串/[flags]`

partten:

其实就是正则表达式,通过正则匹配需要替换的字符串

range:

- %: 全文范围内选择替换
- number,number: 单行范围内输入列数(没啥用)
- number,$: 从指定行到尾部 (也没啥用)

flags:

- g: 全局的查找
- c: 进入一个可选模式, y 全部替换, n 当前不替换, q 直接退出 , l 只替换当前，并且退出

**配合可视化模式下，可以更精确的调整范围，方便替换**

gb: 选中光标所在单词，每按一次 gb 会选下一个相同的单词(区分大小写),并且进入多行选择模式，这样也能很方便的进行替换，不过不能用`.`操作，每一次都需要按一次 gb，略显复杂
