## 前言

硬核的哪吒，我的命由我不由天。

精彩回顾：

[【图文并茂，点赞收藏哦！】重学巩固你的Vuejs知识体系](https://juejin.im/post/5e6e2a5a5188254974680f6a)

[【思维导图】前端开发-巩固你的JavaScript知识体系](https://juejin.im/post/5e8089dde51d4546d72d2099)

[Web页面制作基础](https://juejin.im/post/5e7db7446fb9a03c2e540903)

[学习总结之HTML5剑指前端（建议收藏，图文并茂）](https://juejin.im/post/5e5bc764518825494466ad66)

[前端面试必备ES6全方位总结](https://juejin.im/post/5e480441518825495371f5c7)

本文内容参加掘金技术征文活动《**2020春招面试征文**》，希望大家支持，不要忘记留下你学习的脚印，【点赞】，【评论】，【收藏】以下内容涉及👇：

发布分类归于【阅读】，标签为【面试】

> 目录

1. 个人的面试经历
2. 当作为考官我会考问你的面试重点
3. 个人收集大厂面试题库（含答案）
4. 面试时的小技巧
5. 整理的知识体系（个人重点内容）
6. 对于有面试需求的朋友，需要的帮助

所谓令人心动的offer即是让你心仪的，想要的，所追求的，如果你是社会人士，想起当年面试的自己有过哪些的经历呢？是否遗憾在🏫学校时不曾坚持努力的自己？如果你是在校生，你会面临出校后的一场面试，是否已经准备👌好了呢？

面试如同考试，检验你的知识点是否已经牢牢掌握，一次面试的成功会让你对自己充满信心，也许大多数人面临的面试都是一次次的失败，得到挫败感的心灵打击。

那么面试如何做到对答如流，或者低一点要求如何让对方记住你呢？在考官的逐层盘问下，在脑海里梳理起自己的知识体系，找到自己想要的答案。

> 面试经验，其实可以举一反三，类比考试，经过以往的在校考试，学习技巧等相类似，只不过面试是面试管当场问你题目，你作答这样的一种模式，面试一般有几轮，各各公司各有不同而已。

面试也是一次难得的自我摸底考试。从目录中的6点内容，希望能帮助自己也帮助他人的成长。

### 1. 个人的面试经历

个人的面试经历，从在校被老师推荐到朋友的前端开发工作岗位，到自己重新找工作，反复面试了几家进了其中一家，到目前的某公司前端开发负责人，个人感觉自己的面试经历都是步入正常轨迹，即是准备面试简历，展示自己的项目到论述自己在校的成就等。

内容重点强行在于面试的经验与面试的准备，面试准备其实就是自己掌握的知识体系，与必备的面试考点，网红题目。

### 2. 当作为考官我会考问你的面试重点

下面，带你一起阅读一下知识体系，大篇幅面试重点。希望能帮助到你。

#### 面试官：说说`VueRouter`

`Vue.js`加`Vue Router`创建单页应用，非常简单。通过组合组件来组成自己的应用程序，当要把`Vue Router`添加进来，然后把组件`components`映射到路由`routes`，然后告诉`Vue Router`渲染它们。

`VueRouter`中的动态路由匹配，可以在路由中设置多段“路径参数”，对应的值都会设置到`$route.params`中。

|模式|	匹配路径|	`$route.params`|
|:---|:---|:---|
|`/user/:username`|	`/user/evan`|	`{ username: 'evan' }`|
|`/user/:username/post/:post_id`|	`/user/evan/post/123`|	`{ username: 'evan', post_id: '123' }`|

> 响应路由参数的变化

当使用路由参数时，从`/user/foo`导航到`/user/bar`，原来的组件实例会被复用。因为两个路由都渲染同个组件，比起销毁再创建，复用则显得更加高效。不过，这也意味着组件的生命周期钩子不会再被调用。

- `Vue Router`中的嵌套路由
- 编程式的导航

声明式与编程式：

|声明式|	编程式|
|:---|:---|
|`<router-link :to="...">`|	`router.push(...)`|

示例：

```
router.replace(location, onComplete?, onAbort?)
```

声明式与编程式：

|声明式|	编程式|
|:---|:---|
|`<router-link :to="..." replace>`|	`router.replace(...)`|

- 了解命名路由的使用
- 了解`VueRouter`重定向和别名的使用
- 了解路由组件传参:布尔模式，对象模式，函数模式
- 了解`Vue Router`的`html5 history`模式
- 了解如何用`webpack`从零构建`vue.js+vuerouter+webpack`项目
- 了解`VUe Router`中的导航守卫
- 了解`Vue Router`中的路由元信息
- 了解`Vue Router`中的过渡动效
- 了解`Vue Router`中的数据获取
- 了解`Vue Router`中的滚动行为

`vue-router`是什么，这里的路由就是`SPA`（单页应用）的路径管理器。路由模块的本质就是建立起`url`和页面之间的映射关系。

单页面应用(`SPA`)的核心之一是: 更新视图而不重新请求页面

`hash`模式，默认为`hash`模式，使用`url`的`hash`来模拟一个完整的`url`，当`url`发生改变时，页面是不会重新加载的。

`hash`是`#`，`url`的锚点，表示网页中的一个位置，只改变`#`符号后的部分是不会重新加载网页，只会滚动到相应的位置。

即是`hash`出现在`url`中，不会被包含在`http`请求中，对后端没有影响，所以改变`hash`是不会重新加载页面的。但是注意，每次改变`#`符号后面的部分，都会在浏览器的访问历史中添加一个记录，当使用“后退”按钮时，就可以回到上一次的位置。

`hash`模式下，通过改变锚点值，根据不同的值就可以渲染至`dom`指定的位置。

> `hash`模式的原理是`onhashchange`事件，用于监听`hash`值的变化，可以在`window`对象上监听这个事件。

`history`模式，利用了`html5 history interface`中的`pushState()`方法和`replaceState()`方法，这两种方法用于浏览器记录栈。

使用`history`模式，需要后台配置支持，会更好！在服务器端增加一个能够覆盖所有情况的静态资源，如果`url`匹配不到任何静态资源，就应该返回一个`index.html`页面，这个页面就是`app`依赖的页面。

```
const routes = [ 
  {path: "/", name: "home", component:Home}
  {path: "/register", name: "register", component: Register},
  {path: "/login", name: "login", component: Login},
  {path: "*", redirect: "/"}]
```

实现页面跳转的方式：

![](https://user-gold-cdn.xitu.io/2020/4/12/1716deddc8709fc1?w=721&h=241&f=png&s=22173)

示例：

```
import Vue from 'vue';
import VueRouter from 'vue-router';
import App from './components/app.vue';
import Home from './components/home.vue'
Vue.use(VueRouter);
let router = new VueRouter({
    routes: [
        { path: '/home', component: Home }
    ]
});
new Vue({
    el: '#app',
    router: router,
    render: c => c(App),
})
```

```
<template>
    <div>
        <router-view></router-view>
    </div>
</template>
<script>
    export default {
        data(){
            return {}
        }
    }
</script>
```

![](https://user-gold-cdn.xitu.io/2020/4/12/1716e00c9e29578f?w=1253&h=578&f=png&s=87953)
 
```
this.$router.go(-1)

this.$router.replace('/1')

this.$router.replace({name:'1'})

this.$router.push('/1')

this.$router.push({name:'1'})
```

那么`$router.push`和`$router.replace`的区别

1. 使用`push`方法的跳转会向`history`栈中添加新的记录，当点击浏览器返回按钮时可以返回之前的页面
2. 使用`replace`方法不会向`history`添加新记录，而是替换掉当前的`history`记录。

安装依赖：`npm install vue-router`

`main.js`:

```
import Vue from 'vue'
import APP from './App'
import router from './router'

new Vue({
 router: router,
 render: h=>h(App),
 data: {
     eventHub: new Vue()
 }
}.$mount('#app');
```

懒加载的方式：

```
component: resolve => require(['/'], resolve)
```

```
import Vue from 'vue';
import VueRouter from 'vue-router';
import linkParams from './page/linkParams.vue';
Vue.use(VueRouter);
const router = new VueRouter({
 mode: 'history',
 base: __dirname,
 routes: [
  {
      path: '/linkParams/:userId',
      name: 'linkParams',
      component: linkParams
  },
  {
      path: '/imgParams',
      name: 'xxx',
      component: resolve => require([], resolve)
  }
 ]
})
```

> 编程式导航

示例：

```
this.$router.push('home')

this.$router.push({path: 'home'})

this.$router.push({name:'user',params:{userId:123}})

this.$router.push({path: 'register', query: {userId: '123'}})
```

全局钩子函数

```
router.beforeEach((to, from, next)=>{
  next();
});
router.afterEach((to, from, next) => {

});
```

路由独享钩子函数

```
const router = new VueRouter({
  routes: [
    {
      path: '/foo',
      component: Foo,
      beforeEnter: (to, from, next) => {
        // ...
      }
    }
  ]
})
```

组件内钩子函数

```
const BOO = {
    template: '---',
    beforeRouteEnter(to, from, next){
        
    },
    beforeRouteUpdate(to, from, next){
        
    },
    beforeRouteLeave(to, from, next){
        
    }
}
```

`route object`路由信息对象，表示当前激活的路由的状态信息，包含了当前`url`解析得到的信息，还有`url`匹配到的`route records`路由记录。

`spa`单页面应用，前端路由的核心就是改变视图的同时不会向后端发出请求。

`webpack`搭建项目：

```
npm init -y
```

```
npm add -D webpack webpack-cli
```

```
npm run build
```

```
node dist/main.js
```

打包`html`

```
npm add -D html-webpack-plugin
```

添加`vue`

```
npm add vue
```

```
npm add -D webpack-dev-server
```

```
npm add -D style-loader css-loader
```

```
npm add -D less-loader
```

```
npm add -D less
```

```
npm add vue-router
```

```
npm add express
```

路由这个概念是由后端出现的，通过浏览器中`url`发送请求，服务器监听到端口有发送过来的请求，进行解析`url`的路径，根据服务器的路由配置，返回相应的信息，浏览器根据数据包的`Content-Type`来判断如何进行解析。

路由时跟后端服务器进行交互的一种方式，根据不同的路径，请求不同的资源。

实现原理，`spa`单一页面应用程序，一个页面当它在加载页面的时候，不会加载整个页面的内容，只会更新指定的某个容器中的内容。

单一页面应用核心：更新视图不会重新请求页面；`vue-router`在实现单页面应用前端路由时，提供了三种方式，`hash`模式，`history`模式，`abstract`模式。

1. `hash`，为使用`URL hash`值来作路由
2. `history`，依赖`html5 history api`和服务器配置
3. `abstract`，支持所有`JavaScript`运行环境

> 为什么有了后端路由，还要前端路由呢？

后端路由最不好之处在于：每次路由的切换都会导致页面刷新，这样的作风对于用户体验来说不太友好。为了更好的用户体验，就有了前端路由。

它的出现，让浏览器不会重新刷新了。

了解一下：

1. `window.history.pushState()`，在会话浏览历史记录中添加一条记录。
2. `window.history.replaceState()`，该方法是将修改会话浏览历史的当前记录，浏览历史记录的总长度没有变化。

这两个方法可以改变`url`，页面也不会重新刷新。

当我们使用`hash`路由模式，每次`hash`值得改变，会触发`hashchange`事件，所以我们通过监听该事件来判断`hash`值是否发生了变化。

`history`模式，在`window`对象中提供了`onpopstate`事件来监听历史栈的改变。

安装依赖：

```
npm install vue-router
```

`main.js`

```
import router from './router';

new Vue({
 router: router,
 render: h => h(App),
})
```

#### 了解JavaScript

1. `JavaScript`的定义：它是一种具有 函数优先，轻量级，解释型，即时编译型 的编程语言。`JS`是一种动态的基于原型和多范式的脚本语言，支持面向对象，命令式和函数式的语言。
2. 它支持面向对象编程，命令式编程，函数式编程，函数先行的语言；它提供了操作文本，数组，日期以及正则表达式等。
3. 变量的声明通常在其余的代码执行之前完成
4. 变量的声明，无论发生在哪里，都在执行任何代码之前进行处理，用var声明的变量的作用域是它当前的执行上下文，它可以是嵌套的函数，也可以是声明在任何函数外的变量，如果你重新声明一个JavaScript变量，它将不会丢失其值。
5. 将赋值给未声明变量的值在执行赋值时

示例：
```
<script>
var pdada = document.querySelector('p');
pdada.addEventListener('click',updateName);
function updateName(){
    var name = prompt('输入一个新的名字');
    pdada.textContent = '魔王哪吒-达达前端'
}

// onclick
document.querySelector('html').onclick=function() {};
```

变量的描述：声明和未声明变量之间的区别：

1. 声明变量的作用域限制在其声明位置的上下文中，而非声明变量总是全局的。
2. 声明变量在任何代码执行前创建，而非声明变量只有在执行赋值操作的时候才会被创建。
3. 声明变量是它所在上下文环境的不可配置属性，非声明变量是可配置的。

示例：

```
console.log(dada); // 抛出ReferenceError
console.log(魔王哪吒); // 打印“魔王哪吒”
```

```
var a;
console.log(a); // 打印"undefined"或""（不同浏览器实现不同）
console.log("魔王哪吒"); // 魔王哪吒
```

```
var a = 1;
b = 2;
delete this.a; // 严格模式下抛出错误
delete this.b;
console.log(a,b); // 抛出ReferenceError
// b属性已经被删除
```

> 建议始终声明变量，无论它们是在函数还是全局作用域内，在`ECMAScript5`严格模式下，分配给未声明的变量会引发错误。

什么是变量提升

由于变量声明总是在任意代码执行之前进行处理，所以在代码中的任意位置声明变量总是等效于在代码开头声明，变量可以在声明之前使用。

> 所有的变量声明移动到函数或者全局代码的开头位置。

所以建议始终在作用域顶部声明变量，即是在全局代码的顶部和函数代码的顶部，这样可以清晰地知道哪些变量是函数作用域，哪些变量是在作用域链上解决。

多个变量的初始化

```
var x=0;

function f(){
    var x=y=1; // x在函数内部声明，y不是
}
f();

console.log(x,y); // 0, 1
// x是全局变量
// y是隐式声明的全局变量
```

隐式全局变量和外部函数作用域

```
// x是全局变量，赋值为0
var x=0;
// undefined，因为z还不存在
console.log(typeof z);

function a() { // 当a被调用时
 var y = 2; // y被声明成函数a 作用域的变量，赋值为2
 console.log(x,y); // 0 2
 function b() {
     // 当b被调用时
     x=3; // 全局变量x被赋值为3,不生成全局变量
     y=4; // 已经在的外部函数的y变量 被赋值为4，不生成新的全局变量
     z=5; // 创建新的全局变量z，并赋值为5
     // 在严格模式下，会抛出ReferenceError
 }
 b(); // 调用b时创建了全局变量z
 console.log(x,z); // 3,5
}

a(); // 调用a时同时调用了b
console.log(x,z); // 3,5
console.log(typeof y); // undefined,因为y是a函数的本地变量
```

伪代码，循环过程：

```
loop(foo=0, eatFood=10){
    if(foo = eatFood){
        exit loop;
    }else{
        foo+=2;
    }
}
```

原型链：每个对象都有一个原型对象，对象以其原型为模板，从原型继承方法和属性。原型对象也可以拥有原型，并从中继承方法和属性，一层一层，以此类推的这种关系被称为原型链。

换句话说，这些属性和方法是定义在`Object`的构造函数之上的`prototype`属性上，而非对象实例本身。

```
{
    constructor: ƒ doSomething(),
    __proto__: {
        constructor: ƒ Object(),
        hasOwnProperty: ƒ hasOwnProperty(),
        isPrototypeOf: ƒ isPrototypeOf(),
        propertyIsEnumerable: ƒ propertyIsEnumerable(),
        toLocaleString: ƒ toLocaleString(),
        toString: ƒ toString(),
        valueOf: ƒ valueOf()
    }
}
```

了解掌握什么是原型，`Prototype`和`__proto__`，以及原型链

![](https://user-gold-cdn.xitu.io/2020/4/19/17191c3a51d41239?w=464&h=625&f=png&s=61013)

![](https://user-gold-cdn.xitu.io/2020/4/19/17191c6782e09548?w=477&h=437&f=png&s=45930)

![](https://user-gold-cdn.xitu.io/2020/4/19/17191cad4ba7d348?w=368&h=184&f=png&s=43292)

`create()`：使用`Object.create()`方法创建新的对象实例：

```
// person1 为原型对象创建了person2对象
// person2.__proto__ 结果返回对象person1
var person2 = Object.create(person1);

// person2.__proto__ === person1
```

`create()`实际上是从指定原型对象创建一个新的对象。

> `constructor`属性

每个实例对象都从原型中继承了一个`constructor`属性，该属性指向了用于构造此实例对象的构造函数。

```
person1.constructor
person2.constructor
```

都将返回`Person()`构造器，因为该构造器包含这些实例的原始定义。

想要获取某个对象实例的构造器的名字：

```
instanceName.constructor.name

// person1.constructor.name
```

原型式的继承

定义构造器函数

```
function Person(first, last, age, gender, interests) {
    this.name = {
        first,
        last,
    };
    this.age = age;
    this.gender = gender;
    this.interests = interests;
}

Person.prototype.greeting = function(){
    console.log('hello'+this.name.first)
}

function dadaqianduan(first, last, age, gender, interests, subject) {
    Person.call(this, first, last, age, gender, interests);
    
    this.subject = subject;
}
```

#### Function.prototype.call()

`call()`方法调用一个函数，具有一个指定的this值和分别地提供的参数（参数的列表）

这个方法的作用和apply()方法类似，只有一个区别，就是call()方法接收的是若干个参数的列表，而apply()方法接收的是一个包含多个参数的数组。

语法：

```
fun.call(thisArg, arg1, arg2, ...)
```

返回值，使用调用者提供的this值和参数调用该函数的返回值，若该方法没有返回值，则返回`undefined`。

![](https://user-gold-cdn.xitu.io/2020/4/19/17192e713703f1fe?w=558&h=577&f=png&s=47028)

图中的this指向了abc的位置。

> 从无参构造函数继承

示例：

```
function dada(){
    this.width = 10;
    this.height = 20;
}

// 无参构造函数继承

function da1() {
    dada.call(this);
    this.opacity = 0.5;
    this.color = 'blue';
}
```

```
var a = new da1()

a
```

![](https://user-gold-cdn.xitu.io/2020/4/19/17192f4e6c8418fa?w=205&h=105&f=png&s=15852)

设置原型和构造器的引用

```
Teacher.prototype = Object.create(Person.prototype)
```

> 任何你想要被继承的方法都应该定义在构造函数的`prototype`对象里，并且永远使用父类的`prototype`来创造子类的`prototype`，这样才不会打乱类继承结构。

why is necessary to set the prototype constructor?

```
Student.prototype.coonstructor = Student;
```

示例：

```
// define the Person Class
function Person(name) {
    this.name = name;
}

Person.prototype.copy = function() {
    // return new Person(this.name);
    return new this.constructor(this.name);
};

// define the Student class
function Student(name) {
    Person.call(this, name);
}

// inherit Person
Student.prototype = Object.create(Person.prototype);
```

```
var student1 = new Student("掘金");
console.log(student1.copy() instanceof Student); // false
```

添加：

```
Student.prototype.constructor = Student;

var student1 = new Student("掘金");
console.log(student1.copy() instanceof Student); // true
```

> 继承

示例：

```
Teacher.prototype = Object.create(Person.prototype)
Teacher.prototype.constructor = Teacher
```

> 什么是JSON

![](https://user-gold-cdn.xitu.io/2020/4/20/171934b13cf1f012?w=522&h=107&f=png&s=35784)

声明：

`var`：声明一个变量，可选初始化一个值
`let`：声明一个块作用域的局部变量，可选初始化一个值
`const`：声明一个块作用域的只读常量

使用变量来作为值的符号名，变量的名字又叫做标识符，它必须以字母，下划线，或者美元符号（`$`）开头；后续的字符也可以是数字。

> `labeled`语句

一个`label`提供了一个可以让你引用到您程序别的位置的标识符。

`for...in`语句，循环一个指定的变量来循环一个对象所有可枚举的属性。

`for...of`和`for...in`两种循环语句之间的区别：

1. `for...in`循环遍历的结果是数组元素的下标
2. `for...of`遍历的结果是元素的值

函数声明：一个函数定义，也称为函数声明，或函数语句，由一系列的`function`关键字组成。

递归：一个函数可以指向并调用自身。

嵌套函数：一个函数里面嵌套另外一个函数。嵌套（内部）函数对其容器（外部）函数是私有的。它自身形成了一个闭包。内部函数包含外部函数的作用域。

内部函数形成了一个闭包，它可以访问外部函数的参数和变量，但是外部函数却不能使用它的参数和变量。

内部函数可以访问外部函数的作用域，因此当内部函数生命周期大于外部函数时，外部函数中定义的变量和函数的生命周期比内部函数执行时间长才行，当内部函数被销毁后，外部函数才会被销毁。

> 使用`arguments`对象

函数的实际参数被保存在一个类似数组的`arguments`对象中。

箭头函数相比函数表达式具有较短的语法并以词法的方式绑定this。

![](https://user-gold-cdn.xitu.io/2020/4/22/171a21663a29f20b?w=377&h=803&f=png&s=57509)

```
typeof(null)
// object

typeof({})
// object
```

表达式：一组代码的集合，它返回一个值。`this`关键字被用于指代当前的对象，通常，`this`指代的是方法中正在被调用的对象。

`split`通过将字符串分离成一个个子串来把一个string对象分裂到一个字符串数组中。

`slice`从一个字符串提取片段并作为新字符串返回。

`substring`,`substr`，分别通过指定起始和结束位置，起始位置和长度来返回字符串的指定子集。

`match`,`replace`,`search`通过正则表达式来工作。

`toLowerCase`,`toUpperCase`分别返回字符串的小写表示和大写表示。

`normalize`按照指定的一种`Unicode`正规形式将当前字符串正规化。

`repeat`，将字符串内容重复指定次数后返回。

`trim`，去掉字符串开头和结尾的空白字符。

#### 正则表达式

正则表达式是用于匹配字符串中字符组合的模式。在JavaScript中，正则表达式也是对象。

使用一个正则表达式字面量：

```
const regex = /ab+c/;

const regex = /^[a-zA-Z]+[0-9]*\W?_$/gi;
```

正则表达式可以被用于`RegExp`的`exec`和`test`方法以及`String`的`match`，`replace`，`search`和`split`方法。

`exec()`方法在一个指定字符串中执行一个搜索匹配，返回一个结果数组或`null`。

`test`一个在字符串中测试是否匹配的`RegExp`方法，它返回`true`或`false`。

`match`一个在字符串中执行查找匹配的`String`方法，它返回一个数组或者未匹配到时返回`null`。

`search`一个在字符串中测试匹配的`String`方法，它返回匹配到的位置索引，或者在失败时返回`-1`。

`replace`一个在字符串中执行查找匹配的`String`方法，并且使用替换字符串换掉匹配到的子字符串。

#### 如何使用Promise

一个`Promise`是一个代表异步操作最终完成或者失败的结果对象。本质上是一个绑定了回调的对象，而不是将回调传进函数内部。

示例：

```
function wait(ms){
    return new Promise(function(resolve,reject){
        setTimeout(resolve,ms);
    })
}

console.log('开始')
wait(3000).then(()=>{
  console.log('123')  
})
```

一个`Promise`有以下几种状态：

`pending`：初始状态，既不是成功，也不是失败状态；`fulfilled`：意味着操作成功完成；`rejected`：意味着操作失败。

`Promise`对象是一个代理对象，被代理的值在`Promise`对象创建时可能是未知的。它允许你为异步操作的成功和失败分别绑定相应的处理方法。

让异步方法可以像同步方法那样返回值，但并不是立即返回最终执行结果，而是一个能代表未来出现的结果的`promise`对象。

因为`Promise.prototype.then`和`Promise.prototype.catch`方法返回`promise`对象，所以它们可以被链式调用。

`Promise.all`方法返回一个新的`promise`对象，该`promise`对象在`iterable`参数对象里所有的`promise`对象都成功的时候才会触发成功，一旦有任何一个`iterable`里面的`promise`对象失败则立即触发该`promise`对象的失败。

一个新的`promise`对象在触发成功状态后，会把一个包含`iterable`里所有`promise`返回值的数组作为成功回调的返回值，顺序跟`iterable`的顺序保持一致，如果这个新的`promise`对象触发了失败状态，它会把`iterable`里第一个触发失败的`promise`对象的错误信息作为它的失败错误信息。

`Promise.race`当`iterable`参数里的任意一个子`promise`被成功或失败后，父`promise`马上也会用子`promise`的成功返回值或失败详情作为参数调用父`promise`绑定的相应句柄，并返回该`promise`对象。

#### JavaScript中的带键的集合

一个`Map`对象就是一个简单的键值对映射集合，可以按照数据插入时的顺序遍历所有的元素。

#### JavaScript中的Object对象

枚举一个对象的所有属性

`for...in`循环，该方法依次访问一个对象及其原型链中所有可枚举的属性。

`Object.keys(o)`，该方法返回一个对象`o`自身包含的所有属性的名称的数组。

`Object.getOwnPropertyName(o)`，该方法返回一个数组，它包含了对象`o`所有拥有的属性的名称。

```
var arr = ["a", "b", "c"];
console.log(Object.getOwnPropertyNames(arr).sort());

// 结果
["0", "1", "2", "length"]

// 类数组对象
var obj = { 0: "a", 1: "b", 2: "c" };
console.log(Object.getOwnPropertyNames(obj).sort());

// 结果
["0", "1", "2"]

// 使用Array.forEach输出属性名和属性值
Object.getOwnPropertyName(obj).forEach(function(val, idx, array) {
   console.log(val+"->"+obj[val]); 
});

// 输出
0 -> a
1 -> b
2 -> c
```

#### JavaScript中的内存管理

内存生命周期：

分配你所需要的内存，使用分配的内存，在不需要时需要归还释放内存。


### Node.js

学习Node.js，需要预备知识，html，css，javascript,简单的命令行操作，具有服务端开发经验。

1. node.js不是一门语言
2. node.js不是库，不是框架
3. Node.js是一个JavaScript运行时环境
4. node.js可以解析和执行JavaScript代码

node.js中的JavaScript

没有bom,dom，有EcmaScript，提供额外的api

node.js能做`web`服务器后台，命令行工具

B/S编程模型：`Browser-Server`，`back-end`。模块化编程，`RequireJS`，`SeaJS`，什么是模块化编程，就是可以在node中可以像`@import()`一样来引用加载JavaScript脚本文件。

异步编程：回调函数，`Promise`，`async`，`generator`

文件名不要使用`node.js`来命名，不要使用中文。在node中，采用`EcmaScript`进行编码没有，没有`Bom`，`Dom`，和浏览器中的JavaScript不一样。

```
// fs是 file-system的简写,就是文件夹系统的意思
// 在Node中如果想要进行文件操作,就必须引入fs这个核心模块
// 在js这个核心模块中,就提供了所有的文本操作相关的api
// fs.readFile 就是用来读取文件的

// 使用require方法加载fs核心模块
var fs = require('fs')

// 读取文件
// 第一个参数就是要读取的文件路径
// 第二个参数就是一个回调函数
// error
// 如果读取失败,error就是错误对象
// 如果读取成功,error就是Null
// data
// 如果读取失败,error就是错误对象
// 如果读取成功,data就是读取到的数据

// 成功
// data 数据
// error null
// 失败
// data null
// error 错误对象

fs.readFile('./dada.txt', function(error, data){
	// 文件中存储的其实都是二进制数据0或1
	// 看到的是二进制转16进制
	// toString方法
	console.log(data.toString())
})
```

```
var fs = require('fs')

// 第一个参数:文件路径
// 第二个参数:文件内容
// 第三个参数:回调函数

// 成功
// 文件写入成功,error是null
// 失败
// 文件写入失败,error是错误对象
fs.writeFile('./da.md', '大家好,我是达达前端', function(error){
	console.log('文件写入成功')
})
```

```
// http 帮你创建服务器

// 加载核心模块
var http = require('http')

// 使用http.createServer()方法创建一个web服务器

// 返回一个server实例
var server = http.createServer()

// 服务器提供服务:对数据的服务
// 发请求
// 接收请求
// 处理请求
// 给个反馈

// 注册 当客户端请求过来,就会自动触发服务器的request请求事件
// 然后执行第二个参数
// 回到处理函数

// request请求事件处理函数,需要接收两个参数:
// Request 请求对象
// 请求对象可以用来获取客户端的一些请求信息,例如请求路径
// Response 响应对象
// 
server.on('request', function(request, response){
	console.log('收到客户端的请求了'+request.url)
	
	// response 对象有一个方法
	// write 用来给客户端发送响应数据
	// write 可以使用多次
	// 最后一定一定要使用end来结束响应
	// 否则客户端会一直等待
	response.write('dada')
	response.write('掘金魔王哪吒')
	response.end()
})

// 绑定端口号 启动服务器
server.listen(3000, function(){
	console.log('服务器启动成功')
})
```

> node.js是什么？它是JavaScript运行时，不是语言，框架，它是一个平台，没有BOM，DOM。EcmaScript基本的JavaScript语言部分，在Node.js中为JavaScript提供了一些服务器级别的`api`，文件操作的能力，`http`服务的能力。

```
var http = require('http')

// 创建server
var server = http.createServer()

// 监听request 请求事件,设置请求处理函数
server.on('request',function(req,res){
	console.log('收到请求'+req.url)
	
	res.end('达达前端,魔王哪吒-掘金')
	
	// 根据不同的请求路径发送不同的响应结果
	// 获取请求路径
	// 判断路径响应
	
	// res.end() 响应内容必须是字符串,或二进制数据
	// res.end(JSON.stringify())
	
	var url = req.url
	
	if(url === '/') {
		res.end('index')
	}else if(url === '/login') {
		res.end('login page')
	}else {
		res.end('404 not found')
	}
	
})

// 绑定端口号,启动服务
server.listen(80,function(){
	console.log('服务器启动')
})
```

核心模块：

node为JavaScript提供了很多服务器级别的api，这些api绝大部分包装到了一个具名的核心模块中。

fs核心模块文件操作，http服务器构建的http模块，path路径操作模块等。

在node中，没有全局作用域，只有模块作用域，外部访问不到内部，内部也访问不到外部。

`require`方法有两个作用：

1. 加载文件模块并执行里面的代码
2. 拿到被加载文件模块导出的接口对象

每个文件模块中提供了一个对象：`exports`
`exports` 默认是一个空对象

```
var ret = request('./b')

// console.log(ret)
console.log(ret.foo)

console.log(ret.add(1,2))
```

```
var foo = '达达前端'
// console.log(exports)
exports.foo = 'hello'

exports.add = function(x,y) {
    return x+y
}
```

web服务器开发：

ip地址是用来定位计算机，端口号用来定位具体的应用程序，所有需要联网通信的软件都会占用一个端口号，端口号的范围从0-65536之间，在计算机中有一些默认端口号，建议不要去使用。

响应内容类型：`Content-type`

```
var http = require('http')

var server = http.createServer()

server.on('request', function(req, res){
	// 解决编码问题
	// res.setHeader('Content-Type','text/plain;charset=urf-8')
	// res.end('dadaqianduan')
	
	var url = req.url
	// text/plain 普通文本
	if(url === '/plain'){
		res.setHeader('Content-Type', 'text/plain;charset=utf-8')
		res.end('dadaqianduan')
	}else if(url === '/html'){
		res.setHeader('Content-Type', 'text/html;charset=utf-8')
		res.end('<p>dadaqianduan</p>')
	}
	
})

server.listen(3000, function(){
	console.log('server is runing...')
})
```

```
var http = require('http')
var fs = require('fs')

var server = http.createServer()

server.on('request', function(req, res){
	var url = req.url
	if(url === '/'){
		fs.readFile('./resource/index.html', function(err,data){
			if(err){
				res.setHeader('Content-Type','text/plain;charset=utf-8')
				res.end('文件读取失败,请稍后重试')
			}else{
				// data默认是二进制数据
				// toString转为字符串
				
				// 图片资源不要指定编码
				// res.setHeader('Content-Type','image/jpeg')
				res.end(data)
			}
		})
	}
})

server.listen(3000, function(){
	
})

// url 统一资源定位符
```

![](https://user-gold-cdn.xitu.io/2020/4/29/171c627623db9b27?w=906&h=761&f=png&s=67204)

通过网络发送文件

发送的并不是文件，本质上是发送文件的内容；当浏览器收到服务器响应内容之后，就会根据你的`Content-Type`进行对应的解析处理。

#### 服务器渲染和客户端渲染的区别

1. 客户端渲染不利于SEO搜索引擎优化
2. 服务端渲染可以被抓取到，客户端异步渲染就很难获取到
3. 真正的网站既不是纯异步也不是纯服务渲染

#### ip地址和端口号

所有联网的程序都需要进行网络通信，计算机只有一个物理网卡，而且同一个局域网中，网卡的地址必须是唯一的。

网卡是通过唯一的ip地址来进行定位的。端口号用来定位具体的应用程序，所有需要联网通信的应用程序都会占用一个端口号。端口号的范围0到65536之间。

#### JavaScript思维导图

![](https://user-gold-cdn.xitu.io/2020/4/30/171c824d6dea0ad8?w=1165&h=252&f=png&s=39110)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c82a4f9129bbe?w=1003&h=677&f=png&s=86534)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c8319fab2dc24?w=902&h=225&f=png&s=31162)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c83d6b672ae85?w=1062&h=492&f=png&s=69975)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c864a0fc64cb1?w=1055&h=672&f=png&s=74669)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c8722882a4edd?w=1184&h=624&f=png&s=76280)

![](https://user-gold-cdn.xitu.io/2020/4/30/171c8898a7e66315?w=1400&h=643&f=png&s=104148)

![](https://user-gold-cdn.xitu.io/2020/5/1/171cdb7067e714d5?w=1410&h=430&f=png&s=65132)

![](https://user-gold-cdn.xitu.io/2020/5/1/171cdd3ddcb4acac?w=853&h=559&f=png&s=67203)

![](https://user-gold-cdn.xitu.io/2020/5/1/171ce127d7e6a6cc?w=888&h=483&f=png&s=60400)

![](https://user-gold-cdn.xitu.io/2020/5/1/171ce29dc78e7d1b?w=1059&h=621&f=png&s=97537)

![](https://user-gold-cdn.xitu.io/2020/5/1/171cf67cf0d6798e?w=830&h=182&f=png&s=19896)

![](https://user-gold-cdn.xitu.io/2020/5/2/171d4c446571ddc0?w=288&h=330&f=png&s=11231)

![](https://user-gold-cdn.xitu.io/2020/5/2/171d5e4e7d0cb057?w=1259&h=757&f=png&s=119487)

![](https://user-gold-cdn.xitu.io/2020/5/3/171d8fe1eaaff809?w=1215&h=733&f=png&s=139461)

![](https://user-gold-cdn.xitu.io/2020/5/3/171da06b8d955c86?w=1190&h=814&f=png&s=101344)

![](https://user-gold-cdn.xitu.io/2020/5/3/171da813a4717181?w=1256&h=609&f=png&s=94800)

![](https://user-gold-cdn.xitu.io/2020/5/4/171dc9ea28d20b75?w=1061&h=718&f=png&s=94214)

![](https://user-gold-cdn.xitu.io/2020/5/4/171dce098e11b089?w=1082&h=636&f=png&s=98812)

![](https://user-gold-cdn.xitu.io/2020/5/4/171dd8a2fe213d0c)

![](https://user-gold-cdn.xitu.io/2020/5/4/171de08ca677e84f?w=1090&h=701&f=png&s=119873)

![](https://user-gold-cdn.xitu.io/2020/5/4/171debdb3ca7b617?w=984&h=599&f=png&s=99038)

![](https://user-gold-cdn.xitu.io/2020/5/4/171dfd0aedc87c1c?w=1013&h=700&f=png&s=129459)

![](https://user-gold-cdn.xitu.io/2020/5/5/171e1c4994b159fe?w=836&h=809&f=png&s=71778)

![](https://user-gold-cdn.xitu.io/2020/5/5/171e1ec5b7f90d33?w=786&h=712&f=png&s=73166)

![](https://user-gold-cdn.xitu.io/2020/5/5/171e1f8189824632?w=963&h=685&f=png&s=77035)

![](https://user-gold-cdn.xitu.io/2020/5/5/171e20db9039b9c2?w=1366&h=709&f=png&s=117814)

![](https://user-gold-cdn.xitu.io/2020/5/5/171e238607479a22?w=966&h=736&f=png&s=88308)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e6f05242be6cc?w=1140&h=758&f=png&s=108537)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e722862f98bfa?w=1082&h=679&f=png&s=88790)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e72a4c6db6a08?w=995&h=595&f=png&s=76051)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e7365d2db2182?w=1229&h=782&f=png&s=101442)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e73b820f7d7e2?w=970&h=708&f=png&s=71060)

![](https://user-gold-cdn.xitu.io/2020/5/6/171e76823774581d?w=1195&h=551&f=png&s=81151)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec18b47b3ad2a?w=1177&h=809&f=png&s=117561)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec2478606f4bf?w=1141&h=798&f=png&s=103707)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec2f6e7443071?w=1071&h=734&f=png&s=98871)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec49679903f37?w=1222&h=774&f=png&s=114883)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec78414e5c2d9?w=1250&h=822&f=png&s=132648)

![](https://user-gold-cdn.xitu.io/2020/5/7/171ec84fcc839c08?w=574&h=438&f=png&s=34786)

![](https://user-gold-cdn.xitu.io/2020/5/7/171efd3389e6d80d?w=1322&h=695&f=png&s=106910)

![](https://user-gold-cdn.xitu.io/2020/5/8/171f176aa0dcbc07?w=1505&h=773&f=png&s=103472)

![](https://user-gold-cdn.xitu.io/2020/5/8/171f1a47208773e9?w=554&h=445&f=png&s=41377)

![](https://user-gold-cdn.xitu.io/2020/5/8/171f1b44cc2ccdbc?w=1288&h=832&f=png&s=125432)

![](https://user-gold-cdn.xitu.io/2020/5/9/171f6bd5ba3cf9f3?w=528&h=550&f=png&s=51204)

![](https://user-gold-cdn.xitu.io/2020/5/9/171f6d4ee49eb749?w=1392&h=760&f=png&s=127402)

![](https://user-gold-cdn.xitu.io/2020/5/9/171f6e52842bb48f?w=1269&h=793&f=png&s=94223)

![](https://user-gold-cdn.xitu.io/2020/5/11/17200c623499cff2?w=1425&h=656&f=png&s=94650)

![](https://user-gold-cdn.xitu.io/2020/5/12/172061be9b74d765?w=1088&h=741&f=png&s=86880)

更加深入JavaScript等待下一篇总结。

### 3. 个人收集大厂面试题库（含答案）

interview-answe 1+1：目录

https://github.com/webVueBlog/interview-answe

### 4. 面试时的小技巧

面试考察点：

1. 基础部分，需要掌握基础技术点，库和框架
2. 经验部分，如做过什么项目，项目中解决了什么核心问题；项目开发过程中，前后端多个角色是如何配合的；多人如何合作开发；针对你的工作做过的如何思考，项目，团队，自身各个方面都可以进行谈论
3. 思路部分，框架适用的场景，设计某个技术场景的解决方案
4. 面试部分，一轮，老大面，考关注综合能力，二轮，技术总监，关注算法和综合能力，三轮，hr将公司的好等

对于简历：不要列举太多，一般两页就够，强调特殊技能，管理，跨端，全栈，做的重要项目，核心解决了什么问题，附加github或者网站等。

面试准备，将最近最近做过的重要的技术点梳理一下，能过清晰说出整体的架构和思考改进，常见问题复习一下，不必全面，但要重要，准备问题留着问面试官。

面试时，要沉着冷静，不要想太多，就事论事，让面试官听你讲。掌握主动权，很多问题并没有标准答案，所以尽量答就行，考官的考察点可能并不是问题本身。

### 5. 整理的知识体系

【 suggestion 👍 】 from 0 to 1 web front-end

web-0-1目录

![](https://user-gold-cdn.xitu.io/2020/5/15/17215ab45115c78c?w=1011&h=732&f=png&s=92709)

https://github.com/webVueBlog/web-0-1

### 6. 对于有面试需求的朋友，所提供的帮助

优秀的工程师，有好奇心，学习能力，分析解决问题的方式和能力。

利用技术解决生活中遇到的问题，有自己的小作品，专栏或者学习总结，对技术投入大量的时间等。

看书，边看边写，模仿实现，学习流行的开发框架

用框架开发小应用，开发项目等

深入了解各种框架解决的核心问题，解决多人开发问题，工程化

深入js底层，了解各种框架的核心机制，架构师

更多精彩内容：http://www.dadaqianduan.cn/#/

### 7. 参考文献

MDN:https://developer.mozilla.org/

维基百科:https://zh.wikipedia.org/

JavaScript高级程序设计（第3版）

![](https://user-gold-cdn.xitu.io/2020/5/15/17215abea98ec350?w=900&h=500&f=png&s=211339)