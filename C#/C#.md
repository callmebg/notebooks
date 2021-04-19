# 简介

- 专为公共语言基础结构（CLI）设计的
  - CLI右可执行代码和运行时环境组成，允许在不同的计算机平台和体系结构上使用各种高级语言。
- 成为一种广泛应用的专业语言的原因：
  - 现代的、通用的
  - 面向对象
  - 面向组件
  - 结构化语言
  - 产生高效率的程序
  - 可以在多种计算机平台上编译
  - .Net框架的一部分



## 重要功能：

- 布尔条件
- 自动垃圾回收
- 标准库
- 组件版本（Assembly Versioning）
- 属性和事件
- 委托（Delegates）和事件管理
- 易于使用的泛型（Generics）
- 索引器（Indexers）
- 条件编译
- 简单的多线程
- LINQ和Lambda表达式
- 集成Windows



# 环境

## .Net框架（Framework）

.Net 框架是一个创新的平台，能帮您编写出下面类型的应用程序：

- Windows 应用程序
- Web 应用程序
- Web 服务



.Net 框架应用程序是多平台的应用程序。框架的设计方式使它适用于下列各种语言：C#、C++、Visual Basic、Jscript、COBOL 等等。所有这些语言可以访问框架，彼此之间也可以互相交互。

.Net 框架由一个巨大的代码库组成，用于 C# 等客户端语言。下面列出一些 .Net 框架的组件：

- 公共语言运行库（Common Language Runtime - CLR）
- .Net 框架类库（.Net Framework Class Library）
- 公共语言规范（Common Language Specification）
- 通用类型系统（Common Type System）
- 元数据（Metadata）和组件（Assemblies）
- Windows 窗体（Windows Forms）
- ASP.Net 和 ASP.Net AJAX
- ADO.Net
- Windows 工作流基础（Windows Workflow Foundation - WF）
- Windows 显示基础（Windows Presentation Foundation）
- Windows 通信基础（Windows Communication Foundation - WCF）
- LINQ





# 程序结构

## 实例

一个C#程序主要包括以下部分：

- 命名空间声明
- 一个class
- class方法
- class属性
- 一个 **Main** 方法
- 语句和表达式
- 注释



```c#
using System;
namespace HelloWorldApplication
{
    class HelloWorld
    {
        static void Main(string[] args)
        {
            /* */
            Console.WriteLine("Hello World");
            Console.ReadKey();
        }
    }
}
```

输出

`Hello World`



- 第一行：`using System`，using 关键字用于在程序中包含 System 命名空间，一个程序一般有多个 using 语句
- 下一行，namespace 声明，一个 namespace 里包含一系列的类
- 下一行，class 声明，
- 下一行，Main 方法，是所有 C# 程序的入口点，
- 注释
- 最后一行 `Console.ReadKey()`，针对VS.NET用户的，等待一个按键的动作，防止程序屏幕快速运行并关闭（相当于 _getch()）



## 注意

- 大小写敏感
- 所有语句和表达式必须以分号结尾
- 程序执行从 Main 方法开始
- 与Java不同，文件名可以不同于类的名称。





# 基本语法

## 实例

```c#
using System;
namespace RectangleApplication
{
    class Rectangle
    {
        // 成员函数
        double length;
        double width;
        public void Acceptdetails()
        {
            length = 4.5;
            width = 3.5;
        }
        public double GetArea()
        {
            return length * width;
		}
        public void Display()
        {
            Console.WriteLine("Length: {0}", length);
            Console.WriteLine("Width: {0}", width);
            Console.WriteLine("Area: {0}", GetArea());
        }
        
        class ExecuteRectangle
        {
            static void Main(string[] args)
            {
				Rectangle r = new Rectangle();
                r.Acceptdetails();
                r.Display();
                Console.ReadLine();
            }
        }
    }
}
```



## 标识符

- 用来识别类、变量、函数或任何其它用户定义的项目
- 字母、下划线或者 **`@`** 开头，后面可以跟一系列的字母、数字（ 0 - 9 ）、下划线（ _ ）、@。
- 标识符中的第一个字符不能是数字
- 标识符必须不包含任何嵌入的空格或符号，比如 ? - +! # % ^ & * ( ) [ ] { } . ; : " ' / \。
- 标识符不能是 C# 关键字。除非它们有一个 @ 前缀。 例如，@if 是有效的标识符，但 if 不是，因为 if 是关键字。
- 标识符必须区分大小写。大写字母和小写字母被认为是不同的字母
- 不能与C#的类库名称相同。



## 关键字

- 如果想使用这些关键字作为标识符，可以在关键字前面加上 @ 字符作为前缀。

- 在 C# 中，有些关键字在代码的上下文中有特殊的意义，如 get 和 set，这些被称为上下文关键字（contextual keywords）。

  下表列出了 C# 中的保留关键字（Reserved Keywords）和上下文关键字（Contextual Keywords）：

|                  |           |           |            |                        |                       |                |
| ---------------- | --------- | --------- | ---------- | ---------------------- | --------------------- | :------------- |
| **保留关键字**   |           |           |            |                        |                       |                |
| abstract         | as        | base      | bool       | break                  | byte                  | case           |
| catch            | char      | checked   | class      | const                  | continue              | decimal        |
| default          | delegate  | do        | double     | else                   | enum                  | event          |
| explicit         | extern    | false     | finally    | fixed                  | float                 | for            |
| foreach          | goto      | if        | implicit   | in                     | in (generic modifier) | int            |
| interface        | internal  | is        | lock       | long                   | namespace             | new            |
| null             | object    | operator  | out        | out (generic modifier) | override              | params         |
| private          | protected | public    | readonly   | ref                    | return                | sbyte          |
| sealed           | short     | sizeof    | stackalloc | static                 | string                | struct         |
| switch           | this      | throw     | true       | try                    | typeof                | uint           |
| ulong            | unchecked | unsafe    | ushort     | using                  | virtual               | void           |
| volatile         | while     |           |            |                        |                       |                |
| **上下文关键字** |           |           |            |                        |                       |                |
| add              | alias     | ascending | descending | dynamic                | from                  | get            |
| global           | group     | into      | join       | let                    | orderby               | partial (type) |
| partial (method) | remove    | select    | set        |                        |                       |                |





# 数据类型

- 值类型
- 引用类型
- 指针类型



## 值类型

值类型变量可以直接分配给一个值。它们是从类 **`System.ValueType`** 中派生的。

值类型直接包含数据。比如 **int、char、float**，它们分别存储数字、字符、浮点数。当您声明一个 **int** 类型时，系统分配内存来存储值。



| 类型    | 描述                                 | 范围                                                    | 默认值 |
| :------ | :----------------------------------- | :------------------------------------------------------ | :----- |
| bool    | 布尔值                               | True 或 False                                           | False  |
| byte    | 8 位无符号整数                       | 0 到 255                                                | 0      |
| char    | 16 位 Unicode 字符                   | U +0000 到 U +ffff                                      | '\0'   |
| decimal | 128 位精确的十进制值，28-29 有效位数 | (-7.9 x 1028 到 7.9 x 1028) / 100 到 28                 | 0.0M   |
| double  | 64 位双精度浮点型                    | (+/-)5.0 x 10-324 到 (+/-)1.7 x 10308                   | 0.0D   |
| float   | 32 位单精度浮点型                    | -3.4 x 1038 到 + 3.4 x 1038                             | 0.0F   |
| int     | 32 位有符号整数类型                  | -2,147,483,648 到 2,147,483,647                         | 0      |
| long    | 64 位有符号整数类型                  | -9,223,372,036,854,775,808 到 9,223,372,036,854,775,807 | 0L     |
| sbyte   | 8 位有符号整数类型                   | -128 到 127                                             | 0      |
| short   | 16 位有符号整数类型                  | -32,768 到 32,767                                       | 0      |
| uint    | 32 位无符号整数类型                  | 0 到 4,294,967,295                                      | 0      |
| ulong   | 64 位无符号整数类型                  | 0 到 18,446,744,073,709,551,615                         | 0      |
| ushort  | 16 位无符号整数类型                  | 0 到 65,535                                             | 0      |

如需得到一个类型或一个变量在特定平台上的准确尺寸，可以使用 **`sizeof`** 方法。表达式 *`sizeof(type)`*`产生以字节为单位存储对象或类型的存储尺寸。



## 引用类型

引用类型不包含存储在变量中的实际数据，但它们包含对变量的引用。

换句话说，它们指的是一个内存位置。使用多个变量时，引用类型可以指向一个内存位置。如果内存位置的数据是由一个变量改变的，其他变量会自动反映这种值的变化。

- **内置的** 引用类型有：**object**、**dynamic** 和 **string**。
- 用户**自定义**引用类型有：**class**、**interface** 或 **delegate**



### 对象（object）类型

- C# 通用类型系统（Common Type System - CTS）中所有数据类型的终极基类

- Object 是 `System.Object` 类的别名

- 所以对象（Object）类型可以被分配任何其他类型（值类型、引用类型、预定义类型或用户自定义类型）的值。但是，在分配值之前，需要先进行类型转换。

- 当一个值类型转换为对象类型时，则被称为 **装箱**；另一方面，当一个对象类型转换为值类型时，则被称为 **拆箱**。

  - ```c#
    object obj;
    obj = 100; // 装箱
    ```

- 对象类型变量的类型检查是在**编译时**发生的





### 动态（dynamic）类型

您可以存储任何类型的值在动态数据类型变量中。这些变量的类型检查是在**运行时**发生的。

声明动态类型的语法：

```c#
dynamic <variable_name> = value;
```

例如：

```c#
dynamic d = 20;
```

动态类型与对象类型相似，但是对象类型变量的类型检查是在编译时发生的，而动态类型变量的类型检查是在运行时发生的



### 字符串（string）类型

- 允许您给变量分配任何字符串值
- 字符串（String）类型是 `System.String` 类的别名。它是从对象（Object）类型派生的。
- 字符串（String）类型的值可以通过两种形式进行分配：引号和 @引号。



```c#
string str = "Hello";
string str2 = @"C:\Windows"; 
string str3 = "C:\\Windows"; // 等价于 str2
```

- C# string 字符串的前面可以加 @（称作"**逐字字符串**"）将转义字符（\）**当作普通字符**对待

- @ 字符串中可以任意换行，换行符及缩进空格**都计算**在字符串长度之内。

```c#
string str4 = @"<script type=""text/javascript"">
	<!--
	-->
</script>";
```





## 指针类型

- 指针类型变量存储另一种类型的内存地址
- C# 中的指针与 C 或 C++ 中的指针有相同的功能。

声明语法

```c#
type* identifier;
```

例如：

```c#
char* cptr;
int* iptr;
```





# 类型转换

- 类型转换从根本上说是类型铸造，或者说是把数据从一种类型转换为另一种类型。
- 在 C# 中，类型铸造有两种形式：
  - **隐式类型转换**：这些转换是 C# 默认的以安全方式进行的转换, 不会导致数据丢失。例如，从小的整数类型转换为大的整数类型，从派生类转换为基类。
  - **显示类型转换**：显式类型转换，即强制类型转换。显式转换需要强制转换运算符，而且强制转换会造成数据丢失。



## 实例

```c#
namespace TypeConversionApplication
{
    class ExplicitConversion
    {
        static void Main(string[] args)
        {
            double d = 123.45;
            int i;
            
            i = (int)d;
            Console.WriteLine(i); // 输出 123
            Console.ReadKey();
        }
    }
}
```



## 类型转换方法

C# 提供了下列内置的类型转换方法：

| 序号 | 方法 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **ToBoolean** 如果可能的话，把类型转换为布尔型。             |
| 2    | **ToByte** 把类型转换为字节类型。                            |
| 3    | **ToChar** 如果可能的话，把类型转换为单个 Unicode 字符类型。 |
| 4    | **ToDateTime** 把类型（整数或字符串类型）转换为 日期-时间 结构。 |
| 5    | **ToDecimal** 把浮点型或整数类型转换为十进制类型。           |
| 6    | **ToDouble** 把类型转换为双精度浮点型。                      |
| 7    | **ToInt16** 把类型转换为 16 位整数类型。                     |
| 8    | **ToInt32** 把类型转换为 32 位整数类型。                     |
| 9    | **ToInt64** 把类型转换为 64 位整数类型。                     |
| 10   | **ToSbyte** 把类型转换为有符号字节类型。                     |
| 11   | **ToSingle** 把类型转换为小浮点数类型。                      |
| 12   | **ToString** 把类型转换为字符串类型。                        |
| 13   | **ToType** 把类型转换为指定类型。                            |
| 14   | **ToUInt16** 把类型转换为 16 位无符号整数类型。              |
| 15   | **ToUInt32** 把类型转换为 32 位无符号整数类型。              |
| 16   | **ToUInt64** 把类型转换为 64 位无符号整数类型。              |



## 实例

```c#
namespace TypeConversionApplication
{
    class StringConversion
    {
        static void Main(string[] args)
        {
            int i = 75;
            float f = 53.005f;
            double d = 2345.7652;
            bool b = true;
            
            Console.WriteLine(i.ToString());
            Console.WriteLine(f.ToString());
            Console.ReadKey();
        }
    }
}
```





# 变量

- 一个变量只不过是一个供程序操作的存储区的名字
- 在 C# 中，每个变量都有一个特定的类型，类型决定了变量的内存大小和布局
- 范围内的值可以存储在内存中，可以对变量进行一系列操作。

C# 中提供的基本的值类型大致可以分为以下几类：

| 类型       | 举例                                                       |
| :--------- | :--------------------------------------------------------- |
| 整数类型   | sbyte、byte、short、ushort、int、uint、long、ulong 和 char |
| 浮点型     | float 和 double                                            |
| 十进制类型 | decimal                                                    |
| 布尔类型   | true 或 false 值，指定的值                                 |
| 空类型     | 可为空值的数据类型                                         |

- C# 允许定义其他值类型的变量，比如 **enum**，也允许定义引用类型变量，比如 **class**。



## 变量定义

```
<data_type> <variable_list>;
```



## 变量初始化

- 变量通过在等号后跟一个常量表达式进行初始化（赋值）
- 变量可以在声明时被初始化（指定一个初始值）。
- **正确地初始化变量**是一个良好的编程习惯，否则有时程序会产生意想不到的结果。



## 接受来自用户的值

System 命名空间中的 Console 类提供了一个函数 **ReadLine()**，用于接收用户输入，并把它存储到一个变量中

```c#
int num;
num = Convert.ToInt32(Console.ReadLine());
```

函数 `Convert.ToInt32()`把用户输入的数据类型转换为 int 类型，因为 `Console.ReadLine()`只接收**字符串格式**的数据



## 左值和右值

- **lvalue**：表达式可以出现在赋值语句的左边或者右边
- **rvalue**：表达式只能出现在赋值语句的右边





# 常量

- 常量是固定值，程序执行期间不会改变。
- 常量可以是任何基本数据类型，比如整数常量、浮点常量、字符常量或者字符串常量，还有枚举常量。
- 常量可以被当作常规的变量，只是它们的值在定义后不能被修改。



## 整数常量

- 整数常量可以是十进制、八进制或十六进制的常量。
- 前缀指定基数：0x 或 0X 表示十六进制，0 表示八进制，没有前缀则表示十进制。
- 整数常量也可以有后缀，可以是 U 和 L 的组合，其中，U 和 L 分别表示 unsigned 和 long。后缀可以是大写或者小写，多个后缀以任意顺序进行组合。
  - `078 // 非法，八进制没有 8`
  - `0xFeeL // 合法`
  - `032UU // 非法，不能重复后缀`



## 浮点常数

- 一个浮点常量是由整数部分、小数点、小数部分和指数部分组成
- 您可以使用小数形式或者指数形式来表示浮点常量。
- 例子：
  - `314159E-5L 合法`
  - `12E 非法，不完全指数`
  - `210f 非法，没有小数或者指数`
  - `.e55 非法，缺少整数或者小数`
- 使用小数形式表示时，必须包含小数点、指数或同时包含两者
- 使用指数形式表示时，必须包含整数部分、小数部分或同时包含两者。有符号的指数是用 e 或 E 表示的。





## 字符常量

- 字符常量是括在单引号里，例如，'x'，且可存储在一个简单的字符类型变量中。
- 一个字符常量可以是一个普通字符（例如 'x'）、一个转义序列（例如 '\t'）或者一个通用字符（例如 '\u02C0'）
- 在 C# 中有一些特定的字符，当它们的前面带有反斜杠时有特殊的意义，可用于表示换行符（\n）或制表符 tab（\t）

| 转义序列   | 含义                       |
| :--------- | :------------------------- |
| \\         | \ 字符                     |
| \'         | ' 字符                     |
| \"         | " 字符                     |
| \?         | ? 字符                     |
| \a         | Alert 或 bell              |
| \b         | 退格键（Backspace）        |
| \f         | 换页符（Form feed）        |
| \n         | 换行符（Newline）          |
| \r         | 回车                       |
| \t         | 水平制表符 tab             |
| \v         | 垂直制表符 tab             |
| \ooo       | 一到三位的八进制数         |
| \xhh . . . | 一个或多个数字的十六进制数 |





## 字符串常量

- 字符串常量是括在双引号 **""** 里，或者是括在 **@""** 里
- 字符串常量包含的字符与字符常量相似，可以是：普通字符、转义序列和通用字符
- 使用字符串常量时，可以把一个很长的行拆成多个行，可以使用空格分隔各个部分。

```c#
string a = "hello, world";                  // hello, world
string b = @"hello, world";               // hello, world
string c = "hello \t world";               // hello     world
string d = @"hello \t world";               // hello \t world
string e = "Joe said \"Hello\" to me";      // Joe said "Hello" to me
string f = @"Joe said ""Hello"" to me";   // Joe said "Hello" to me
string g = "\\\\server\\share\\file.txt";   // \\server\share\file.txt
string h = @"\\server\share\file.txt";      // \\server\share\file.txt
string i = "one\r\ntwo\r\nthree";
string j = @"one
two
three";
```





## 定义常量

- 常量是使用 **const** 关键字来定义的 。

```c#
using System;

public class ConstTest
{
    class SampleClass
    {
        public int x;
        public int y;
        public const int c1 = 5;
        public const int c2 = c1 + 5;

        public SampleClass(int p1, int p2)
        {
            x = p1;
            y = p2;
        }
    }

    static void Main()
    {
        SampleClass mC = new SampleClass(11, 22);
        Console.WriteLine("x = {0}, y = {1}", mC.x, mC.y);
        Console.WriteLine("c1 = {0}, c2 = {1}",
                          SampleClass.c1, SampleClass.c2);
    }
}
```





# 运算符

- 运算符是一种告诉编译器执行特定的数学或逻辑操作的符号。C# 有丰富的内置运算符
  - 算术运算符
  - 关系运算符
  - 逻辑运算符
  - 位运算符
  - 赋值运算符
  - 其他运算符



## 算术运算符

| 运算符 | 描述                             | 实例             |
| :----- | :------------------------------- | :--------------- |
| +      | 把两个操作数相加                 | A + B 将得到 30  |
| -      | 从第一个操作数中减去第二个操作数 | A - B 将得到 -10 |
| *      | 把两个操作数相乘                 | A * B 将得到 200 |
| /      | 分子除以分母                     | B / A 将得到 2   |
| %      | 取模运算符，整除后的余数         | B % A 将得到 0   |
| ++     | 自增运算符，整数值增加 1         | A++ 将得到 11    |
| --     | 自减运算符，整数值减少 1         | A-- 将得到 9     |





## 关系运算符

| 运算符 | 描述                                                         | 实例              |
| :----- | :----------------------------------------------------------- | :---------------- |
| ==     | 检查两个操作数的值是否相等，如果相等则条件为真。             | (A == B) 不为真。 |
| !=     | 检查两个操作数的值是否相等，如果不相等则条件为真。           | (A != B) 为真。   |
| >      | 检查左操作数的值是否大于右操作数的值，如果是则条件为真。     | (A > B) 不为真。  |
| <      | 检查左操作数的值是否小于右操作数的值，如果是则条件为真。     | (A < B) 为真。    |
| >=     | 检查左操作数的值是否大于或等于右操作数的值，如果是则条件为真。 | (A >= B) 不为真。 |
| <=     | 检查左操作数的值是否小于或等于右操作数的值，如果是则条件为真。 | (A <= B) 为真。   |



## 逻辑运算符

| 运算符 | 描述                                                         | 实例              |
| :----- | :----------------------------------------------------------- | :---------------- |
| &&     | 称为逻辑与运算符。如果两个操作数都非零，则条件为真。         | (A && B) 为假。   |
| \|\|   | 称为逻辑或运算符。如果两个操作数中有任意一个非零，则条件为真。 | (A \|\| B) 为真。 |
| !      | 称为逻辑非运算符。用来逆转操作数的逻辑状态。如果条件为真则逻辑非运算符将使其为假。 | !(A && B) 为真。  |





## 位运算符

位运算符作用于位，并逐位执行操作。&、 | 和 ^ 的真值表如下所示：

| p    | q    | p & q | p \| q | p ^ q |
| :--- | :--- | :---- | :----- | :---- |
| 0    | 0    | 0     | 0      | 0     |
| 0    | 1    | 0     | 1      | 1     |
| 1    | 1    | 1     | 1      | 0     |
| 1    | 0    | 0     | 1      | 1     |

| 运算符 | 描述                                                         | 实例                                                         |
| :----- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| &      | 如果同时存在于两个操作数中，二进制 AND 运算符复制一位到结果中。 | (A & B) 将得到 12，即为 0000 1100                            |
| \|     | 如果存在于任一操作数中，二进制 OR 运算符复制一位到结果中。   | (A \| B) 将得到 61，即为 0011 1101                           |
| ^      | 如果存在于其中一个操作数中但不同时存在于两个操作数中，二进制异或运算符复制一位到结果中。 | (A ^ B) 将得到 49，即为 0011 0001                            |
| ~      | 按位取反运算符是一元运算符，具有"翻转"位效果，即0变成1，1变成0，包括符号位。 | (~A ) 将得到 -61，即为 1100 0011，一个有符号二进制数的补码形式。 |
| <<     | 二进制左移运算符。左操作数的值向左移动右操作数指定的位数。   | A << 2 将得到 240，即为 1111 0000                            |
| >>     | 二进制右移运算符。左操作数的值向右移动右操作数指定的位数。   | A >> 2 将得到 15，即为 0000 1111                             |





## 赋值运算符

| 运算符 | 描述                                                         | 实例                            |
| :----- | :----------------------------------------------------------- | :------------------------------ |
| =      | 简单的赋值运算符，把右边操作数的值赋给左边操作数             | C = A + B 将把 A + B 的值赋给 C |
| +=     | 加且赋值运算符，把右边操作数加上左边操作数的结果赋值给左边操作数 | C += A 相当于 C = C + A         |
| -=     | 减且赋值运算符，把左边操作数减去右边操作数的结果赋值给左边操作数 | C -= A 相当于 C = C - A         |
| *=     | 乘且赋值运算符，把右边操作数乘以左边操作数的结果赋值给左边操作数 | C *= A 相当于 C = C * A         |
| /=     | 除且赋值运算符，把左边操作数除以右边操作数的结果赋值给左边操作数 | C /= A 相当于 C = C / A         |
| %=     | 求模且赋值运算符，求两个操作数的模赋值给左边操作数           | C %= A 相当于 C = C % A         |
| <<=    | 左移且赋值运算符                                             | C <<= 2 等同于 C = C << 2       |
| >>=    | 右移且赋值运算符                                             | C >>= 2 等同于 C = C >> 2       |
| &=     | 按位与且赋值运算符                                           | C &= 2 等同于 C = C & 2         |
| ^=     | 按位异或且赋值运算符                                         | C ^= 2 等同于 C = C ^ 2         |
| \|=    | 按位或且赋值运算符                                           | C \|= 2 等同于 C = C \| 2       |



## 其他运算符

| 运算符   | 描述                                       | 实例                                                         |
| :------- | :----------------------------------------- | :----------------------------------------------------------- |
| sizeof() | 返回数据类型的大小。                       | sizeof(int)，将返回 4.                                       |
| typeof() | 返回 class 的类型。                        | typeof(StreamReader);                                        |
| &        | 返回变量的地址。                           | &a; 将得到变量的实际地址。                                   |
| *        | 变量的指针。                               | *a; 将指向一个变量。                                         |
| ? :      | 条件表达式                                 | 如果条件为真 ? 则为 X : 否则为 Y                             |
| is       | 判断对象是否为某一类型。                   | If( Ford is Car) // 检查 Ford 是否是 Car 类的一个对象。      |
| **as**   | **强制转换，即使转换失败也不会抛出异常。** | Object obj = new StringReader("Hello"); StringReader r = obj as StringReader; |





## 运算符优先级

下表将按运算符优先级从高到低列出各个运算符，具有较高优先级的运算符出现在表格的上面，具有较低优先级的运算符出现在表格的下面

| 类别       | 运算符                            | 结合性   |
| :--------- | :-------------------------------- | :------- |
| 后缀       | () [] -> . ++ - -                 | 从左到右 |
| 一元       | + - ! ~ ++ - - (type)* & sizeof   | 从右到左 |
| 乘除       | * / %                             | 从左到右 |
| 加减       | + -                               | 从左到右 |
| 移位       | << >>                             | 从左到右 |
| 关系       | < <= > >=                         | 从左到右 |
| 相等       | == !=                             | 从左到右 |
| 位与 AND   | &                                 | 从左到右 |
| 位异或 XOR | ^                                 | 从左到右 |
| 位或 OR    | \|                                | 从左到右 |
| 逻辑与 AND | &&                                | 从左到右 |
| 逻辑或 OR  | \|\|                              | 从左到右 |
| 条件       | ?:                                | 从右到左 |
| 赋值       | = += -= *= /= %=>>= <<= &= ^= \|= | 从右到左 |
| 逗号       | ,                                 | 从左到右 |







# 判断

| 语句                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [if 语句](https://www.runoob.com/csharp/csharp-if.html)      | 一个 **if 语句** 由一个布尔表达式后跟一个或多个语句组成。    |
| [if...else 语句](https://www.runoob.com/csharp/csharp-if-else.html) | 一个 **if 语句** 后可跟一个可选的 **else 语句**，else 语句在布尔表达式为假时执行。 |
| [嵌套 if 语句](https://www.runoob.com/csharp/csharp-nested-if.html) | 您可以在一个 **if** 或 **else if** 语句内使用另一个 **if** 或 **else if** 语句。 |
| [switch 语句](https://www.runoob.com/csharp/csharp-switch.html) | 一个 **switch** 语句允许测试一个变量等于多个值时的情况。     |
| [嵌套 switch 语句](https://www.runoob.com/csharp/csharp-nested-switch.html) | 您可以在一个 **switch** 语句内使用另一个 **switch** 语句。   |



## ？:运算符

我们已经在前面的章节中讲解了 **条件运算符 ? :**，可以用来替代 **if...else** 语句。它的一般形式如下：

```
Exp1 ? Exp2 : Exp3;
```

其中，Exp1、Exp2 和 Exp3 是表达式。请注意，冒号的使用和位置。

? 表达式的值是由 Exp1 决定的。如果 Exp1 为真，则计算 Exp2 的值，结果即为整个 ? 表达式的值。如果 Exp1 为假，则计算 Exp3 的值，结果即为整个 ? 表达式的值。





# 循环

C# 提供了以下几种循环类型。点击链接查看每个类型的细节。

| 循环类型                                                     | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [while 循环](https://www.runoob.com/csharp/csharp-while-loop.html) | 当给定条件为真时，重复语句或语句组。它会在执行循环主体之前测试条件。 |
| [for/foreach 循环](https://www.runoob.com/csharp/csharp-for-loop.html) | 多次执行一个语句序列，简化管理循环变量的代码。               |
| [do...while 循环](https://www.runoob.com/csharp/csharp-do-while-loop.html) | 除了它是在循环主体结尾测试条件外，其他与 while 语句类似。    |
| [嵌套循环](https://www.runoob.com/csharp/csharp-nested-loops.html) | 您可以在 while、for 或 do..while 循环内使用一个或多个循环。  |



### foreach

使用foreach可以迭代数组或者一个集合对象。

#### 实例

```c#
class ForEachTest
{
    static void Main(string[] args)
    {
        int[] fibarray = new int[] {0, 1, 1, 2, 3, 5, 8, 13};
        foreach(int element in fibarray)
        {
            System.Console.WriteLine(element);
        }
        System.Console.WriteLine();
    }
}
```





# 封装

- **封装** 被定义为"把一个或多个项目封闭在一个物理的或者逻辑的包中"。
- 在面向对象程序设计方法论中，封装是为了防止对实现细节的访问。
- 抽象和封装是面向对象程序设计的相关特性。抽象允许相关信息可视化，封装则使开发者*实现所需级别的抽象*。
- C# 封装根据具体的需要，设置使用者的访问权限，并通过 **访问修饰符** 来实现
- 一个 **访问修饰符** 定义了一个类成员的范围和可见性。C# 支持的访问修饰符如下所示：
  - public：所有对象都可以访问；
  - private：对象本身在对象内部可以访问；
    - 类成员的默认访问修饰符为 **private**。
  - protected：只有该类对象及其子类对象可以访问
  - internal：同一个程序集的对象可以访问；
    - 类的默认访问标识符是 internal
  - protected internal：访问限于当前程序集或派生自包含类的类型





## internal 

- internal 访问说明符允许一个类将其成员变量和成员函数暴露给当前程序中的其他函数和对象
- 换句话说，带有 internal 访问修饰符的任何成员可以被定义在该成员所定义的应用程序内的任何类或方法访问。



```c#
using System;

namespace RectangleApplication
{
    class Rectangle
    {
        //成员变量
        internal double length;
        internal double width;
       
        double GetArea()
        {
            return length * width;
        }
       public void Display()
        {
            Console.WriteLine("长度： {0}", length);
            Console.WriteLine("宽度： {0}", width);
            Console.WriteLine("面积： {0}", GetArea());
        }
    }//end class Rectangle    
    class ExecuteRectangle
    {
        static void Main(string[] args)
        {
            Rectangle r = new Rectangle();
            r.length = 4.5;
            r.width = 3.5;
            r.Display();
            Console.ReadLine();
        }
    }
}
```





## protected internal

Protected Internal 访问修饰符允许在本类,派生类或者包含该类的程序集中访问。这也被用于实现继承。







# 方法

- 一个方法是把一些相关的语句组织在一起，用来执行一个任务的语句块。
- 每一个 C# 程序至少有一个带有 Main 方法的类
- 要使用一个方法，您需要：
  - 定义方法
  - 调用方法



## 定义方法

- 当定义一个方法时，从根本上说是在声明它的结构的元素

```
<Access Specifier> <Return Type> <Method Name>(Parameter List)
{
   Method Body
}
```

下面是方法的各个元素：

- **Access Specifier**：访问修饰符，这个决定了变量或方法对于另一个类的可见性。
- **Return type**：返回类型，一个方法可以返回一个值。返回类型是方法返回的值的数据类型。如果方法不返回任何值，则返回类型为 **void**。
- **Method name**：方法名称，是一个唯一的标识符，且是大小写敏感的。它不能与类中声明的其他标识符相同。
- **Parameter list**：参数列表，使用圆括号括起来，该参数是用来传递和接收方法的数据。参数列表是指方法的参数类型、顺序和数量。参数是可选的，也就是说，一个方法可能不包含参数。
- **Method body**：方法主体，包含了完成任务所需的指令集。



## 参数传递

- 当调用带有参数的方法时，您需要向方法传递参数。在 C# 中，有三种向方法传递参数的方式：

| 方式     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| 值参数   | 这种方式复制参数的实际值给函数的形式参数，实参和形参使用的是两个不同内存中的值。在这种情况下，当形参的值发生改变时，不会影响实参的值，从而保证了实参数据的安全。 |
| 引用参数 | 这种方式复制参数的内存位置的引用给形式参数。这意味着，当形参的值发生改变时，同时也改变实参的值。 |
| 输出参数 | 这种方式可以返回多个值。                                     |





## 按引用传递

- 引用参数是一个对变量的**内存位置的引用**。
- 当按引用传递参数时，与值参数不同的是，它不会为这些参数创建一个新的存储位置。
- 引用参数表示与提供给方法的实际参数具有相同的内存位置。
- 在 C# 中，使用 **ref** 关键字声明引用参数
- 提供给参数的变量**需要初始化**



```c#
using System;
namespace CalculatorApplication
{
    class NumberManipulator
    {
        public void swap(ref int x, ref int y)
        {
            int temp = x;
            x = y;
            y = temp;
        }
        
        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            int a = 100;
            int b = 200;
            
            n.swap(ref a, ref b);
        }
    }
}
```



## 按输出传递参数

- return 语句可用于只从函数中返回一个值。但是，可以使用 **输出参数** 来从函数中返回两个值。
- 输出参数会把方法输出的数据赋给自己，其他方面与引用参数相似。
- 调用代码时，传进去的变量数据会**丢失**，即变成了**未初始化状态**，所以调用时，有没有初始化没关系。
- 传进去的参数一定要在函数内部进行初始化



```c#
using System;
namespace CalculatorApplication
{
    class NumberManipulator
    {
        public void getValue(out int x)
        {
            // int temp = x; 报错，x 变成了未初始化状态。
            int temp = 5;
            x = temp;
        }
        
        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            int a = 100;
            
            n.getValue(out a); // a 变成了 5
        }
    }
}
```



- 提供给输出参数的变量**不需要赋值**。
- 当需要从一个参数没有指定初始值的方法中返回值时，输出参数特别有用。

```c#
using System;

namespace CalculatorApplication
{
   class NumberManipulator
   {
      public void getValues(out int x, out int y )
      {
          Console.WriteLine("请输入第一个值： ");
          x = Convert.ToInt32(Console.ReadLine());
          Console.WriteLine("请输入第二个值： ");
          y = Convert.ToInt32(Console.ReadLine());
      }
   
      static void Main(string[] args)
      {
         NumberManipulator n = new NumberManipulator();
         /* 局部变量定义 */
         int a , b;
         
         /* 调用函数来获取值 */
         n.getValues(out a, out b);

         Console.WriteLine("在方法调用之后，a 的值： {0}", a);
         Console.WriteLine("在方法调用之后，b 的值： {0}", b);
         Console.ReadLine();
      }
   }
}
```







# 可空类型

- Nullable



## 单问号和双问号

- 单问号用于对 int, double, bool 等无法直接赋值为 null 的数据类型进行 null 的赋值，意思是这个数据类型是 Nullable 类型的

  - ```c#
    int a = null; // 非法，无法从 null 转为 int
    int? a = null; // 合法
    int? i = 3;
    // 等同于：
    Nullable<int> i = new Nullable<int>(3);
    
    int i; // 默认为 0
    int? ii; // 默认为 null
    ```

  - 

- 双问号可用于判断一个变量在为 null 时返回一个指定的值
- 



## 可空类型

- C# 提供了一个特殊的数据类型，**nullable** 类型（可空类型），可空类型可以表示其基础值类型正常范围内的值，再加上一个 null 值。

  - 例如，Nullable< Int32 >，读作"可空的 Int32"，可以被赋值为 -2,147,483,648 到 2,147,483,647 之间的任意值，也可以被赋值为 null 值。

- 在处理数据库和其他**包含可能未赋值的元素的数据类型时**，将 null 赋值给数值类型或布尔型的功能特别有用。

  - 例如，数据库中的布尔型字段可以存储值 true 或 false，或者，该字段也可以未定义。

- 声明

  - ```
    <data_type> ? <variable_name> = null;
    ```

- 例子：

  - ```c#
    double? num = new double?();
    System.Console.WriteLine(num); 
    ```



## Null合并运算符(??)

- Null 合并运算符用于定义可空类型和引用类型的默认值
- Null 合并运算符为类型转换定义了一个预设值，以防可空类型的值为 Null。
- Null 合并运算符把操作数类型隐式转换为另一个可空（或不可空）的值类型的操作数的类型
- 如果第一个操作数的值为 null，则运算符返回第二个操作数的值，否则返回第一个操作数的值。



### 例子

```c#
using System;
namespace CalculatorApplication
{
    class NullablesAtShow
    {
        static void Main(string[] args)
        {
            double? num1 = null;
            double? num2 = 3.14;
            double num3;
            num3 = num1 ?? 5.34; // num1 如果为 null 则返回 5.34
            num3 = num2 ?? 5.34; // num2 不为 null，返回 num2
        }
    }
}
```







# 数组

- 所有的数组都是由连续的内存位置组成的。最低的地址对应第一个元素，最高的地址对应最后一个元素。
- 

## 声明

```
datatype[] arrayName
// 例如：double[] balance;
```



## 初始化

- 声明一个数组不会在内存中初始化数组
- 数组是一个引用类型，所以您需要使用 **new** 关键字来创建数组的实例。

```c#
double[] balance = new double[10]
```



## 赋值

- 通过使用索引号赋值给一个单独的数组元素

- 声明数组的同时给数组赋值，

  - ```c#
    double[] balance = {1.0, 2.0};
    ```

- 创建并初始化一个数组

  - ```c#
    int[] marks = new int[2]{1, 2};
    ```

- 在上述情况下，你也可以省略数组的大小

  - ```c#
    int[] marks = new int[]{1, 2};
    ```

- 赋值一个数组变量到另一个目标数组变量中。在这种情况下，目标和源会指向相同的内存位置：

  - ```c#
    int[] score = marks;
    ```

- 创建一个数组时，C# 编译器会根据数组类型隐式初始化每个数组元素为一个默认值。例如，int 数组的所有元素都会被初始化为 0。



## 访问

- 元素是通过带索引的数组名称来访问的。这是通过把元素的索引放置在数组名称后的方括号中来实现的。



## foreach循环

```c#
int[] n = new int[3]{1, 2, 3};

foreach(int j in n)
{
	int i = j-100;
}
```



## 多维数组

```c#
string[ , ] names;
int[ , , ] m;
```



### 二维数组

```c#
int[,] a = new int[3,4] = {{0, 0, 0, 0},{0, 0, 0, 0},{0, 0, 0, 0},{0, 0, 0, 0}};
```



#### 访问

```c#
int val = a[2,3];
```



## 交错数组

- 交错数组是数组的数组。
- 交错数组是一维数组。



```c#
int[][] scores = new int[5][];
for(int i=0; i<scores.Length; i++)
{
	scores[i] = new int[4];
}

int [][] s = new int[2][]{new int[]{1,2}, new int[]{1,2,3}};
```





## 传递数组给函数

- 在 C# 中，可以传递数组作为函数的参数。
- 可以通过指定不带索引的数组名称来给函数传递一个指向数组的指针。



```c#
class MyArray
{
    double getAverage(int[] arr, int size)
    {
        // size = arr.Length;
        return 1.0;
    }
    
    static void Main(string[] args)
    {
        MyArray a = new MyArray();
        int [] balance = new int[]{1, 2};
        double avg;
        avg = a.getAverage(balance, 2);
    }
}

/*
//传交错数组
double getAverage(int[][] arr)
{
	return 1.0;
}
*/
```





## 参数数组

- 有时，当声明一个方法时，不能确定要传递给函数作为参数的参数数目。C# 参数数组解决了这个问题，参数数组通常用于传递未知数量的参数给函数。
- 在使用数组作为形参时，C# 提供了 params 关键字，使调用数组为形参的方法时，既可以传递数组实参，也可以传递一组数组元素

```c#
class MyArray
{
    double getAverage(params int[] arr)
    {
        return 1.0;
    }
    
    static void Main(string[] args)
    {
        MyArray a = new MyArray();
        double avg;
        avg = a.getAverage(1, 2, 3, 4);
    }
}
```





## Array类

- Array 类是 C# 中所有数组的基类，它是在 System 命名空间中定义。Array 类提供了各种用于数组的属性和方法。



### Array 类的属性

下表列出了 Array 类中一些最常用的属性：

| 序号 | 属性 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **IsFixedSize** 获取一个值，该值指示数组是否带有固定大小。   |
| 2    | **IsReadOnly** 获取一个值，该值指示数组是否只读。            |
| 3    | **Length** 获取一个 32 位整数，该值表示所有维度的数组中的元素总数。 |
| 4    | **LongLength** 获取一个 64 位整数，该值表示所有维度的数组中的元素总数。 |
| 5    | **Rank** 获取数组的秩（维度）。                              |





### Array类的方法

下表列出了 Array 类中一些最常用的方法：

| 序号 | 方法 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **Clear** 根据元素的类型，设置数组中某个范围的元素为零、为 false 或者为 null。 |
| 2    | **Copy(Array, Array, Int32)** 从数组的第一个元素开始复制某个范围的元素到另一个数组的第一个元素位置。长度由一个 32 位整数指定。 |
| 3    | **CopyTo(Array, Int32)** 从当前的一维数组中复制所有的元素到一个指定的一维数组的指定索引位置。索引由一个 32 位整数指定。 |
| 4    | **GetLength** 获取一个 32 位整数，该值表示指定维度的数组中的元素总数。 |
| 5    | **GetLongLength** 获取一个 64 位整数，该值表示指定维度的数组中的元素总数。 |
| 6    | **GetLowerBound** 获取数组中指定维度的下界。                 |
| 7    | **GetType** 获取当前实例的类型。从对象（Object）继承。       |
| 8    | **GetUpperBound** 获取数组中指定维度的上界。                 |
| 9    | **GetValue(Int32)** 获取一维数组中指定位置的值。索引由一个 32 位整数指定。 |
| 10   | **IndexOf(Array, Object)** 搜索指定的对象，返回整个一维数组中第一次出现的索引。 |
| 11   | **Reverse(Array)** 逆转整个一维数组中元素的顺序。            |
| 12   | **SetValue(Object, Int32)** 给一维数组中指定位置的元素设置值。索引由一个 32 位整数指定。 |
| 13   | **Sort(Array)** 使用数组的每个元素的 Comparable 实现来排序整个**一维数组**中的元素。 |
| 14   | **ToString** 返回一个表示当前对象的字符串。从对象（Object）继承。 |



### 实例

```c#
using System;
namespace ArrayApplication
{
    class MyArray
    {
       
        static void Main(string[] args)
        {
            int[] list = { 34, 72, 13, 44, 25, 30, 10 };

            Console.Write("原始数组： ");
            foreach (int i in list)
            {
                Console.Write(i + " ");
            }
            Console.WriteLine();
           
            // 逆转数组
            Array.Reverse(list);
            Console.Write("逆转数组： ");
            foreach (int i in list)
            {
                Console.Write(i + " ");
            }
            Console.WriteLine();
           
            // 排序数组
            Array.Sort(list);
            Console.Write("排序数组： ");
            foreach (int i in list)
            {
                Console.Write(i + " ");
            }
            Console.WriteLine();

           Console.ReadKey();
        }
    }
}
```







# 字符串

- 可以使用字符数组来表示字符串
- 更常见的做法是使用 **string** 关键字来声明一个字符串变量。string 关键字是 **System.String** 类的别名



### 创建

可以使用以下方法之一来创建 string 对象：

- 通过给 String 变量指定一个字符串
- 通过使用 String 类构造函数
- 通过使用字符串串联运算符（ + ）
- 通过检索属性或调用一个返回字符串的方法
- 通过格式化方法来转换一个值或对象为它的字符串表示形式

```c#
using System;

namespace StringApplication
{
    class Program
    {
        static void Main(string[] args)
        {
           //字符串，字符串连接
            string fname, lname;
            fname = "Rowan";
            lname = "Atkinson";

            string fullname = fname + lname;
            Console.WriteLine("Full Name: {0}", fullname);

            //通过使用 string 构造函数
            char[] letters = { 'H', 'e', 'l', 'l','o' };
            string greetings = new string(letters);
            Console.WriteLine("Greetings: {0}", greetings);

            //方法返回字符串
            string[] sarray = { "Hello", "From", "Tutorials", "Point" };
            string message = String.Join(" ", sarray);
            Console.WriteLine("Message: {0}", message);

            //用于转化值的格式化方法
            DateTime waiting = new DateTime(2012, 10, 10, 17, 58, 1);
            string chat = String.Format("Message sent at {0:t} on {0:D}",
            waiting);
            Console.WriteLine("Message: {0}", chat);
            Console.ReadKey() ;
        }
    }
}

/*
Full Name: RowanAtkinson
Greetings: Hello
Message: Hello From Tutorials Point
Message: Message sent at 17:58 on Wednesday, 10 October 2012
*/
```





## 属性

String 类有以下两个属性：

| 序号 | 属性名称 & 描述                                              |
| :--- | :----------------------------------------------------------- |
| 1    | **Chars** 在当前 *String* 对象中获取 *Char* 对象的指定位置。 |
| 2    | **Length** 在当前的 *String* 对象中获取字符数。              |



## 方法

String 类有许多方法用于 string 对象的操作。下面的表格提供了一些最常用的方法：

| 序号 | 方法名称 & 描述                                              |
| :--- | :----------------------------------------------------------- |
| 1    | **public static int Compare( string strA, string strB )** 比较两个指定的 string 对象，并返回一个表示它们在排列顺序中相对位置的整数。该方法区分大小写。 |
| 2    | **public static int Compare( string strA, string strB, bool ignoreCase )** 比较两个指定的 string 对象，并返回一个表示它们在排列顺序中相对位置的整数。但是，如果布尔参数为真时，该方法不区分大小写。 |
| 3    | **public static string Concat( string str0, string str1 )** 连接两个 string 对象。 |
| 4    | **public static string Concat( string str0, string str1, string str2 )** 连接三个 string 对象。 |
| 5    | **public static string Concat( string str0, string str1, string str2, string str3 )** 连接四个 string 对象。 |
| 6    | **public bool Contains( string value )** 返回一个表示指定 string 对象是否出现在字符串中的值。 |
| 7    | **public static string Copy( string str )** 创建一个与指定字符串具有相同值的新的 String 对象。 |
| 8    | **public void CopyTo( int sourceIndex, char[] destination, int destinationIndex, int count )** 从 string 对象的指定位置开始复制指定数量的字符到 Unicode 字符数组中的指定位置。 |
| 9    | **public bool EndsWith( string value )** 判断 string 对象的结尾是否匹配指定的字符串。 |
| 10   | **public bool Equals( string value )** 判断当前的 string 对象是否与指定的 string 对象具有相同的值。 |
| 11   | **public static bool Equals( string a, string b )** 判断两个指定的 string 对象是否具有相同的值。 |
| 12   | **public static string Format( string format, Object arg0 )** 把指定字符串中一个或多个格式项替换为指定对象的字符串表示形式。 |
| 13   | **public int IndexOf( char value )** 返回指定 Unicode 字符在当前字符串中第一次出现的索引，索引从 0 开始。 |
| 14   | **public int IndexOf( string value )** 返回指定字符串在该实例中第一次出现的索引，索引从 0 开始。 |
| 15   | **public int IndexOf( char value, int startIndex )** 返回指定 Unicode 字符从该字符串中指定字符位置开始搜索第一次出现的索引，索引从 0 开始。 |
| 16   | **public int IndexOf( string value, int startIndex )** 返回指定字符串从该实例中指定字符位置开始搜索第一次出现的索引，索引从 0 开始。 |
| 17   | **public int IndexOfAny( char[] anyOf )** 返回某一个指定的 Unicode 字符数组中任意字符在该实例中第一次出现的索引，索引从 0 开始。 |
| 18   | **public int IndexOfAny( char[] anyOf, int startIndex )** 返回某一个指定的 Unicode 字符数组中任意字符从该实例中指定字符位置开始搜索第一次出现的索引，索引从 0 开始。 |
| 19   | **public string Insert( int startIndex, string value )** 返回一个新的字符串，其中，指定的字符串被插入在当前 string 对象的指定索引位置。 |
| 20   | **public static bool IsNullOrEmpty( string value )** 指示指定的字符串是否为 null 或者是否为一个空的字符串。 |
| 21   | **public static string Join( string separator, string[] value )** 连接一个字符串数组中的所有元素，使用指定的分隔符分隔每个元素。 |
| 22   | **public static string Join( string separator, string[] value, int startIndex, int count )** 连接接一个字符串数组中的指定位置开始的指定元素，使用指定的分隔符分隔每个元素。 |
| 23   | **public int LastIndexOf( char value )** 返回指定 Unicode 字符在当前 string 对象中最后一次出现的索引位置，索引从 0 开始。 |
| 24   | **public int LastIndexOf( string value )** 返回指定字符串在当前 string 对象中最后一次出现的索引位置，索引从 0 开始。 |
| 25   | **public string Remove( int startIndex )** 移除当前实例中的所有字符，从指定位置开始，一直到最后一个位置为止，并返回字符串。 |
| 26   | **public string Remove( int startIndex, int count )** 从当前字符串的指定位置开始移除指定数量的字符，并返回字符串。 |
| 27   | **public string Replace( char oldChar, char newChar )** 把当前 string 对象中，所有指定的 Unicode 字符替换为另一个指定的 Unicode 字符，并返回新的字符串。 |
| 28   | **public string Replace( string oldValue, string newValue )** 把当前 string 对象中，所有指定的字符串替换为另一个指定的字符串，并返回新的字符串。 |
| 29   | **public string[] Split( params char[] separator )** 返回一个字符串数组，包含当前的 string 对象中的子字符串，子字符串是使用指定的 Unicode 字符数组中的元素进行分隔的。 |
| 30   | **public string[] Split( char[] separator, int count )** 返回一个字符串数组，包含当前的 string 对象中的子字符串，子字符串是使用指定的 Unicode 字符数组中的元素进行分隔的。int 参数指定要返回的子字符串的最大数目。 |
| 31   | **public bool StartsWith( string value )** 判断字符串实例的开头是否匹配指定的字符串。 |
| 32   | **public char[] ToCharArray()** 返回一个带有当前 string 对象中所有字符的 Unicode 字符数组。 |
| 33   | **public char[] ToCharArray( int startIndex, int length )** 返回一个带有当前 string 对象中所有字符的 Unicode 字符数组，从指定的索引开始，直到指定的长度为止。 |
| 34   | **public string ToLower()** 把字符串转换为小写并返回。       |
| 35   | **public string ToUpper()** 把字符串转换为大写并返回。       |
| 36   | **public string Trim()** 移除当前 String 对象中的所有前导空白字符和后置空白字符。 |

上面的方法列表并不详尽，请访问 MSDN 库，查看完整的方法列表和 String 类构造函数。





## 格式化日期

```c#
DateTime dt = new DateTime(2017,4,1,13,16,32,108);
string.Format("{0:y yy yyy yyyy}",dt); //17 17 2017 2017
string.Format("{0:M MM MMM MMMM}", dt);//4  04 四月 四月
string.Format("{0:d dd ddd dddd}", dt);//1  01 周六 星期六
string.Format("{0:t tt}", dt);//下 下午
string.Format("{0:H HH}", dt);//13 13
string.Format("{0:h hh}", dt);//1  01
string.Format("{0:m mm}", dt);//16 16
string.Format("{0:s ss}", dt);//32 32
string.Format("{0:F FF FFF FFFF FFFFF FFFFFF FFFFFFF}", dt);//1 1  108 108  108   108    108
string.Format("{0:f ff fff ffff fffff ffffff fffffff}", dt);//1 10 108 1080 10800 108000 1080000
string.Format("{0:z zz zzz}", dt);//+8 +08 +08:00

string.Format("{0:yyyy/MM/dd HH:mm:ss.fff}",dt);　　//2017/04/01 13:16:32.108
string.Format("{0:yyyy/MM/dd dddd}", dt);　　　　　　//2017/04/01 星期六
string.Format("{0:yyyy/MM/dd dddd tt hh:mm}", dt); //2017/04/01 星期六 下午 01:16
string.Format("{0:yyyyMMdd}", dt);　　　　　　　　　//20170401
string.Format("{0:yyyy-MM-dd HH:mm:ss.fff}", dt);　//2017-04-01 13:16:32.108
```

```c#
DateTime dt = new DateTime(2017,4,1,13,16,32,108);
dt.ToString("y yy yyy yyyy");//17 17 2017 2017
dt.ToString("M MM MMM MMMM");//4  04 四月 四月
dt.ToString("d dd ddd dddd");//1  01 周六 星期六
dt.ToString("t tt");//下 下午
dt.ToString("H HH");//13 13
dt.ToString("h hh");//1  01
dt.ToString("m mm");//16 16
dt.ToString("s ss");//32 32
dt.ToString("F FF FFF FFFF FFFFF FFFFFF FFFFFFF");//1 1  108 108  108   108    108
dt.ToString("f ff fff ffff fffff ffffff fffffff");//1 10 108 1080 10800 108000 1080000
dt.ToString("z zz zzz");//+8 +08 +08:00

dt.ToString("yyyy/MM/dd HH:mm:ss.fff");　//2017/04/01 13:16:32.108
dt.ToString("yyyy/MM/dd dddd");　　　　　　//2017/04/01 星期六
dt.ToString("yyyy/MM/dd dddd tt hh:mm"); //2017/04/01 星期六 下午 01:16
dt.ToString("yyyyMMdd");　　　　　　　　　//20170401
dt.ToString("yyyy-MM-dd HH:mm:ss.fff");　//2017-04-01 13:16:32.108
```





# 结构体

```c#
using System;
using System.Text;
     
struct Books
{
   public string title;
   public string author;
   public string subject;
   public int book_id;
};  

public class testStructure
{
   public static void Main(string[] args)
   {

      Books Book1;        /* 声明 Book1，类型为 Books */
      Books Book2;        /* 声明 Book2，类型为 Books */

      /* book 1 详述 */
      Book1.title = "C Programming";
      Book1.author = "Nuha Ali";
      Book1.subject = "C Programming Tutorial";
      Book1.book_id = 6495407;

      /* book 2 详述 */
      Book2.title = "Telecom Billing";
      Book2.author = "Zara Ali";
      Book2.subject =  "Telecom Billing Tutorial";
      Book2.book_id = 6495700;

      /* 打印 Book1 信息 */
      Console.WriteLine( "Book 1 title : {0}", Book1.title);
      Console.WriteLine("Book 1 author : {0}", Book1.author);
      Console.WriteLine("Book 1 subject : {0}", Book1.subject);
      Console.WriteLine("Book 1 book_id :{0}", Book1.book_id);

      /* 打印 Book2 信息 */
      Console.WriteLine("Book 2 title : {0}", Book2.title);
      Console.WriteLine("Book 2 author : {0}", Book2.author);
      Console.WriteLine("Book 2 subject : {0}", Book2.subject);
      Console.WriteLine("Book 2 book_id : {0}", Book2.book_id);      

      Console.ReadKey();

   }
}
```



## 特点

在 C# 中的结构与传统的 C 或 C++ 中的结构不同。C# 中的结构有以下特点：

- 结构可带有方法、字段、索引、属性、运算符方法和事件。
- 结构可定义构造函数，但不能定义析构函数。但是，您不能为结构定义无参构造函数。无参构造函数(默认)是自动定义的，且不能被改变。
- 与类不同，结构不能继承其他的结构或类。
- 结构不能作为其他结构或类的基础结构。
- 结构可实现一个或多个接口。
- 结构成员不能指定为 abstract、virtual 或 protected。
- 当您使用 **New** 操作符创建一个结构对象时，会调用适当的构造函数来创建结构。与类不同，结构可以不使用 New 操作符即可被实例化。
- 如果不使用 New 操作符，只有在所有的字段都被初始化之后，字段才被赋值，对象才被使用。



## 类vs结构

类和结构有以下几个基本的不同点：

- 类是引用类型，结构是值类型。
- 结构不支持继承。
- 结构不能声明默认的构造函数。
- 结构体中声明的字段无法赋予初值，类可以
  - 结构体中，`private int a = 1;`，报错
- 结构体的构造函数中，必须为结构体所有字段赋值，类的构造函数无此限制
- 类的对象是存储在堆空间中，结构存储在栈中。堆空间大，但访问速度较慢，栈空间小，访问速度相对更快。故而，当我们描述一个轻量级对象的时候，结构可提高效率，成本更低。当然，这也得从需求出发，假如我们在传值的时候希望传递的是对象的引用地址而不是对象的拷贝，就应该使用类了





# 枚举

- 枚举是一组命名整型常量。枚举类型是使用 **enum** 关键字声明的。

- C# 枚举是值类型。换句话说，枚举包含自己的值，且不能继承或传递继承。

- 枚举列表中的每个符号代表一个整数值，一个比它前面的符号大的整数值。默认情况下，第一个枚举符号的值是 0.例如：

- ```c#
  enum Days { Sun, Mon, tue, Wed, thu, Fri, Sat };
  ```

- 





# 类

当你定义一个类时，你定义了一个数据类型的蓝图。这实际上并没有定义任何的数据，但它定义了类的名称意味着什么，也就是说，类的对象由什么组成及在这个对象上可执行什么操作。对象是类的实例。构成类的方法和变量称为类的成员。



## 定义

```
<access specifier> class  class_name
{
    // member variables
    <access specifier> <data type> variable1;
    <access specifier> <data type> variable2;
    ...
    <access specifier> <data type> variableN;
    // member methods
    <access specifier> <return type> method1(parameter_list)
    {
        // method body
    }
    <access specifier> <return type> method2(parameter_list)
    {
        // method body
    }
    ...
    <access specifier> <return type> methodN(parameter_list)
    {
        // method body
    }
}
```

请注意：

- 访问标识符 <access specifier> 指定了对类及其成员的访问规则。如果没有指定，则使用默认的访问标识符。类的默认访问标识符是 **internal**，成员的默认访问标识符是 **private**。
  - 带有 internal 访问修饰符的任何成员可以被定义在该成员所定义的应用程序内的任何类或方法访问。
- 数据类型 <data type> 指定了变量的类型，返回类型 <return type> 指定了返回的方法返回的数据类型。
- 如果要访问类的成员，你要使用点（.）运算符。
- 点运算符链接了对象的名称和成员的名称。



## 析构函数

- 析构函数不能继承或重载



## 静态成员

- 静态变量可在成员函数或类的定义外部进行初始化。你也可以在类的定义内部初始化静态变量。

```c#
class Test
{
	static int a = 1;//
	a = 2;//出错，当前上下文中不存在名称 "a"
	pirvate void Plus()
	{
		a=1;
		a++;
	}
}
```





# 继承

- 一个类可以派生自多个类或接口，这意味着它可以从多个基类或接口继承数据和函数。

```
<访问修饰符符> class <基类>
{
 ...
}
class <派生类> : <基类>
{
 ...
}
```



## 基类初始化

- 派生类继承了基类的成员变量和成员方法。因此父类对象应在子类对象创建之前被创建。您可以在成员初始化列表中进行父类的初始化。

```c#
namespace TestConsole
{
    class Base
    {
        private int a;
        private int b;
        public Base(int a, int b)
        {
            a = 1;
            b = 2;
        }
    }

    class Derive : Base
    {
        public Derive(int a, int b) : base(a, b) { }
    }
}
```



## 多重继承

- 多重继承指的是一个类别可以同时从多于一个父类继承行为与特征的功能。与单一继承相对，单一继承指一个类别只可以继承自一个父类。
- **C# 不支持多重继承**。但是，您可以使用接口来实现多重继承

```c#
   class Shape
   {
      public void setWidth(int w)
      {
         width = w;
      }
      public void setHeight(int h)
      {
         height = h;
      }
      protected int width;
      protected int height;
   }

   // 基类 PaintCost
   public interface PaintCost
   {
      int getCost(int area);

   }
   // 派生类
   class Rectangle : Shape, PaintCost
   {
      public int getArea()
      {
         return (width * height);
      }
      public int getCost(int area)
      {
         return area * 70;
      }
   }
```





# 多态

- 在面向对象编程范式中，多态性往往表现为"一个接口，多个功能"。
- 多态性可以是静态的或动态的。在**静态多态性**中，函数的响应是在编译时发生的。在**动态多态性**中，函数的响应是在运行时发生的。
- 在 C# 中，**每个类型**都是多态的，因为包括用户定义类型在内的所有类型都继承自 Object。



## 静态多态

在编译时，函数和对象的连接机制被称为**早期绑定**，也被称为静态绑定。C# 提供了两种技术来实现静态多态性。分别为：

- 函数重载
- 运算符重载



### 函数重载

- 可以在同一个范围内对相同的函数名有多个定义。函数的定义必须彼此不同，可以是参数列表中的参数类型不同，也可以是参数个数不同。不能重载只有返回类型不同的函数声明。



## 动态多态

- C# 允许您使用关键字 **abstract** 创建抽象类，用于提供接口的部分类的实现。

- 当一个派生类继承自该抽象类时，实现即完成

- **抽象类**包含抽象方法，抽象方法可被派生类实现

- 下面是有关抽象类的一些规则：

  - 您不能创建一个抽象类的实例。

  - 您不能在一个抽象类外部声明一个抽象方法。

  - 通过在类定义前面放置关键字 **sealed**，可以将类声明为**密封类**。当一个类被声明为 **sealed** 时，它不能被继承。抽象类不能被声明为 sealed。

    - ```c#
      public sealed class Test{}
      ```

- ```c#
  abstract class Shape
  {
  	abstract public int area();
  }
  
  class Rectangle : Shape
  {
      public override int area(){}
  }
  ```



当有一个定义在类中的函数需要在继承类中实现时，可以使用**虚方法**。

- 虚方法是使用关键字 **virtual** 声明的。

  虚方法可以在不同的继承类中有不同的实现。

  对虚方法的调用是在**运行时**发生的。

  动态多态性是通过 **抽象类** 和 **虚方法** 实现的。



# 运算符重载

- 可以重定义或重载 C# 中内置的运算符
- 重载运算符是具有特殊名称的函数，是通过关键字 **operator** 后跟运算符的符号来定义的
- 与其他函数一样，重载运算符有返回类型和参数列表。

```c#
public static Box Operator+(Box b, Box c)
{
	Box box = new Box();
    box.length = b.length + c.length;
    return box;
}
```



## 可重载和不可重载的运算符

下表描述了 C# 中运算符重载的能力：

| 运算符                                    | 描述                                         |
| :---------------------------------------- | :------------------------------------------- |
| +, -, !, ~, ++, --                        | 这些一元运算符只有一个操作数，且可以被重载。 |
| +, -, *, /, %                             | 这些二元运算符带有两个操作数，且可以被重载。 |
| ==, !=, <, >, <=, >=                      | 这些比较运算符可以被重载。                   |
| &&, \|\|                                  | 这些条件逻辑运算符不能被直接重载。           |
| +=, -=, *=, /=, %=                        | 这些赋值运算符不能被重载。                   |
| =, ., ?:, ->, **new**, is, sizeof, typeof | 这些运算符不能被重载。                       |





# 接口

- 接口定义了所有类继承接口时应遵循的语法合同。
- 接口定义了语法合同 **"是什么"** 部分，派生类定义了语法合同 **"怎么做"** 部分。
- 接口定义了属性、方法和事件，这些都是接口的成员。
- 接口只包含了成员的声明。成员的定义是派生类的责任。
- 接口使得实现接口的类或结构在形式上保持一致。
- 抽象类在某种程度上与接口类似，但是，它们大多只是用在当只有少数方法由基类声明由派生类实现时。



## 定义

- 使用 **interface**声明，

- 默认 **public **

- 接口通常 **以 I 开头**，

- ```c#
  interface IMyInterface
  {
      void Test();
  }
  ```



## 继承

- 需要实现接口的方法，而且方法名必须与接口定义的方法名一致。
- 如果一个接口继承了其他接口，那么实现类或者结构就需要实现所有接口的成员



## 例子

```c#
using System;

interface IParentInterface
{
    void ParentInterfaceMethod();
}

interface IMyInterface : IParentInterface
{
    void MethodToImplement();
}

class InterfaceImplementer : IMyInterface
{
    static void Main()
    {
        InterfaceImplementer iImp = new InterfaceImplementer();
        iImp.MethodToImplement();
        iImp.ParentInterfaceMethod();
    }

    public void MethodToImplement()
    {
        Console.WriteLine("MethodToImplement() called.");
    }

    public void ParentInterfaceMethod()
    {
        Console.WriteLine("ParentInterfaceMethod() called.");
    }
}
```





# 命名空间

- 设计目的是提供一种让一组名称与其他名称分隔开的方式
- 在一个命名空间中声明的类的名称与另一个命名空间中声明的相同的类的名称不冲突



## 定义

- 以关键字 **namespace** 开始



## 调用

- ```c#
  using System;
  namespace first_space
  {
     class namespace_cl
     {
        public void func()
        {
           Console.WriteLine("Inside first_space");
        }
     }
  }
  namespace second_space
  {
     class namespace_cl
     {
        public void func()
        {
           Console.WriteLine("Inside second_space");
        }
     }
  }  
  class TestClass
  {
     static void Main(string[] args)
     {
        first_space.namespace_cl fc = new first_space.namespace_cl();
        second_space.namespace_cl sc = new second_space.namespace_cl();
        fc.func();
        sc.func();
        Console.ReadKey();
     }
  ```



## using 关键字

- 表明程序使用的是给定命名空间中的名称

- 使用之后就不用在前面加上命名空间的名称

- ```c#
  // 起别名
  using ElseName = This.Is.Very.Long.NameSpaceName;
  ```

- ```c#
  // 其他用法
  // 允许指定资源的对象应当何时释放资源
  // 使用的对象必须实现 IDisposable 接口，自方法提供了 Dispose 方法，释放资源
  
  // 1
  Font font1 = new Font("Arial", 10.0f);
  using (font1)
  {
      // ...
  }
  
  // 2
  using (Font font2 = new Font("Arial", 10.0f))
  {
      // ...
  }
  
  // 3，初始化多个，但类型必须相同
  using (Font font3 = new Font("Arial", 10.0f), font4 = new Font("Arial", 10.0f))
  {
      // ...
  }
  ```

- 



## 嵌套命名空间

- 使用点(**.**)运算符访问嵌套的命名空间的成员

```c#
using SomeNameSpace;
using SomeNameSpace.Nested;

namespace SomeNameSpace
{
    // ...
    namespace Nested
    {
	
    }
}
```









# 预处理器指令

- 预处理器指令指导编译器在实际编译开始之前对信息进行预处理
- 所有的预处理器指令都是以 # 开始。且在一行上，只有空白字符可以出现在预处理器指令之前。
- 预处理器指令不是语句，所以它们不以分号（;）结束
- C# 编译器没有一个单独的预处理器，但是，指令被处理时就像是有一个单独的预处理器一样。
- 在 C# 中，预处理器指令用于在条件编译中起作用。与 C 和 C++ 不同的是，它们不是用来创建宏。一个预处理器指令必须是该行上的唯一指令。



## 预处理器指令列表

| 预处理器指令 | 描述                                                         |
| :----------- | :----------------------------------------------------------- |
| #define      | 它用于定义一系列成为符号的字符。                             |
| #undef       | 它用于取消定义符号。                                         |
| #if          | 它用于测试符号是否为真。                                     |
| #else        | 它用于创建复合条件指令，与 #if 一起使用。                    |
| #elif        | 它用于创建复合条件指令。                                     |
| #endif       | 指定一个条件指令的结束。                                     |
| #line        | 它可以让您修改编译器的行数以及（可选地）输出错误和警告的文件名。 |
| #error       | 它允许从代码的指定位置生成一个错误。                         |
| #warning     | 它允许从代码的指定位置生成一级警告。                         |
| #region      | 它可以让您在使用 Visual Studio Code Editor 的大纲特性时，指定一个可展开或折叠的代码块。 |
| #endregion   | 它标识着 #region 块的结束。                                  |



## #define

- 放在文件开头

- \#define 预处理器指令创建符号常量。

- \#define 允许您定义一个符号，这样，通过使用符号作为传递给 #if 指令的表达式，表达式将返回 true。

- ```c#
  #define symbol
  ```



```c#
#define PI
using System;
namespace PreprocessorDAppl
{
    class Program
    {
		static void Main(string[] args)
        {
			#if(PI)
                Console.WriteLine(" ");
            #else
                Console.WriteLine(" ");
            #endif
                Console.ReadKey();
        }
    }
}
```



## 条件指令

- 条件指令用于测试符号是否为真。如果为真，编译器会执行 #if 和下一个指令之间的代码。
- 条件指令用于在调试版本或编译指定配置时编译代码
- 一个以 **#if** 指令开始的条件指令，必须显示地以一个 **#endif** 指令终止。





# 正则表达式

- 一种匹配输入文本的模式
- 模式由一个或多个字符、运算符和结构组成



## 定义

下面列出了用于定义正则表达式的各种类别的字符、运算符和结构。

- 字符转义
- 字符类
- 定位点
- 分组构造
- 限定符
- 反向引用构造
- 备用构造
- 替换
- 杂项构造



## 字符类

字符类与一组字符中的任何一个字符匹配。

下表列出了字符类：

| 字符类                 | 描述                                                         | 模式   | 匹配                                       |
| :--------------------- | :----------------------------------------------------------- | :----- | :----------------------------------------- |
| **[character_group]**  | 匹配 character_group 中的任何单个字符。 默认情况下，匹配区分大小写。 | [mn]   | "mat" 中的 "m"，"moon" 中的 "m" 和 "n"     |
| **[^character_group]** | 非：与不在 character_group 中的任何单个字符匹配。 默认情况下，character_group 中的字符区分大小写。 | [^aei] | "avail" 中的 "v" 和 "l"                    |
| **[ first - last ]**   | 字符范围：与从 first 到 last 的范围中的任何单个字符匹配。    | [b-d]  | [b-d]irds 可以匹配 Birds、 Cirds、 Dirds   |
| **.**                  | 通配符：与除 \n 之外的任何单个字符匹配。 若要匹配原意句点字符（. 或 \u002E），您必须在该字符前面加上转义符 (\.)。 | a.e    | "have" 中的 "ave"， "mate" 中的 "ate"      |
| **\p{ name }**         | 与 *name* 指定的 Unicode 通用类别或命名块中的任何单个字符匹配。 | \p{Lu} | "City Lights" 中的 "C" 和 "L"              |
| **\P{ name }**         | 与不在 *name* 指定的 Unicode 通用类别或命名块中的任何单个字符匹配。 | \P{Lu} | "City" 中的 "i"、 "t" 和 "y"               |
| **\w**                 | 与任何单词字符匹配。                                         | \w     | "Room#1" 中的 "R"、 "o"、 "m" 和 "1"       |
| **\W**                 | 与任何非单词字符匹配。                                       | \W     | "Room#1" 中的 "#"                          |
| **\s**                 | 与任何空白字符匹配。                                         | \w\s   | "ID A1.3" 中的 "D "                        |
| **\S**                 | 与任何非空白字符匹配。                                       | \s\S   | "int __ctr" 中的 " _"                      |
| **\d**                 | 与任何十进制数字匹配。                                       | \d     | "4 = IV" 中的 "4"                          |
| **\D**                 | 匹配不是十进制数的任意字符。                                 | \D     | "4 = IV" 中的 " "、 "="、 " "、 "I" 和 "V" |





## 定义点

定位点或原子零宽度断言会使匹配成功或失败，具体取决于字符串中的当前位置，但它们不会使引擎在字符串中前进或使用字符。

下表列出了定位点：

| 断言   | 描述                                                         | 模式     | 匹配                                            |
| :----- | :----------------------------------------------------------- | :------- | :---------------------------------------------- |
| **^**  | 匹配必须从字符串或一行的开头开始。                           | ^\d{3}   | "567-777-" 中的 "567"                           |
| **$**  | 匹配必须出现在字符串的末尾或出现在行或字符串末尾的 **\n** 之前。 | -\d{4}$  | "8-12-2012" 中的 "-2012"                        |
| **\A** | 匹配必须出现在字符串的开头。                                 | \A\w{4}  | "Code-007-" 中的 "Code"                         |
| **\Z** | 匹配必须出现在字符串的末尾或出现在字符串末尾的 **\n** 之前。 | -\d{3}\Z | "Bond-901-007" 中的 "-007"                      |
| **\z** | 匹配必须出现在字符串的末尾。                                 | -\d{3}\z | "-901-333" 中的 "-333"                          |
| **\G** | 匹配必须出现在上一个匹配结束的地方。                         | \G\(\d\) | "(1)(3)(5)[7](9)" 中的 "(1)"、 "(3)" 和 "(5)"   |
| **\b** | 匹配一个单词边界，也就是指单词和空格间的位置。               | er\b     | 匹配"never"中的"er"，但不能匹配"verb"中的"er"。 |
| **\B** | 匹配非单词边界。                                             | er\B     | 匹配"verb"中的"er"，但不能匹配"never"中的"er"。 |



## 分组构造

分组构造描述了正则表达式的子表达式，通常用于捕获输入字符串的子字符串。

这一部分比较难于理解，可以阅读 **[正则表达式-选择](https://www.runoob.com/regexp/regexp-syntax.html#reg-select)** 、**[正则表达式的先行断言(lookahead)和后行断言(lookbehind)](https://www.runoob.com/w3cnote/reg-lookahead-lookbehind.html)** 帮助理解。

下表列出了分组构造：

| 分组构造                             | 描述                                                 | 模式                                                         | 匹配                                                         |
| :----------------------------------- | :--------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **( subexpression )**                | 捕获匹配的子表达式并将其分配到一个从零开始的序号中。 | (\w)\1                                                       | "deep" 中的 "ee"                                             |
| **(?< name >subexpression)**         | 将匹配的子表达式捕获到一个命名组中。                 | (?< double>\w)\k< double>                                    | "deep" 中的 "ee"                                             |
| **(?< name1 -name2 >subexpression)** | 定义平衡组定义。                                     | (((?'Open'\()[^\(\)]*)+((?'Close-Open'\))[^\(\)]*)+)*(?(Open)(?!))$ | "3+2^((1-3)*(3-1))" 中的 "((1-3)*(3-1))"                     |
| **(?: subexpression)**               | 定义非捕获组。                                       | Write(?:Line)?                                               | "Console.WriteLine()" 中的 "WriteLine"                       |
| **(?imnsx-imnsx:subexpression)**     | 应用或禁用 *subexpression* 中指定的选项。            | A\d{2}(?i:\w+)\b                                             | "A12xl A12XL a12xl" 中的 "A12xl" 和 "A12XL"                  |
| **(?= subexpression)**               | 零宽度正预测先行断言。                               | \w+(?=\.)                                                    | "He is. The dog ran. The sun is out." 中的 "is"、 "ran" 和 "out" |
| **(?! subexpression)**               | 零宽度负预测先行断言。                               | \b(?!un)\w+\b                                                | "unsure sure unity used" 中的 "sure" 和 "used"               |
| **(?<=subexpression)**               | 零宽度正回顾后发断言。                               | (?<=19)\d{2}\b                                               | "1851 1999 1950 1905 2003" 中的 "99"、"50"和 "05"            |
| **(?<! subexpression)**              | 零宽度负回顾后发断言。                               | (?<!wo)man\b                                                 | "Hi woman Hi man" 中的 "man"                                 |
| **(?> subexpression)**               | 非回溯（也称为"贪婪"）子表达式。                     | [13579](?>A+B+)                                              | "1ABB 3ABBC 5AB 5AC" 中的 "1ABB"、 "3ABB" 和 "5AB"           |



## 限定符

限定符指定在输入字符串中必须存在上一个元素（可以是字符、组或字符类）的多少个实例才能出现匹配项。 限定符包括下表中列出的语言元素。

下表列出了限定符：

| 限定符         | 描述                                                   | 模式       | 匹配                                                         |
| :------------- | :----------------------------------------------------- | :--------- | :----------------------------------------------------------- |
| *****          | 匹配上一个元素零次或多次。                             | \d*\.\d    | ".0"、 "19.9"、 "219.9"                                      |
| **+**          | 匹配上一个元素一次或多次。                             | "be+"      | "been" 中的 "bee"， "bent" 中的 "be"                         |
| **?**          | 匹配上一个元素零次或一次。                             | "rai?n"    | "ran"、 "rain"                                               |
| **{ n }**      | 匹配上一个元素恰好 n 次。                              | ",\d{3}"   | "1,043.6" 中的 ",043"， "9,876,543,210" 中的 ",876"、 ",543" 和 ",210" |
| **{ n ,}**     | 匹配上一个元素至少 n 次。                              | "\d{2,}"   | "166"、 "29"、 "1930"                                        |
| **{ n , m }**  | 匹配上一个元素至少 n 次，但不多于 m 次。               | "\d{3,5}"  | "166"， "17668"， "193024" 中的 "19302"                      |
| ***?**         | 匹配上一个元素零次或多次，但次数尽可能少。             | \d*?\.\d   | ".0"、 "19.9"、 "219.9"                                      |
| **+?**         | 匹配上一个元素一次或多次，但次数尽可能少。             | "be+?"     | "been" 中的 "be"， "bent" 中的 "be"                          |
| **??**         | 匹配上一个元素零次或一次，但次数尽可能少。             | "rai??n"   | "ran"、 "rain"                                               |
| **{ n }?**     | 匹配前导元素恰好 n 次。                                | ",\d{3}?"  | "1,043.6" 中的 ",043"， "9,876,543,210" 中的 ",876"、 ",543" 和 ",210" |
| **{ n ,}?**    | 匹配上一个元素至少 n 次，但次数尽可能少。              | "\d{2,}?"  | "166"、 "29" 和 "1930"                                       |
| **{ n , m }?** | 匹配上一个元素的次数介于 n 和 m 之间，但次数尽可能少。 | "\d{3,5}?" | "166"， "17668"， "193024" 中的 "193" 和 "024"               |



## 反向引用构造

反向引用允许在同一正则表达式中随后标识以前匹配的子表达式。

下表列出了反向引用构造：

| 反向引用构造   | 描述                                | 模式                  | 匹配             |
| :------------- | :---------------------------------- | :-------------------- | :--------------- |
| **\ number**   | 反向引用。 匹配编号子表达式的值。   | (\w)\1                | "seek" 中的 "ee" |
| **\k< name >** | 命名反向引用。 匹配命名表达式的值。 | (?< char>\w)\k< char> | "seek" 中的 "ee" |



## 备用构造

备用构造用于修改正则表达式以启用 either/or 匹配。

下表列出了备用构造：

| 备用构造                        | 描述                                                         | 模式                                 | 匹配                                                         |
| :------------------------------ | :----------------------------------------------------------- | :----------------------------------- | :----------------------------------------------------------- |
| **\|**                          | 匹配以竖线 (\|) 字符分隔的任何一个元素。                     | th(e\|is\|at)                        | "this is the day. " 中的 "the" 和 "this"                     |
| **(?( expression )yes \| no )** | 如果正则表达式模式由 expression 匹配指定，则匹配 *yes*；否则匹配可选的 *no* 部分。 expression 被解释为零宽度断言。 | (?(A)A\d{2}\b\|\b\d{3}\b)            | "A10 C103 910" 中的 "A10" 和 "910"                           |
| **(?( name )yes \| no )**       | 如果 name 或已命名或已编号的捕获组具有匹配，则匹配 *yes*；否则匹配可选的 *no*。 | (?< quoted>")?(?(quoted).+?"\|\S+\s) | "Dogs.jpg "Yiska playing.jpg"" 中的 Dogs.jpg 和 "Yiska playing.jpg" |





## 替换

替换是替换模式中使用的正则表达式。

下表列出了用于替换的字符：

| 字符            | 描述                                 | 模式                                 | 替换模式          | 输入字符串 | 结果字符串   |
| :-------------- | :----------------------------------- | :----------------------------------- | :---------------- | :--------- | :----------- |
| **$**number     | 替换按组 *number* 匹配的子字符串。   | \b(\w+)(\s)(\w+)\b                   | $3$2$1            | "one two"  | "two one"    |
| **${**name**}** | 替换按命名组 *name* 匹配的子字符串。 | \b(?< word1>\w+)(\s)(?< word2>\w+)\b | ${word2} ${word1} | "one two"  | "two one"    |
| **$$**          | 替换字符"$"。                        | \b(\d+)\s?USD                        | $$$1              | "103 USD"  | "$103"       |
| **$&**          | 替换整个匹配项的一个副本。           | (\$*(\d*(\.+\d+)?){1})               | **$&              | "$1.30"    | "**$1.30**"  |
| **$`**          | 替换匹配前的输入字符串的所有文本。   | B+                                   | $`                | "AABBCC"   | "AAAACC"     |
| **$'**          | 替换匹配后的输入字符串的所有文本。   | B+                                   | $'                | "AABBCC"   | "AACCCC"     |
| **$+**          | 替换最后捕获的组。                   | B+(C+)                               | $+                | "AABBCCDD" | AACCDD       |
| **$_**          | 替换整个输入字符串。                 | B+                                   | $_                | "AABBCC"   | "AAAABBCCCC" |



## 杂项构造

下表列出了各种杂项构造：

| 构造               | 描述                                                   | 实例                                                   |
| :----------------- | :----------------------------------------------------- | :----------------------------------------------------- |
| **(?imnsx-imnsx)** | 在模式中间对诸如不区分大小写这样的选项进行设置或禁用。 | \bA(?i)b\w+\b 匹配 "ABA Able Act" 中的 "ABA" 和 "Able" |
| **(?#注释)**       | 内联注释。该注释在第一个右括号处终止。                 | \bA(?#匹配以A开头的单词)\w+\b                          |
| **#** [行尾]       | 该注释以非转义的 # 开头，并继续到行的结尾。            | (?x)\bA\w+\b#匹配以 A 开头的单词                       |



## Regex类

Regex 类用于表示一个正则表达式。

下表列出了 Regex 类中一些常用的方法：

| 序号 | 方法 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **public bool IsMatch( string input )** 指示 Regex 构造函数中指定的正则表达式是否在指定的输入字符串中找到匹配项。 |
| 2    | **public bool IsMatch( string input, int startat )** 指示 Regex 构造函数中指定的正则表达式是否在指定的输入字符串中找到匹配项，从字符串中指定的开始位置开始。 |
| 3    | **public static bool IsMatch( string input, string pattern )** 指示指定的正则表达式是否在指定的输入字符串中找到匹配项。 |
| 4    | **public MatchCollection Matches( string input )** 在指定的输入字符串中搜索正则表达式的所有匹配项。 |
| 5    | **public string Replace( string input, string replacement )** 在指定的输入字符串中，把所有匹配正则表达式模式的所有匹配的字符串替换为指定的替换字符串。 |
| 6    | **public string[] Split( string input )** 把输入字符串分割为子字符串数组，根据在 Regex 构造函数中指定的正则表达式模式定义的位置进行分割。 |





# 异常处理

- 异常提供了一种把程序控制权从某个部分转移到另一个部分的方式
- C# 异常处理时建立在四个关键词之上的：**try**、**catch**、**finally** 和 **throw**。
  - **try**：一个 try 块标识了一个将被激活的特定的异常的代码块。后跟一个或多个 catch 块。
  - **catch**：程序通过异常处理程序捕获异常。catch 关键字表示异常的捕获。
  - **finally**：finally 块用于执行给定的语句，不管异常是否被抛出都会执行。例如，如果您打开一个文件，不管是否出现异常文件都要被关闭。
  - **throw**：当问题出现时，程序抛出一个异常。使用 throw 关键字来完成



## 语法

- 假设一个块将出现异常，一个方法使用 try 和 catch 关键字捕获异常。try/catch 块内的代码为受保护的代码

```c#
try
{

}
catch(ExceptionName e1)
{
    
}
catch(ExceptionName e2)
{
    
}
finally
{
    
}
```



## 异常类

- C# 异常是使用类来表示的。C# 中的异常类主要是直接或间接地派生于 **System.Exception** 类

- **System.ApplicationException** 和 **System.SystemException** 类是派生于 System.Exception 类的异常类。

- **System.ApplicationException** 类支持由应用程序生成的异常。所以程序员定义的异常都应派生自该类。

- **System.SystemException** 类是所有预定义的系统异常的基类

  - 下表列出了一些派生自 System.SystemException 类的预定义的异常类：

    | 异常类                            | 描述                                           |
    | :-------------------------------- | :--------------------------------------------- |
    | System.IO.IOException             | 处理 I/O 错误。                                |
    | System.IndexOutOfRangeException   | 处理当方法指向超出范围的数组索引时生成的错误。 |
    | System.ArrayTypeMismatchException | 处理当数组类型不匹配时生成的错误。             |
    | System.NullReferenceException     | 处理当依从一个空对象时生成的错误。             |
    | System.DivideByZeroException      | 处理当除以零时生成的错误。                     |
    | System.InvalidCastException       | 处理在类型转换期间生成的错误。                 |
    | System.OutOfMemoryException       | 处理空闲内存不足生成的错误。                   |
    | System.StackOverflowException     | 处理栈溢出生成的错误。                         |





## 异常处理

- C# 以 try 和 catch 块的形式提供了一种结构化的异常处理方案。使用这些块，把核心程序语句与错误处理语句分离开。

```c#
using System;
namespace ErrorHandlingApplication
{
    class DivNumbers
    {
        int result;
        DivNumbers()
        {
            result = 0;
        }
        public void division(int num1, int num2)
        {
            try
            {
                result = num1 / num2;
            }
            catch (DivideByZeroException e)
            {
                Console.WriteLine("Exception caught: {0}", e);
            }
            finally
            {
                Console.WriteLine("Result: {0}", result);
            }

        }
        static void Main(string[] args)
        {
            DivNumbers d = new DivNumbers();
            d.division(25, 0);
            Console.ReadKey();
        }
    }
}
```





## 创建用户自定义异常

- 用户自定义的异常类是派生自 **ApplicationException** 类

```c#
using System;
namespace UserDefinedException
{
    class TestTemperature
    {
        static void Main(string[] args)
        {
            Temperature temp = new Temperature();
            try
            {
                temp.showTemp();
            }
            catch(TempIsZeroException e)
            {
                Console.WriteLine("TempIsZeroException: {0}", e.Message);
            }
            finally
            {
                Console.ReadKey();
            }
        }
    }
}

public class TempIsZeroException : ApplicationException
{
    public TempIsZeroException(string message):base(message)
    {
        
    }
}

public class Temperature
{
    int temperature = 0;
    public void showTemp()
    {
        if(temperature==0)
        {
            throw (new TempIsZeroException("Zero Temperature found"));
        }
    }
}
```



## 抛出对象

- 如果异常是直接或间接派生自 **System.Exception** 类，您可以抛出一个对象。您可以在 catch 块中使用 throw 语句来抛出当前的对象 

```c#
catch(Exception e)
{
    throw e;
}
```





# 文件的输入和输出

- 当打开文件进行读写时，它变成一个 **流**。
- 从根本上说，流是通过通信路径传递的字节序列
- 有两个主要的流：**输入流** 和 **输出流**。**输入流**用于从文件读取数据（读操作），**输出流**用于向文件写入数据（写操作）



## I/O类

- System.IO 命名空间有各种不同的类，用于执行各种文件操作，如创建和删除文件、读取或写入文件，关闭文件等

下表列出了一些 System.IO 命名空间中常用的非抽象类：

| I/O 类         | 描述                               |
| :------------- | :--------------------------------- |
| BinaryReader   | 从二进制流读取原始数据。           |
| BinaryWriter   | 以二进制格式写入原始数据。         |
| BufferedStream | 字节流的临时存储。                 |
| Directory      | 有助于操作目录结构。               |
| DirectoryInfo  | 用于对目录执行操作。               |
| DriveInfo      | 提供驱动器的信息。                 |
| File           | 有助于处理文件。                   |
| FileInfo       | 用于对文件执行操作。               |
| FileStream     | 用于文件中任何位置的读写。         |
| MemoryStream   | 用于随机访问存储在内存中的数据流。 |
| Path           | 对路径信息执行操作。               |
| StreamReader   | 用于从字节流中读取字符。           |
| StreamWriter   | 用于向一个流中写入字符。           |
| StringReader   | 用于读取字符串缓冲区。             |
| StringWriter   | 用于写入字符串缓冲区。             |



## FileStream类

- System.IO 命名空间中的 **FileStream** 类有助于文件的读写与关闭。该类派生自抽象类 Stream。
- 需要创建一个 **FileStream** 对象来创建一个新的文件，或打开一个已有的文件

```c#
FileStream <object_name> = new FileStream(<file_name>, <FileMode Enumerator>, <FileAccess Enumerator>, <FileShare Enumerator>);
```



| 参数       | 描述                                                         |
| :--------- | :----------------------------------------------------------- |
| FileMode   | **FileMode** 枚举定义了各种打开文件的方法。FileMode 枚举的成员有：**Append**：打开一个已有的文件，并将光标放置在文件的末尾。如果文件不存在，则创建文件。**Create**：创建一个新的文件。如果文件已存在，则删除旧文件，然后创建新文件。**CreateNew**：指定操作系统应创建一个新的文件。如果文件已存在，则抛出异常。**Open**：打开一个已有的文件。如果文件不存在，则抛出异常。**OpenOrCreate**：指定操作系统应打开一个已有的文件。如果文件不存在，则用指定的名称创建一个新的文件打开。**Truncate**：打开一个已有的文件，文件一旦打开，就将被截断为零字节大小。然后我们可以向文件写入全新的数据，但是保留文件的初始创建日期。如果文件不存在，则抛出异常。 |
| FileAccess | **FileAccess** 枚举的成员有：**Read**、**ReadWrite** 和 **Write**。 |
| FileShare  | **FileShare** 枚举的成员有：**Inheritable**：允许文件句柄可由子进程继承。Win32 不直接支持此功能。**None**：谢绝共享当前文件。文件关闭前，打开该文件的任何请求（由此进程或另一进程发出的请求）都将失败。**Read**：允许随后打开文件读取。如果未指定此标志，则文件关闭前，任何打开该文件以进行读取的请求（由此进程或另一进程发出的请求）都将失败。但是，即使指定了此标志，仍可能需要附加权限才能够访问该文件。**ReadWrite**：允许随后打开文件读取或写入。如果未指定此标志，则文件关闭前，任何打开该文件以进行读取或写入的请求（由此进程或另一进程发出）都将失败。但是，即使指定了此标志，仍可能需要附加权限才能够访问该文件。**Write**：允许随后打开文件写入。如果未指定此标志，则文件关闭前，任何打开该文件以进行写入的请求（由此进程或另一进过程发出的请求）都将失败。但是，即使指定了此标志，仍可能需要附加权限才能够访问该文件。**Delete**：允许随后删除文件。 |





## 高级文件操作

### 文本文件的读写

- 它涉及到文本文件的读写。
- **StreamReader** 和 **StreamWriter** 类有助于完成文本文件的读写
- 这些类从抽象基类 Stream 继承，Stream 支持文件流的字节读写。



#### StreamReader类



