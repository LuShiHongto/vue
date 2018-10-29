# vue介绍

[vue官网](https://cn.vuejs.org/)

先下载`vue.js`，然后在html文件中引入

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.5.17/dist/vue.js"></script>
```

`jquery.js` 提供`$或者jQuery`全局变量

`vue.js`  提供`Vue`全局变量

Vue 的核心库只关注视图层  读音view

# 开发工具

用git下载工具，然后方便我们开发vue项目
```bash
git clone https://github.com/vuejs/vue-devtools.git
```

# helloworld

1. 先实例化`Vue`,里面允许我们放很多选项(https://cn.vuejs.org/v2/api/),可以放**数据，DOM，生命钩子，资源和组合**

```js
var vm = new Vue({
  // 选项
})
```
你用jQ，第一要有数据，第二要有节点，没节点，数据没意义
```js
$.ajax()//
$(el).html(data)
//寻找节点，然后放数据
```

2. 放入必要的选项，el和data是必须要有的

el就是寻找节点（找作用域），data就是配合`{{}}`来渲染数据
```js
var vm = new Vue({
    // 选项
    data:{
        name:"lemon1"
    },
    el:"#demo"
})
```

3. 在view层的`id`为`demo`的作用域里面配合`{{}}`绑定数据

```html
<div id="demo">
    <p>{{num+1+'1'}}</p>
</div>
```

# jQuery和Vue的表达式和指令

文本值 v-text

```js
$().text();

<p>{{name}}</p>
<p v-text="name"></p>
```

属性值

`:style`和`:class`是必须接受一个对象

`:xxx`都可以接受任何变量
```js
$().attr();
$().css();
$().addClass();

<p :name="name"></p>
```