## 1.定义
“Lambda 表达式”(lambda expression)是一个匿名函数，Lambda表达式基于数学中的λ演算得名，直接对应于其中的lambda抽象(lambda abstraction)，是一个匿名函数，即没有函数名的函数。Lambda表达式可以表示闭包（注意和数学传统意义上的不同）。

## 2.Java使用Lambda解决的问题
写出更简洁、更灵活的diam，更紧凑的代码风格，使Java的语言表达能力得到了提升。

## 3.Lambda的表达式

## 4.表达式语法

Lambda表达式在Java语言引入一个新的语法元素和操作符。这个操作符号为“->”，它将Lambda分两部分：
 左侧： 指定Lambda表达式需要的所有参数
 右侧： 指定Lambda体，即Lambda表达式要执行的功能。

### 4.1 六个语法格式

语法格式一： 无参，无返回值，Lambda体只需要一条语句

```
()-> System.out.println("hey! Lambda.");
```

语法格式二：Lambda需要一个参数

```
(value) -> System.out.println(value);
```

语法格式三：Lamdba只需要一个参数时，参数的小括号可以省略

```
value -> System.out.println(value)
```

语法格式四： Lambda需要两个参数，并且有返回值

```
(x, y) -> {
	System.out.println("hey! ");
	return x+y;
};
```

语法格式五： 当Lambda体只有一条语句，retrun 与大括号可以省略

```
(x, y) -> x + y;
```
语法格式六：数据类型可以省略，由推断器给出

```

（Long x, Long y）-> {

	System.out.println("This is ...");

	return x + y;
}
```

注：“类型推断器”可以使Lambda表达式无需指定类型，程序可以编译，因为javac根据程序的上下文，在后台推断出了参数的类型，Lambda表达式的类型依赖于上下文环境，由于编译器推断出来。

