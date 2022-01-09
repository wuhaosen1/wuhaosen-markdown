# ES6 新特性学习

每日一小时左右，熟练掌握 es6-es11 各类新特性

# DAY 1

node 安装源 nrm 安装东西比较快，安装完可以 ls 查看可用的源，

然后 use 使用相对应的源进行资源的下载，一般用 taobao 源

![image-20211001093724981](ES6新特性学习.assets/image-20211001093724981.png)

上图为源的各种操作

![image-20211001094959636](ES6新特性学习.assets/image-20211001094959636.png)

开发环境的构建，构建完之后用 vscode 就可以进行 es 学习

### let

![image-20211001095850233](ES6新特性学习.assets/image-20211001095850233.png)

不加 var 相当于一个属性，delete 只可以删除属性，因此打印出来第 11 行就会报错，a 相当于一个变量，顶层对象属性和全局变量是 js 的一个败笔，把他俩挂钩了

let 的特性

![image-20211001100505815](ES6新特性学习.assets/image-20211001100505815.png)

### const

const 定义一个常量，而且需要在定义的时候赋值，它的块级作用域和 let 一样，也不允许提升和暂时性死区，const 的常量是不允许被改变的，const 如果定义对象的话，那对象的地址就不会被改变

![image-20211001112223731](ES6新特性学习.assets/image-20211001112223731.png)

它可以冻结最外层的对象，要想冻结里面的 year 就需要冻结他的 skill 对象

# DAY 2

![image-20211002085850972](ES6新特性学习.assets/image-20211002085850972.png)

es5 写常量就是这样子写，到了 es6 就用 const 来定义常量

### let 和 const 的选择

定量用 const，变量用 let，let 和 const 有作用域，var 没有作用域

### 变量的解构赋值

![image-20211002090820599](ES6新特性学习.assets/image-20211002090820599.png)

![image-20211002091018281](ES6新特性学习.assets/image-20211002091018281.png)

通过左右两边写成一样的模式就可以进行解构赋值，输出来的结果就是 123，上图是数组的解构赋值

![image-20211002091502944](ES6新特性学习.assets/image-20211002091502944.png)

此项是对象的解构赋值，也跟数组的逻辑一样，左右两边模式一样

![image-20211002091725458](ES6新特性学习.assets/image-20211002091725458.png)

以上是对象的解构赋值

![image-20211002091833510](ES6新特性学习.assets/image-20211002091833510.png)

以上是字符串的解构赋值跟数组的类似

### 变量解构赋值的默认值

一般有赋值就是赋值的值，没有的话就是一开始定义的那个值，赋值是一种惰性赋值

若遇到 json 的结构赋值，可以用 json 的两种方法，JSON。pause

还有 JSON。stringify

### 数组的遍历方式 es5

![image-20211002092829367](ES6新特性学习.assets/image-20211002092829367.png)

![image-20211002093437490](ES6新特性学习.assets/image-20211002093437490.png)

break 和 continue 不可以使用在 foreach 中，foreach（function（elem，index，array）{}）

map 会遍历每一个参数形成新的数组

filter

![image-20211002093830662](ES6新特性学习.assets/image-20211002093830662.png)

会找到符合结果的数据形成新的数组

some 遍历是否符合的值返回的是布尔值![image-20211002094104247](ES6新特性学习.assets/image-20211002094104247.png)

在数组里边找到一个符合的就会返回 true

every

![image-20211002094217947](ES6新特性学习.assets/image-20211002094217947.png)

每一个都符合才会返回 true

reduce 相当于一个累加器

![image-20211002094420672](ES6新特性学习.assets/image-20211002094420672.png)

他有 4 个参数，一个是 prev，一个是 cur，一个是 index，最后一个就是 arry，通过 return prevent+cur 就可以求出数组的和，O 代表返回值的初始值

![image-20211002094628898](ES6新特性学习.assets/image-20211002094628898.png)

他还可以很方便的求出数组里最大的值

数组去重

![image-20211002094848214](ES6新特性学习.assets/image-20211002094848214.png)

prev.push（cur），这样就可以很快速的完成数组去重

for in 遍历数组

![image-20211002095041865](ES6新特性学习.assets/image-20211002095041865.png)

它不仅能遍历数组也可以遍历数组中的对象

### es6 的新遍历方式

![image-20211002095210737](ES6新特性学习.assets/image-20211002095210737.png)

find 返回第一个通过测试的元素，findindex 都是一个方法跟 es5 相似

![image-20211002095414147](ES6新特性学习.assets/image-20211002095414147.png)

for of 的用法

![image-20211002095556120](ES6新特性学习.assets/image-20211002095556120.png)

前面对应的是 value 后面对应的是值， entries 返回的是下标和值因此要两个返回值

### 数组的扩展

1.判断数组的方式，用 instanceof Array

2.伪数组没有数组的方法

3.伪数组转化为真实数组

![image-20211002115533329](ES6新特性学习.assets/image-20211002115533329.png)

通过 slice 方法可以将伪数组转化为数组

4![image-20211002115647843](ES6新特性学习.assets/image-20211002115647843.png)

arguments 代表着就是我们传的参数

5.将伪数组转化为数组的方法

![image-20211002115933927](ES6新特性学习.assets/image-20211002115933927.png)

es 6 from ，es5 中用的是 slice

![image-20211002120239405](ES6新特性学习.assets/image-20211002120239405.png)

构造一个新数组，当穿的参数为 1 个的时候代表长度，2 个以上代表数组的值

es 6 of

![image-20211002120446703](ES6新特性学习.assets/image-20211002120446703.png)

用 array of 就可以解决上诉问题

![image-20211002120652764](ES6新特性学习.assets/image-20211002120652764.png)

它也可以将各种数据拼装成新的数组

![image-20211002120954401](ES6新特性学习.assets/image-20211002120954401.png)

copyWithin，从下标为 1 的开始替换，用下标为 3 的替换下标为 1 的值

![image-20211002121248459](ES6新特性学习.assets/image-20211002121248459.png)

fill 填充，第一个参数代表填充内容，第二个代表填充位置，第三个代表填充到哪，但不包含那个位置

index of es5 里边的

![image-20211002122309024](ES6新特性学习.assets/image-20211002122309024.png)

有某个数就会返回某个数的下标，nan 的话不能检测，并且，不存在的数返回-1

![image-20211002122508939](ES6新特性学习.assets/image-20211002122508939.png)

includes，有就会返回 true，可以解决 es5 里边不可以找到 nan 的问题

### 模板字符串的使用

用‘{里面加内容}’就可以直接进行字符串的拼接

${里面加内容}，就可以用变量`````

![image-20211005083538630](ES6新特性学习.assets/image-20211005083538630.png)

###

### es6 简化方式

![image-20211005084707468](ES6新特性学习.assets/image-20211005084707468.png)

函数后面的：和 function 可以不用写以及，属性名和属性相同，可以直接用属性

### 箭头函数

![image-20211005090955993](ES6新特性学习.assets/image-20211005090955993.png)

箭头函数的 this 指向是指向上一级的对象，并且箭头函数不可以构造实例化对象

![image-20211005091500047](ES6新特性学习.assets/image-20211005091500047.png)

用箭头函数去作为回调函数的使用

### rest

arguments 是一个伪数组所以不能用对象的方法

![image-20211005091901851](ES6新特性学习.assets/image-20211005091901851.png)

。。。args 就可以代表 rest 参数，他是一个数组，。。。后面的参数是自定义的随便写，rest 参数必须放最后

### 函数的参数

![image-20211005092339750](ES6新特性学习.assets/image-20211005092339750.png)

可以默认支持参数默认值

### spread 扩展运算符

![image-20211005092714054](ES6新特性学习.assets/image-20211005092714054.png)

也是。。。可以将伪数组转化为数组 ， 分隔的参数序列

![image-20211005093131336](ES6新特性学习.assets/image-20211005093131336.png)

也可以通过此方式将别人属性变成直接的一个属性

也可以使用 spread 运算符来实现数组的合并

![image-20211005102824694](ES6新特性学习.assets/image-20211005102824694.png)

深拷贝是拷贝值，浅拷贝就拷贝地址

将伪数组转化为数组

![image-20211005103219833](ES6新特性学习.assets/image-20211005103219833.png)

### symbol 数据类型

![image-20211005164828513](ES6新特性学习.assets/image-20211005164828513.png)

使用 symbol 来获取对象的属性值的时候，我们要加个中括号才可以

![image-20211005183456232](ES6新特性学习.assets/image-20211005183456232.png)

若想遍历里边属性，必须通过一个 Reflect。ownKey（），先获取键名，再通过 for 循环遍历获取里面的属性值

### 迭代器 iterator 生成器

for in 循环得到的是下标

for of 循环得到的是值

# DAY 3

### map

### class

### 数值的扩展

![image-20211006224410073](ES6新特性学习.assets/image-20211006224410073.png)

2，8，10，16 进制表示

![image-20211006225036342](ES6新特性学习.assets/image-20211006225036342.png)

![image-20211006225224564](ES6新特性学习.assets/image-20211006225224564.png)

### 对象的扩展

![image-20211006225725682](ES6新特性学习.assets/image-20211006225725682.png)

Object。assgin 对象的合并

--proto--

### 深拷贝浅拷贝

浅拷贝可以修改原来的值

![image-20211007083844793](ES6新特性学习.assets/image-20211007083844793.png)

concat 和 slice 都素浅拷贝，扩展运算符也是浅拷贝，。。。【】、

深拷贝

深拷贝不可以修改原来的东西

用 JSON。stringify 不能拷贝方法，

方法：函数在对象里面叫做方法，函数在对象外叫做函数

递归

![image-20211007085352296](ES6新特性学习.assets/image-20211007085352296.png)

先新建一个数组和对象再把值赋给它们，就可以保证深拷贝

## HTTP

![image-20211008091151091](ES6新特性学习.assets/image-20211008091151091.png)

报文目录

![image-20211010095803725](ES6新特性学习.assets/image-20211010095803725.png)

通过 post 请求，给服务器发送提取表单中的内容，

get，post，respond

每个 if else 判断都是路由规则

![image-20211010100842885](ES6新特性学习.assets/image-20211010100842885.png)

get 请求

headers 就是请求头的东西，

preview 就是响应体预览的效果

# DAY 4

将 npm yarn cnpm 和 cyarn 学习完啦，版本管理工具

# DAY 5

## es6 模块化学习

![image-20211014093120618](ES6新特性学习.assets/image-20211014093120618.png)

![image-20211014093431251](ES6新特性学习.assets/image-20211014093431251.png)

有 3 种暴露方式

用解构方式导入错误的话就可以用 as 重命名就好了

## ES6 模块化内容复盘

模块暴露

- 分别暴露 export let name = 'iloveyou'
- 统一暴露 let a=100; let b =200; export {a,b}
- 默认暴露 export default {name:'atguigu.com'}

模块导入

- 通用形式导入. 针对任何一种暴露方式都有效. 缺点就是变量名称.属性来操作 m1.foo() m1.bar()
- 解构形式导入. 注意别名重名问题. 重名可以使用 as 进行别名设置.
  针对默认暴露 import {default as m3} from './m3'
- 简便方式导入. 只能针对默认暴露 import m4 from './m4'
- 关于 npm 包的导入 直接使用 import $ from 'jquery'

1. 通用方式 import \* as m from './m1.js' //m.default.
2. 解构方式 import {default as m2} from './m2.js'
3. 简便方式 import m3 from './m3.js'

## AJAX

![image-20211015093514797](ES6新特性学习.assets/image-20211015093514797.png)

原生 ajax 操作步骤

![image-20211015094052087](ES6新特性学习.assets/image-20211015094052087.png)

要服务器返回的结果

![image-20211015094206571](ES6新特性学习.assets/image-20211015094206571.png)

ajax 服务

## readyState 属性值

- 0 未初始化
- 1 open
- 2 send
- 3 服务返回一部分结果的时候
- 4 所有的结果都返回后

## 用 jQuery 发送 Ajax 请求

![image-20211016090327790](ES6新特性学习.assets/image-20211016090327790.png)

# DAY 6

## JS 错误

### **1.1.1.** **\*\*错误的类型\*\***

\1. Error: 所有错误的父类型

\2. ReferenceError: 引用的变量不存在

\3. TypeError: 数据类型不正确的错误

\4. RangeError: 数据值不在其所允许的范围内

\5. SyntaxError: 语法错误

### **1.1.2.** **\*\*错误处理\*\***

\1. 捕获错误: try ... catch

\2. 抛出错误: throw error

### **1.1.3.** **\*\*error 对象的结构\*\***

\1. message 属性: 错误相关信息

\2. stack 属性: 函数调用栈记录信息

/\*

\1. 常见内置错误

\*/

// ReferenceError: 引用的变量不存在

// console.log(a) // ReferenceError: a is not defined

// TypeError: 数据类型不正确的错误

var b = null

// console.log(b.xxx) // TypeError: Cannot read property 'xxx' of null

b = 3

// console.log(b.xxx()) // TypeError: b.xxx is not a function

// RangeError: 数据值不在其所允许的范围内

function fn1() {

fn1()

}

// fn1() // RangeError: Maximum call stack size exceeded

// SyntaxError: 语法错误

// const c = """" // SyntaxError: Unexpected string

/\*

\2. 错误处理

\*/

// 2.1 捕获错误

try {

var d = 3

d()

} catch (error) {

console.log(error.message)

console.log(error.stack)

}

console.log('捕获错误后还可以继续执行')

// 2.2 抛出错误

function doThing() {

const time = Date.now()

if (time %2 === 1) {

console.log('当前是奇数, 可以执行业务逻辑处理')

} else {

throw new Error('当前时间是偶数, 无法处理业务逻辑')

}

}

try {

doThing()

} catch (error) { // 捕获错误, 做相应的界面提示

alert(error.message)

}

## promise

## 手写 promise

![image-20211019104006396](ES6新特性学习.assets/image-20211019104006396.png)

1 首先是构造 promise 函数对象

![image-20211019104036054](ES6新特性学习.assets/image-20211019104036054.png)

2.添加 then 方法，同步 i 任务状态下

![image-20211019110459482](ES6新特性学习.assets/image-20211019110459482.png)

3，添加 then 方法一部状态下先初始化一个数组，将 pending 状态先保存

![image-20211019113511664](ES6新特性学习.assets/image-20211019113511664.png)

4.回到函数，检查数组是否有数据有的话就执行相关回调

# DAY 7

## 通过 Ajax 发送请求

![image-20211022130107382](ES6新特性学习.assets/image-20211022130107382.png)

并且设置对应类型的请求头需要什么请求头就设置相对应的请求头

## 设置 Ajax4 步骤

1.let x = new XMLHttpRequest（）

2.x.onreadystatechange = function(){

if(readyState === 4{

if(status>=200&&<300){

console.log(x.responseText);//获取相应的相应文本

} })

}

3.x.open("请求方式（get）","请求路径（/server）");

4.x.send()

### Ajax 返回类型设置

![image-20211022131232910](ES6新特性学习.assets/image-20211022131232910.png)

Ajax 可以设置返回的类型，在设置 Ajax 的时候可以进行预设置

![image-20211022132006208](ES6新特性学习.assets/image-20211022132006208.png)

通过 jQuery 也可以设置相似的

### x.timeout 和 x.ontimeout 设置

![image-20211022143527377](ES6新特性学习.assets/image-20211022143527377.png)

延时或者重新发送服务

## axios

axios 发送请求传回来的是一个 promise

### axios 发送 get 请求

![image-20211022174725346](ES6新特性学习.assets/image-20211022174725346.png)

通过此方式绑定点击事件发送 get 请求，响应体直接可以获得 js 对象

### get 请求传参用的是 params

![image-20211022190134642](ES6新特性学习.assets/image-20211022190134642.png)

### axios 发送 post 请求

![image-20211022184247515](ES6新特性学习.assets/image-20211022184247515.png)

### post 传参用的是 data，params，也可以通过 url 传参

### put 请求传参

也类似于 post，可用 data 和 params，

### DELETE 通过 axios 发送请求

![image-20211022192059042](ES6新特性学习.assets/image-20211022192059042.png)

在 url 中传参，params（参数）就是 url 后面的

## axios 与 jsonserver 结合

![image-20211022194519251](ES6新特性学习.assets/image-20211022194519251.png)

![image-20211022194547422](ES6新特性学习.assets/image-20211022194547422.png)

建立一个 db。json，通过 axios，引入 axios

### Patch 局部修改

![image-20211022200132633](ES6新特性学习.assets/image-20211022200132633.png)

### 检索数据

![image-20211022200733969](ES6新特性学习.assets/image-20211022200733969.png)

跟个问好-gte 这是在文档查询的 json-server，在 GitHub 查询得到的

## axios 使用对象方法发送 Ajax 请求

1.![image-20211022201038793](ES6新特性学习.assets/image-20211022201038793.png)

同源策略的话要设置跨域的东西，添加一个请求头允许跨域访问

。post，![image-20211022201230155](ES6新特性学习.assets/image-20211022201230155.png)

![image-20211022201342125](ES6新特性学习.assets/image-20211022201342125.png)

可以通过 config 设置，也可以设置请求头信息

![image-20211022201741405](ES6新特性学习.assets/image-20211022201741405.png)

![image-20211022201840408](ES6新特性学习.assets/image-20211022201840408.png)

设置请求头信息的两种方式

# DAY 8

## axios 访问段子早测

晚上总结练习一下压入表格的段子接口

## axios 创建实例对象发送请求

![image-20211023131135472](ES6新特性学习.assets/image-20211023131135472.png)

可以通过 create 方法来创建实例对象

## axios 默认配置

![image-20211023131245328](ES6新特性学习.assets/image-20211023131245328.png)

可以设置默认配置减少代码重复率

## axios 发送/取消请求

![image-20211024085043429](ES6新特性学习.assets/image-20211024085043429.png)

![image-20211024085137677](ES6新特性学习.assets/image-20211024085137677.png)

取消通过调用发送请求 cancel token 里面的 c 取消函数来取消发送请求

三步：1 声明全局变量，2 配置 cancel token 值，3 调用函数，可以在函数内传递参数![image-20211024085643634](ES6新特性学习.assets/image-20211024085643634.png)

![image-20211024090143447](ES6新特性学习.assets/image-20211024090143447.png)

取消之后会返回一个失败的 promise 所以要设置一下 error

，为了优化代码防止用户重复点击发送请求使服务器承载量过大，一般要在点击发送前加一个判断，if quxiao ！== null 执行取消代码 quxiao（），意思是已经执行了请求代码不能再继续发送请求，还要在请求完成后改变 quxiao 的状态，quxiao = null

## 函数延时数据

![image-20211024085408949](ES6新特性学习.assets/image-20211024085408949.png)

## 封装一个 axios

![image-20211024121516043](ES6新特性学习.assets/image-20211024121516043.png)

## axios 拦截器

axios.interceptors.request.use(function(){})

![image-20211024155337309](ES6新特性学习.assets/image-20211024155337309.png)

## axios 取消请求

![image-20211024162001515](ES6新特性学习.assets/image-20211024162001515.png)

## axios 文字说明和图示介绍

看 doc

## axios 案例演示

可以通过 axios。defaults。timeout/baseUrl/headers/设置默认配置，若是有较多的需要配置的代码可以通过默认设置减少代码量

### 设置 loading 提示，进度条

NProgress.start(),和 NProgress.done()可以设置一个定时器来规定几秒钟完成，
例如： 引入 NProgerss 包，然后，NProgress.start();setTimeout(function(){NProgress.done},4000),要设置当完成的时候设置 done



## 回收机制

编记回收

编号回收



# js高级深度理解

## js函数闭包的使用

### 高阶函数

函数可做作为函数的返回值，也可以用作参数,使用方式

例子1：

'''

function makeadd( add) {

​    function add (x) {

​        return add + x      

​       }

​    return add

}

var add1 = makeadd(5)

console.log(add1(5))  //10

'''

例子2：

'''

  function calculate (a,b,cal) {

​      console(cal(a,b))

}

​     function add (a,b) {

  return a+b

}

   function sub( a,b ) {

 return a-b 

}

calculate(1,2,add)    //3

'''

这就形成了闭包， 内壁函数的引用对外部有影响导致外部函数不会被释放



## 数组的方法

### fliter

var nums = [ 5， 5，20，10]

filter 过滤

nums.filter(函数 => boolean )

会自动回调传入的参数,传入3个参数,需要返回一个Boolean值

'''

var nueNUms = nums.filter((item,index,arr) => {

​    return  item % 2 === 0

})

'''

如果用item的话就会一个个回调nums的值，以上就是返回一个偶数的数组



### map映射

var nums2 = nums.map((item) => {

​    return item *10

})

num2就会返回一个10倍的数组



### forEach：迭代、遍历

nums.forEach(() => {

   console.log(nums)   //用于遍历数组

})

forEach没有返回值



### reduce：累加

方法1 

for (  let  i=0; i<nums.length; i++){

   total += nums[i]

}

使用reduce

nums.reduce(function (prevalue//返回的是上一次的值,item) {

​        return prevalue + item //返回的就是累加成的值

},100/100为初始值)





### find/findIndex

查找，返回的是符合条件的元素，返回true就是返回第一个元素,用法：

例1：

'''

var need = nums.find( () => {

​    return true

})

//例2

var friend = [{name:'xx',age:11},{name:'zz',age:12},{name:cc,age:13}]

  const myfriend = friend.find(() => {

​     friend.name === 'xx'    // {name:'xx',age:11}

})

findIndex //找到的就是下标，索引值

'''



### 创建数组实例

 var arr = new Array(123).fill(1),意思就是长度为123的数组，填充1

## this指向

在浏览器的全局this指向的是WIndow，在node里的this是一个空对象{}。

### 隐式绑定

默认绑定，引擎帮我们自动绑定

### call 和apply区别显示绑定

。call和。apply都可以调用函数，可直接执行

foo。call（）



function sum(n1,n2){

 console.log(n1+n2,this)

}

sum.call('call',12,23)

sum.apply('apply',[12,23])

一个传一个个对象还有传数组的区别

### bind显示绑定

绑定完会显示一个新的函数，开辟一块新的空间

'''

function foo () {

 console.log(this)

}

foo.call('aaa')//指向string



var newFoo = foo.bind('aaa')

newFoo()//优先级更高的是显示绑定

'''

### new绑定

'''

function Person(){

this.name = name

this.age = age

  console.log(this)

}

var p = new Person("xixi",123).

'''

通过new关键字调用函数时（构造器），这个时候的this调用这个构造器创建出来的对象，this = 创建出来的对象

这个绑定的过程就是new绑定



### forEach

arr.forEach(( item，index ，arry) => {

}，this)，forEach和Map第二个参数可以改变this指向，forEach可以传item，index，arr函数本身三个参数

## 绑定this优先级

默认绑定优先级是最低的

显示绑定优先级高于隐式绑定

new优先级高于隐式绑定

new优先级高于显示绑定（不能和apply 和call同时使用）

bind优先级高于call

apply和call和bind传入null和undefined会this指向window



### 箭头函数

1、不绑定this 和 arguments

2、不能和new一起使用会抛出错误



常见简写

1.参数只有一个的时候小括号可以省略

2.函数执行体只有一行代码大括号可以省略，并且将执行体的返回值作为返回值

3.如果一个箭头函数只有一行代码，并且返回一个对象，需要加一个小括号



不绑定this从上层找this





## this面试题

![image-20211219103227389](JS高级.assets/image-20211219103227389.png)

图中小括号加不加一样，若括号里有独立表达式就属于独立函数调用指向window





![image-20211219103908940](JS高级.assets/image-20211219103908940.png)

定义对象是没有产生作用域的，所以在对象里面的箭头函数指向的是window，图中为独立函数调用指向的是window



## call apply 和bind 实现

call方法实现：

undefined和null返回window

用this改变指向，添加一个属性用后删除

用。。。args结构，也可以传递剩余参数



apply：跟call类似，就是传的参数需要时数组



bind：需要返回一个函数，并且可以进行绑定，定义和调用分别传参数



### arguments

arguments.length可以看参数长度

根据索引值获取某个参数arguments[index]

arguments.callee返回整个原函数

箭头函数不绑定arguments会去上层里面找

在node全局里面有arguments，在window没有会报错



箭头函数可以用剩余参数

var foo = （num1,num2,...args) => {

   console.log(args)

}

foo(12,12,23,44,566,7)

### arguments转数组

let newarry2 = Array.prototype.slice.call(arguments)

let newarray3 = [].slice.call(arguments)



es6语法：

let newarray4 = Array.from(arguments)

let newarray5 = [...arguments]

## javascipt纯函数

不产生副作用的函数

相同输入产生相同输出

不修改外部全局变量，不修改传入的参数，不会改变



### 副作用

side effect 表示函数执行时，修改了全局变量，参数或者外部的存储



例如：

'''

var names = ["sss","ssd","ssf"]

var names2 = names.slice(0,1)//表示截取0-1的数组并返回一个新的数组

var names3 =names.splice(0,1)//表示截取0-1并返回原来的数组，此方法会修改原数组，修改了元素组的行为称为副作用

'''



### 柯里化 

只传递函数的一部分参数调用它，让它返回一个函数处理余下参数，这个过程就称为柯里化

例：

'''

 function add(x,y,z){

  returen x+y+z

}



function sun(x){

   ruturn function(y) {

​      return function(z){

}

}

}



var sum = x => y => z => x + y + z

'''



柯里化函数的实现，function foo(m,n,z,x,c,v,b){}

console.log(foo.length)// 7可以直接通过函数.length拿到参数的长度

### 组合函数

将多个函数组合在一起执行

组合函数的实现

'''

function hsCompose(...fns) {

 var length = fns.length

 for(var i = 0 ; i < length ; i++){

  if(typeof fns[i] !== 'function'){

  throw new TypeError("Expected arguments are functions") 

}

 }

function compose (...args) {

 var index = 0  

 var result = length?fns[index].apply(this,args) : args

 while(++index < length) {

 result = fns[index].call(this,result) 

}

 return result

}

 return compose

}

'''



### with语句

es 5 以前只有两个东西会形成作用域， 函数和全局

with语句会形成自己的作用域

对象不会产生作用域，直接{}是有作用域的

'''

var message:"jams"

var obj = { name:"why",age: 18 ,message:"kebo"}

function foo() {

 function bar() {

 with(obj){

 console.log(message) //kebo

 console.log("xxx")

}

}

} 

'''

已经不推荐使用了

## eval函数

它是一个全局函数它可以将传入的字符串当作JavaScript代码运行



var jsstring = 'var message = "hello";console.log(message);'

eval(jsstring)

webpack => devtool 有时候可以看到eval

缺点：

可读性差，

是一个字符串容易被篡改不安全

必须通过js解释器不能被js引擎优化

## 严格模式

strict mode严格模式

限制：

会抛出静默错误

js引擎在执行代码的时候可以经行更多优化

仅用了ECMA未来版本中可能会定义的一些语法

用法：给js文件，给函数内部

“use strict”

打包的代码会自动开启严格模式

eval添加变量不能被使用

自执行函数会指向undefined不会指向window

setTimeout在严格模式下依然指向window

## Object对象方法

### .defineProperty，可以设置get和set

接受三个参数，对象，属性或者symbol，额外的限制条件以及value如下

用法：

'''

Object.definePropety(obj,"name",{

 configurable:false

 writable:false

 value:"why"

})

'''

第三个参数可传

数据属性描述符：

![image-20211222101101539](JS高级.assets/image-20211222101101539.png)

存取属性描述符，他有默认值

![image-20211222101616756](JS高级.assets/image-20211222101616756.png)



![image-20211222100918601](JS高级.assets/image-20211222100918601.png)

存储属性描述符，get set

![image-20211222102238189](JS高级.assets/image-20211222102238189.png)

_在社区被默认为私有属性

### definedProperties

可以定义多个属性，后面直接用对象

### getOwnPropertyDescriptor【s】(obj)

用于获取某个属性的描述符，或者所有属性

### .preventExtensions(obj)

阻止对象添加新的属性

### .seal（obj）

可以给属性

设置不可配置

### .freeze(obj)

设置属性不可修改

### 构造函数

一般构造函数，首字母大写比较好，比较长的用驼峰

es6的新语法，就是通过class来创建类



缺点：定义函数的时候就会产生新的函数对象，会造成空间浪费，所以就有了'''__proto__'''和prototype这样就可以将相同的属性存储到一个对象中这样子就可以比较节约空间



## 原型 【【prototype】】

——proto——很多浏览器都给数据存在一个属性

获取属性 Object.getPrototypeOf()

一般都用__proto_叫做隐式原型

当从一个对象获取属性时，会从原型链查早

''' 

obj.__ proto __ . age 隐式原型，对象有proto属性，都是指向函数的显示原型

''' 

''' 

 obj.prototype.xxx显示原型

''' 

对象的原型是隐式原型

函数也是一个对象，因为它是函数所以他多了一个显示原型

会用隐式原型指向显示原型

![image-20211223092300199](JS高级.assets/image-20211223092300199.png)

这两个值是相等的，对象的隐式原型指向构造函数的显示原型

![image-20211223093018194](JS高级.assets/image-20211223093018194.png)

prototype.constructor构造器指向构造函数本身所以有以下写法

foo.prototype.constructor.prototype.constructor.prototype.constructor.



foo. prototype = { }赋值为一个新的对象

表示打开了一个新的对象，然后foo的prototype就指向了

这个新的对象，一般用于改多个原型的属性，但是就少了constructor构造器，我们一般用Object.definePropoty(foo.prototype,"constructor",{

 enum:false,

 configurable:true,

 writable:true,

 value:foo



})

### 批量创建构造函数

![image-20211223101037288](JS高级.assets/image-20211223101037288.png)

最佳方案

对象里面最好不要随便用箭头函数

## 面向对象

三大特性：封装，继承，动态，抽象

## 原型链

属性的-- proto --为父级元素的Object.prototype 

Object是所有类的父类



function Person(){

}

function student(){

}



原型链继承有三个弊端：1.新建出来的对象不会显示——proto——的属性，2.获取函数引用的时候会影响其他对象的属性，3.传入参数的时候不能在原函数处理

### 借用构造函数继承

function Student() {

 Person.call(this)

}

弊端，person函数至少被调用两次

stu的原型对象上会多出一些属性

### 对象原型式继承

var info = Object.create(obj)

### 判断属性是否存在、

可以用info.hasOwnProperty（"name"）判断对象是否存在name属性

也可以用：

“address” in info 判断info里面存在address属性



instanceof检测某个构造函数的prototype是否出现在某个对象的原型链上面

### 究极原型链

Function.prototype === Function.__proto__

Function的原型对象是自己创建出来的

Function即是对象也是函数，所以，是Object创建的Function对象

![image-20211225093324874](JS高级.assets/image-20211225093324874-16403960062561.png)

### minin类的混入

是用一个函数用于构造新的类继承原来的类再返回新的类

1.14

## es6

method shorthand方法的简写

foo：function(){}  === foo(){}

计算属性名

[name + 123] : "xixi"

### 数组结构

![image-20211228102041747](JS高级.assets/image-20211228102041747.png)

### 对象结构

![image-20211228103041456](JS高级.assets/image-20211228103041456.png)

### 块级作用域

![image-20211228121500537](JS高级.assets/image-20211228121500537.png)

![image-20211228121738240](JS高级.assets/image-20211228121738240.png)





for (const   item of names) {

 

} 

### 函数参数默认值

![image-20211228135211025](JS高级.assets/image-20211228135211025.png)

### 对象默认值以及解构

![image-20211228135625031](JS高级.assets/image-20211228135625031.png)

有默认值的参数最好放在最后

有默认值的参数，之后的参数都是不算在长度里边

![image-20211228140127599](JS高级.assets/image-20211228140127599.png)

### SET

![image-20211229105845497](JS高级.assets/image-20211229105845497.png)

可以删除，数组去重，看个数，clear方法

![image-20211229110011561](JS高级.assets/image-20211229110011561.png)

set遍历

### weakset

不能添加基本数据类型只能放对象类型

对对象是一个弱引用，如果对象引用被消除，他就被消除

有has，add，没有foreach等遍历方法，以及clear方法



### Map

1.通过构造方法创建

允许对象来作为key

const map = new Map()

map.set(obj,"aaa")





const set2 = new Map([obj1,"Aaa],[Obj2,"222"])



有 get，has，delete，clear

可以用foreEach遍历

map2.forEach((item,key) {

   console.log(item,ley)

})



for(const item of map2) {

 console,log(item[0],item[1])

}



for (const [key,value] of map2) {

   console.log(key , value)

}



### weakmap

有has，get，delete

vue3响应式原理







## es7 2016

### Array Includes

判断数组是否存在某个数的时候

例：

'''

 const names = [1,2,3,4,5,6,6]

 if(names.indexOf(7) !== -1) {

   表示包含的时候

}



if (names.includes("222",3)) {

  console.log(第一个参数传寻找的数，第二个表示从哪开始找)

}



'''

### 指数运算符

'''

const result = Math.pow(3,3)//3的三次方

const result1 = 3**3

'''



## es8

### object的value值获取

Object.key(obj)

Object.values(object)

如果传入的是字符串就会返回单个字符组成的数组



### Object entries

Object.entries(obj)

返回的是一个数组

![image-20211230095138666](JS高级.assets/image-20211230095138666.png)

### String Padding

字符填充

'''

const message = "hello world"

const newmessage = message.padStart(15,"~")//表示填充15个~在前面

//。padEnd在后面填充

'''

案例：

'''

 const cardnumber = "2132132131233213"

const reducenumber = carnumber.slice(-4)

const final number = reducenumber.padStart(cardnumber.length-4"*")

'''

### Object Descriptors

### Async Function : async ,await



## es9

### Async iterators

### 对象的展开运算符

### promise的Finally





## es10

### flat flatMap

flat 降维，用于数组降维

flatMap降维遍历

const names = [ "hellow world","xixi","haha"]

用map 

const word = names.Map((item) => {

​		console.log(item)//打印的是一个个数组组成的word

​			//如果用flatMap就可以纸打印一个数组然后返回

})



for in拿到的是索引值，for of 才是拿到每个元素

### Object.fromEntries

将Object.entries转化为对象类型



params 参数



### trimStart  trimEnd

去除空格，



### Symbol description

### optional catch binding





## es11

### bigint

比较大的数字有时候不能正确显示大数字

es11之前最大能表示的int型 = Number.Max_SAFE_INTEGER

const bigInt = 2342365463456763673767567547n,在最后面加一个n，运算的时候也要加n

或者用BigInt(num)相加



### nulish coalescing operator

空值合并运算

||

const bar = foo || “default value”

？？

const bar = foo ？？ “default value”

### optional chaining

可选链

是在判断null和undefined的时候更加方便

？.判断是否存在属性



### global this

在node里面全局对象是global，在浏览器在是window

globalThis全局里面的this



### for in操作标准化

### dynamic import

### promise.allSetted

### import meta

## es12

finalizationRegistry类，当对象被销毁的时候执行

const finalRegistry = new FinalizationRegistry((value) = {

console.log(value)

})

finalizationRegistry.register(obj，“obj”)

检测对象是否被回收

### weakRef类

### local-assign-operator

||=

&&=

？？=

相当于let message = xxx

message = message || “value”

message ||= “value”

### ——

大数字的下划线

### 可以利用definPropotry监听对象

## proxy类和reflect对象

![image-20211231092606089](JS高级.assets/image-20211231092606089.png)

监听对象操作：

''' js

const obj = {

 name: "why",

 age:18

}



const objProxy = new Proxy(obj,{

 get：function(target,key) {

 //target表示对象，key

  return target[key]

},

 set: function(target, key, newValue) {

console.log(`监听到设置时间${target}`)

target[key] = newValue

}

})//捕获器有13种 trap

'''

in捕获器

has: function(target, key) {

 console.log(`监听到in操作`)

 return ket in target

}

"name" in objProxy

删除捕获器

deleteProperty: function(target, key) {

 

}

13种捕获器以及使用方法

![image-20211231094108807](JS高级.assets/image-20211231094108807.png)



### reflect对象es6

Reflect.

一般配合proxy使用为了防止直接操作对象

''' js

const obj = {

 name: "whs",

 age: 18

}

const objProxy = new Proxy(obj,{

  set: function(target, key) {

   const result = Reflect.set(target, key, newValue, receiver){    

receiver就是我们创建的Proxy对象

}

 if result() {

}else{}

}

})

只有get和set才有receiver

receiver参数表示proxy代理对象，可以用于改变this

''' 

![image-20211231200705111](JS高级.assets/image-20211231200705111.png)

### reflect的constructor的作用

![image-20211231200959760](JS高级.assets/image-20211231200959760.png)

## 响应式原理实现

自己敲

## promise

es6新增的

promise.then

promise.catch

executor执行器

* 状态：

pending,待定的

fulfilled,resolved,确定的

rejected，拒绝的



### resolve方法函数传递的三个参数

1.普通的数据或者对象

2.传入一个promise，返回的状态由传入的promise决定

3.传入一个obj但是又then方法的对象，会执行里面的resolve

28

### then方法

1.同一个promise可以多次被then调用

2.then可以有返回值，如果返回一个普通的值，其实是返回一个promise里面的resolve，它的返回值是包裹在promise中

例：promise.then(res => {

  return "aaa"

}).then(res => {

 console.log(res)// aaa

})

3.返回的是一个对象并且该对象实现了thenable，则会有该对象里面的then决定是resolve还是reject，且返回的res也是有里面的值决定的

### catch方法

1.throw Error的时候会抛出错误，也会调用错误的回调

2.通过catch方法传入错误的回调

用法1：

promise.catch( err => {

 console.log(err)

})

用法2：

promise.then(res => {

 return 111

}).catch(err => {

  console.log(err)

})

//此用法抛出的错误。是第一个promise的错误不是then回调的promise，如果第一个没有错误，才让返回的用

注意事项：

如果promise.then(res => {

 console.log(111)

})

promise.catch(err => {

 console.log("error")

})

上面两个代码是独立运行的所以当promise是错误的时候，就会执行第一个，会发生错误，在node中就会退出运行环境

### finally方法

es9里面新增的特性

promise.finally(() => {

 comsole.log("finally code executor")

})

finally 也是返回promise，但是一般很少最后继续写方法

最后会执行的方法

### resolve类方法

使用方法，假如我们要将一个对象转成promise

const promise = Promise.resolve({nmae:"why"})

相当于

const promise2 = new Promise((resolve,reject) => {

 resolve({name:"why"})

})



promise.then(res => {

 console.log("res:", res)

})

跟上面resolve方法一样有三种参数传递返回值也是相同

### reject类方法

reject无论传入什么值，返回的也是在reject执行，传入promise还是promise的resolve都会执行reject







### all类方法

需求：当所有的Promise都变成fulfilled时，再拿到解构

promise.all([p1,p2,p3], "aaa").then(res => {

 console.log(res)

})

会将结果按照p1,p2,p3的顺序返回成一个数组



如果有一个错误就会执行catch

promise.all([p1,p2,p3], "aaa").then(res => {

 console.log(res)

}).catch( err => {

  console.log(err)//打印的是错误的那个promise

})

### allSettled类方法

es11新增的方法

等所有都有结果的时候，这时候就会给你对应的结果

![image-20220102160821497](JS高级.assets/image-20220102160821497.png)

会返回一个数组且里面是由一个个对象组成，如果状态时fulfilled就会返回一个value，如果是rejected就会返回一个reason

### race类方法

谁先有结果就打印谁

如果有rejected就会打印rejected



### any方法

在es12新增的方法

等到有一个resolved的时候才会执行，如果全都是错误

就会返回一个all promise were rejected

2.08

 '''js

class 

 '''

## 迭代器——生成器

**迭代器**

1. 迭代器是一个对象，与可迭代对象有关系但是是不同的两个东西

2. 迭代器需要遵守迭代器协议，interator，迭代器对象有next属性是一个无参或者一个参数的函数，并且可以多次调用，会返回一个Boolean值，一个value值，当遍历完所有的数后会变成true和undefined

3. 生成迭代器的函数，需要手写   

   

   

**可迭代对象**

1. 就是将迭代器以及需要迭代的东西，还有迭代的函数组合而成一个可迭代对象
2. 可迭代对象和迭代器都是对象

![image-20220106221316655](JS高级.assets/image-20220106221316655.png)

上图就是一个可迭代对象，用箭头函数就是为了让this指向iterableObj

3. for。。。of遍历就是需要对象为可迭代对象
4. 内置创建可迭代对象，`const interator1=names[Symbol.interator]()`,返回的是一个可迭代对象，所以就可以使用inrerator1.next(),内置的原生对象，String，Array，Map，arguments对象，NodeList对象
5. 对象的解构赋值不是应用的迭代器而是es9新增的特性用entry和entries

**生成器**generator函数

1. 生成器是一种特殊的迭代器可以传参，生成器函数传入的参数是上一个yield的返回值，const p = yield xxx

2. es6新增的函数控制使用的方案，可以控制函数什么时候执行，什么时候停止

3. 直接在function后面加一个*，也可以yield关键字控制流程，在yield的时候就会停止运行函数

4. 当我们调用生成器函数时，会返回一个生成器对象，它是一个特殊的迭代器

5. 如果想执行生成器第一个yield（产出），就直接调用一次next，这样子就会执行第一段的那个yield之前的代码

6. 如果需要返回值，就直接在yield后面加上返回值就行，返回的也是跟迭代器一个的对象，用法也跟迭代器类似

7. 可以调用return方法终止函数执行且可以传入参数，也是在上一个yield的返回值取得参数，且后面都不会执行了

8. throw方法，抛出错误generator.throw(),可以用try。。。catch，捕获错误之后就可以继续进行运行代码

9. 用生成器替换迭代器

   function* createArrayIterator(){

    for(const item of names){

      yield item

   }

   }       == yield* names    后面跟一个可迭代的对象

**自定义类的迭代**

### async

也是用生成器产生的

async和await实现的



### error

throw new Error 如果是同步函数就会停止运行，异步的话还会继续执行，可以在catch接受reject的错误信息



### await 

必须用在async里面

面试题二

## node事件循环

![image-20220108092450639](JS高级.assets/image-20220108092450639.png)

## 模块化commonjs

node实现了commonjs规范   module.export{}

const why =  require("url")

这样子就可以导入其他的对象了

### require细节

是一个函数，可以帮助我们引用另一个文件，

查找规则：

1.如果查找的是一个node核心模块，它会直接返回核心模块并且停止查找

2.如果是路径。/ ../   /表示相对路径和绝对路径，它会自动加上后缀名，js ，json， node 按着这些顺序寻找，后会查找index,js,index.json,index.node文件

3.不是路径也不是核心模块，会根据path的路径进行查找

根据module.path的路径查找

### 模块加载过程

每个module实例有个loaded，如果被require引用过一次之后，再次引用也只会执行一次，如果有循环引入，深度优先遍历，广度优先遍历，dfs搜索，node就是用深度优先算法

conmonjs缺点，主要用于同步代码，浏览器端引用的时候容易造成阻塞

### AMD CMD模块化规范

amd异步加载模块

用requirejs 和  

导入导出

![image-20220108202534205](JS高级.assets/image-20220108202534205.png)

![image-20220108202557532](JS高级.assets/image-20220108202557532.png)

以上两图为amd的导入导出规范 

1.18，用的是requirejs包





CMD

![image-20220108214732031](JS高级.assets/image-20220108214732031.png)

![image-20220108214756289](JS高级.assets/image-20220108214756289.png)

cmd规范也是异步的规范seajs

### ESModule

运用ＥＳＭｏｄｕｌｅ就会自动执行严格模式，运用的是import　和　export两个关键字

ｅｓ　module的几种导入导出方式：

导出：

１．export　function　ｆｏｏ（）｛｝

export　ｃｏｎｓｔ　ｎａｍｅ　＝＂ｘｘｘ＂

２．ｅｘｐｏｒｔ　｛

　ｎａｍｅ，

　ａｇｅ

｝

３．ｅｘｐｏｒｔ　ｎａｍｅ　ａｓ　ｆｎａｍｅ

导入：

１.import　｛ｘｘｘ｝　from　“．／ｆｏｏ．ｊｓ”

２．ｉｍｐｏｒｔ　｛ｎａｍｅ　ａｓ　ｆｎａｍｅ｝　ｆｒｏｍ

３．ｉｍｐｏｒｔ　＊　ａｓ　ｆｏｏ　ｆｒｏｍ　＂ｘｘｘ＂

使用的时候就用ｆｏｏ。ｎａｍｅ





将多个文件统一到ｉｎｄｅｘ处，export　，封装第三方库的时候经常用到export　＊　，这样可以将全部导出，



default用法

export　ｄｅｆａｕｌｔ　ｆｏｏ

export　｛

ｆｏｏ　ａｓ　default

｝

这样导入的时候就不用｛｝





import　函数

用法，将导入变成异步的

import（＂．／ｆｏｏ．ｊｓ＂）．ｔｈｅｎ（ｒｅｓ　＝＞　｛

　　　ｃｏｎｓｏｌｅ．ｌｏｇ（ｒｅｓ．ｎａｍｅ）

｝）



ｅｓ１１新增内容

ｃｏｎｓｏｌｅ．ｌｏｇ（ｉｍｐｏｒｔ．ｍｅｔａ），打印模块路径





es Module 模块解析

![image-20220109132553300](JS高级.assets/image-20220109132553300.png)

1.构建阶段

![image-20220109133327474](JS高级.assets/image-20220109133327474.png)

主要是下载以及缓存所需要的模块

2.3.实例化阶段-求值阶段

![image-20220109133443197](JS高级.assets/image-20220109133443197.png)

阶段二分配空间，阶段三赋值







在浏览器端不可以结合commonjs和esmodule使用，

在node环境中需要看版本

在平时开发环境中，webpack环境中可以结合使用





### npm

包管理工具

1.3、0休息
