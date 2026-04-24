# Bish3.1 Plans

* [x] 🟢 让函数能获取调用者的`BishScope`
* [x] 🔴 让程序能获取自身的字节码
* [ ] 🔴 让程序能获取自身的源代码
  - 需要在编译产物中储存字节码对应的行数和源代码位置
* [ ] 🟡 加入`async`
* [x] 🟡 加入**BishCompiler**和**Bish**的测试
* [x] 🟡 将`import`不涉及编译的部分下放到**BishRuntime**，编译时注入`root`和`compile`
* [ ] 🟢 加入`object`的默认`hook_enter`和`hook_exit`实现
* [ ] 🟢 加入内插字符串
* [x] 🟡 将字节码和`BishFrame`作为`BishObject`
* [ ] 🟢 加入用于编译和编译文件的函数
* [x] 🟢 在函数中存储捕获的`frame`
