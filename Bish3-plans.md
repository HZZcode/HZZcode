# Bish3 Plans
此文件用于个人记录[Bish](https://github.com/labbish/Bish)的下一个大版本的更改计划。颜色用于表示（预估的）实施难度。

|🔴🔴⚪⚪⚪⚪|🟡🟡⚪⚪⚪⚪|🟢🟢🟢🟢🟢⚪|

* [x] 🔴 区分`SetMember`和`DefMember`
  - [x] 进而让`BishScope`直接作为`BishObject`，从而去除掉`reflect`
  - [专栏](https://www.bilibili.com/opus/1181531621797396483)
* [ ] 🟢 让函数能获取调用者的`BishScope`
* [x] 🟡 把文件全局作用域和内置全局作用域分开，前者的外层为后者，后者在整个运行时共享
  - 增加字节码`GET_BUILTIN`单独用于获取后者
  - ~~禁止向内置全局作用域的直接修改（但是保留特殊方法，比如用`BishScope`）~~
* [ ] 🔴 让程序能获取自身的字节码/源代码
* [x] 🔴 模糊`expr`和`stat`的边界
  - 进而去除三元运算符、合并2种`switch`写法
  - [专栏](https://www.bilibili.com/opus/1188186811118125061)
* [x] 🟢 合并项目
  - [x] 将**BishLSP**并入**Bish**
  - [x] 将**BishBytecode**并入**BishRuntime**
* [x] 🟢 把**bish-vsc**作为*HZZcode*的单独项目分割出来
* [x] 🟡 尽可能把所有测试都改写成*Bish*代码，去掉直接使用对象操作/字节码的测试
* [ ] 🟡 改革错误处理系统
  - [专栏](https://www.bilibili.com/opus/1189376916487929857)
* [ ] 🟡 加入`async`
* [x] 🟢 把`Func`类型变成内置的（而不是放到库里面）
* [x] 🟢 加入type的构造函数
* [ ] 🔴 支持自定义`hook_bind`
* [ ] 🔴 把`BuiltinBinder`变成编译期的，使用源生成器生成`ModuleInitializer`
  - [ ] 支持自动生成`getter`/`setter`/`deller`
* [ ] 🟡 改用线程安全容器
  - [ ] `List`->`ConcurrentList`
  - [x] `Dictionary`->`ConcurrentDictionary`
* [ ] 🟡 尽可能减少字段（特别是`public`的），改成访问修饰符恰当的属性
* [x] 🟢 支持空`return`
* [ ] 🔴 完善`BytecodeParser`，改为使用源生成器
