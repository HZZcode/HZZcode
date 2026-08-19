# ZZ的小短文目录

因为我几乎每次写东西都会随手丢到一个随机平台，以及有一些过去写的东西在现在的我看来已经很烂了不推荐看，所以在这里整理一下我自认为还算满意的文章。

## labbish杂谈

在设计实现[Bish语言](https://github.com/labbish/Bish)的过程中，参考学习其它各种语言的设计，产生的一些想法。

- [畅想：基于数据流分析的自动并行化？](https://www.bilibili.com/opus/1181110092244713474) 2026.3.18
  饭后的奇妙想法，事后看来其实是“重新发现”了SSA。
- [什么是好的变量存取设计？](https://www.bilibili.com/opus/1181531621797396483) 2026.3.19
  如你所见Bish2设计得不怎么样。
- [statement和expression需要边界吗？](https://www.bilibili.com/opus/1188186811118125061) 2026.4.6
  另一篇Bish3前夕写的东西。
- [既要异常机制，又要Result语法糖？](https://www.bilibili.com/opus/1189376916487929857) 2026.4.10
  同上。当时并不了解Zig，现在我不好说哪个的错误处理更好。
- [所以，怎么做异步？](https://www.bilibili.com/opus/1195142373215043590) 2026.4.25
  实际上是直到那时我才真的搞懂了啥是异步，过去只会无脑往上加`async`。
- [从零开始的JSON解析器](https://www.bilibili.com/opus/1197411984249716757) 2026.5.1
  是的，那之前我甚至不会写递归下降。要不怎么说Antlr4伟大无需多言呢？
- [关于对象初始化的合理姿势](https://www.bilibili.com/opus/1202157794230272021) 2026.5.14
  构造函数已死也是老生常谈的话题了。

## 没苦硬吃系列

- [论为什么C#的接口静态抽象方法就是typeclass](https://zhuanlan.zhihu.com/p/2072282773423908065) 2026.8.16
  如题，实现了可以静态分派的typeclass。
  [论为什么C#的接口静态抽象方法就是trait](https://zhuanlan.zhihu.com/p/2072288201629235196) 2026.8.16
  这次是就像`dyn Trait`一样的动态分派。
- [论为什么你应该用typescript取代lean4](https://zhuanlan.zhihu.com/p/2073349262268690668) 2026.8.19
  在Typescript类型系统描述`And`, `Or`, `Not`。
  [论为什么你不应该用typescript取代lean4](https://zhuanlan.zhihu.com/p/2073373051539015120) 2026.8.19
  还有任意&存在类型。
- [论为什么C#的类型系统是Rank-N的](https://zhuanlan.zhihu.com/p/2073467269791991728) 2026.8.19
  你有想过C#支持接口中的和`virtual`的泛型方法意味着什么吗？

## 杂项

- [ZZ的代码风格Guide](guide/coding.md) 2026.4.12
  感觉自己的代码审美还是比较独特的。
- [从Peano算术到Grothendieck宇宙](guide/infinity.md) 2026.6.29
  什么叫我竟然还会数学？Github对markdown内嵌公式支持有点不好，可以看[放图片的B站版](https://www.bilibili.com/opus/1230427153047224336)或者下载。