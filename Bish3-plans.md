# Bish3 Plans
此文件用于个人记录[Bish](https://github.com/labbish/Bish)的下一个大版本的更改计划。

* 区分`SetMember`和`DefMember`
  - 进而让`BishScope`直接作为`BishObject`，从而去除掉`reflect`
  - [专栏](https://www.bilibili.com/opus/1181531621797396483)
* 让函数能获取调用者的`BishScope`
* 把文件全局作用域和内置全局作用域分开，前者的外层为后者，后者在整个运行时共享；增加字节码`GET_BUILTIN`单独用于获取后者
* 尽可能把更多东西直接存在`BishObject`里面（比如`BishFrame`甚至`BishBytecode`），减少Proxy类的使用
* 模糊`expr`和`stat`的边界
  - 进而去除三元运算符、合并2种`switch`写法
  - [专栏](https://www.bilibili.com/opus/1188186811118125061)
* 将**BishLSP**并入**Bish**，**BishBytecode**并入**BishRuntime**
* 把**bish-vsc**作为单独的项目分割出来
  - 可以作为*HZZcode*的项目，这个不算语言核心的部分
* 尽可能把所有测试都改写成*Bish*代码，去掉直接使用对象操作/字节码的测试
* 改革错误处理系统
  - [专栏](https://www.bilibili.com/opus/1189376916487929857)
* 加入`async`（没想好怎么设计）
  - 但无论如何我不太希望异步带有染色性
* 把`function`类型变成内置的（而不是放到库里面）
* 试着找到一个处理`hook`造成的`StackOverflow`的统一、简洁的方法
* 支持自定义`hook_bind`
* 想办法在语言内部处理函数递归溢出的问题
  - 也许可以考虑自己实现一个函数栈，这样也能对异步有帮助
* 把`BuiltinBinder`变成编译期的
  - 也许该用*Rust*重写*Bish*了？
    * 优势：从零开始，可以避免很多技术债；生成宏很好用；性能可能有点提升（虽然这本来就不是重点）
    * 劣势：需要自己写*GC*；可能会带来不少额外复杂性；*Rust*的对象模型可能并不适合*Bish*
  - 更简单的方案：用*Roslyn*的代码生成（使用`ModuleInitializer`）
  - 支持自动生成`getter`/`setter`/`deller`
* 把各种用`List`和`Dictionary`的地方改成`IList`和`IDictionary`并且用线程安全版本
* 支持空`return`
