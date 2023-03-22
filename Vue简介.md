# Vue

### 1.1. Vue 简介

#### 1.1.1. 官网

- [英文官网](https://www.yuque.com/r/goto?url=https%3A%2F%2Fvuejs.org%2F)
- [中文官网]([Vue.js - 渐进式 JavaScript 框架 | Vue.js (vuejs.org)](https://cn.vuejs.org/))

#### 1.1.2.介绍与描述

- Vue是—套用来动态**构建用户界面的渐进式**`JavaScript`框架
  - **构建用户界面**:把数据通过某种办法变成用户界面
  - **渐进式**:`Vue`可以自底向上逐层的应用，简单应用只需要一个轻量小巧的核心库，复杂应用可以引入各式各样的`Vue`插件
- 作者:尤雨溪

![](.\assets\1.1.2.png)

#### 1.1.3. Vue的特点

1．遵循MVVM模式

2．编码简洁，体积小，运行效率高，适合移动/PC端开发

3．它本身只关注Ul，可以引入其它第三方库开发项目

4．采用**组件化**模式，提高代码复用率、且让代码更好维护

![](.\assets\1.1.3.png)

5.**声明式**编程，让编码人员无需直接操作 `DOM`，提高开发效率

![](.\assets\1.1.3.5.png)

- 使用 **虚拟DOM**和 **Diff算法**，尽量复用 `DOM`节点

![](.\assets\1.1.3.6.png)

#### 1.1.4.与其他JS框架的关联

- 借鉴angular的**模板**和**数据绑定**技术
- 借鉴react的**组件化**和**虚拟DOM**技术

#### 1.1.5.Vue周边库

- vue-cli: vue 脚手架
-  vue-resource(axios): ajax请求.
- vue-router:路由
- vuex:状态管理（它是vue 的插件但是没有用vue-xxx的命名规则)
- vue-lazyload:图片懒加载
- vue-scroller:页面滑动相关
- mint-ui:基于vue的U组件库(移动端)
- element-ui:基于vue的U组件库(PC端)

### 1.2.初识Vue

**前置工作**

1．给浏览器安装**Vue Devtools**插件

2.标签引入`Vue`包

3．(可选)阻止`vue` 在启动时生成生产提示 **Vue.config.productionTip = false**

4.**favicon**需要将页签图标放在项目根路径，重新打开就有了(**shfit+F5**强制刷新)

**初识Vue**

1.想让`Vue`工作，就必须创建一个 `Vue`实例，且要传入一个**配置**对象

2.root容器里的代码依然符合`html规范`，只不过混入了一些特殊的 `Vue语法`

3.root容器里的代码被称为**Vue模板**

4.Vue 实例与容器是**一一对应**的

5.真实开发中只有一个 `Vue实例`，并且会配合着组件—起使用

6.**{ixxx}}**中的xxx要写**js表达式**，且xxx可以自动读取到`data` 中的所有属性

​	**注意区分**: js表达式和js代码(语句)

​	a.表达式:一个表达式会产生一个值，可以放在任何一个需要值的地方

​		a 	a+b 	demo(1)  	x === y ? 'a' : 'b'

​	b. js代码(语句)

​		if(){}	for(){}

7.一旦data 中的数据发生变化，那么模板中用到该数据的地方也会自动更新

