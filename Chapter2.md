# 词法结构

## 概念
* JavaScript 程序是由 **Unicode 字符集编写的**，Unicode 是 ASCII 和 Latin-1 的超集

* **ASCII** 包含 128 个字符，33 个无法显示的控制字符和 95 个可显示字符

```
例如：十进制：32->空格, 65->A, 97->a 十六进制：20->空格, 41->A, 61->a
```

* **Unicode 转义序列**是 6 个 ASCII 字符来代表任意 16 位 Unicode 内码，其总是以 '\u' 为前缀，后跟 4 个十六进制数字

```
例如：'\u0020'->空格
```

* Unicode 为所有字符定义了一个**首选的编码格式**，并给出了一个标准化的处理方式

```
例如：字符 'é' 可以由 Unicode 字符 '\u00e9' 表示，也可以由普通 ASCII 字符 e 跟随一个语调符 '\u0065\u0301' 表示
```

* **标识符**，由字母、下划线 _ 或 美元符 $ 开始，后跟任意字母、数字、下划线 _ 或 美元符 $，用来对变量和函数进行命名
* **保留字**

```
true  false  null
function  return
for  in  do  while  if  else
switch  case  break  continue  default  finally
new  delete  this  var  let  const
try  catch  throw  debugger
instanceof  typeof
import  export  class  extends  super
static  private  public  protected
implements  yield  interface  package
with  void  enum
```

  **ECMAScript3 将 Java 所有的关键字也列为了自己的保留字**

  其中有一些本身也是 JavaScript 的保留字包含在上面，还有一些是 Java 特有的关键字

```
boolean  char  doubel  float  int  long  short
byte  abstract  final  goto  native  synchronized  throws  transient  volatile
```
	**另外，JavaScript 还预定义了全局变量和函数**

  也应当将其视为“保留字”避免用作变量名和函数名

```
undefined  String  Boolean  Object  Array  Date  RegExp  Math  JSON
Function  arguments
Number  Infinity  isFinite  NaN  isNaN  parseInt  parseFloat
Error  SyntaxError  RangeError  EvalError  ReferenceError  TypeError
URIError  encodeURI  encodeURIComponent  decodeURI  decodeURIComponent
eval
```

## 特性
* HTML 不区分大小写，JavaScript 区分大小写
