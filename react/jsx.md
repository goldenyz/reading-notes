# JSX中需要注意的一些细节
最近在复习JSX时，发现一些比较容易忽视的细节问题，记录如下：

### 自定义的Component名字需要首字母大写
这个原则意味着，不仅在定义Component(或import)的时候，要首字母大写。而且如果把Component赋值给变量，且该变量被用来创建Element，则该变量的变量名也必须是首字母大写的。

### {}中接受的是表达式
这意味着不能使用if和for。

### Functions也可以作为Component的children
实际上，Component的children可以是任何类型，就和其他props一样。

### 字符串
字符串开始和结束的空白将被自动去掉。字符串之间的换行将被转换成一个空格。因此以下各个情况的输出是一致的：
```
<div>Hello World</div>

<div>
  Hello World
</div>

<div>
  Hello
  World
</div>

<div>

  Hello World
</div>
```

### {}中的表达式返回值为以下之一时，会被忽略: Booleans, null, undefined
0不会被忽略，所以在判断`**.length`等长度相关变量时，不要省略逻辑运算符

## References
* [Introducing JSX](https://facebook.github.io/react/docs/introducing-jsx.html)
* [JSX In Depth](https://facebook.github.io/react/docs/jsx-in-depth.html)