# Vue 核心 MVVM模型 数据代理

### 1.6 MVVM 模型

![1679019050792](./assets\1.6.png)

`MVVM` 模型

- M:模型**Model**,`data`中的数据
- V:视图**View**，模板代码
- VM:视图模型**ViewModel**`,Vue实例`观察发现
- `data`中所有的属性，最后都出现在了`vm`身上
- `vm`身上所有的属性及`Vue`原型身上所有的属性，在`Vue模板`中都可以直接使用

### 1.7 Vue中的数据代理

`Object.defineproperty`方法

**数据代理**：通过一个对象代理对另一个对象中属性的操作(读/写)

1. `Vue`中的数据代理通过`vm`对象来代理`data`对象中属性的操作（读/写)

2.  `Vue`中数据代理的好处:更加方便的操作`data`中的数据

3. 基本原理

   a．通过**object.defineProperty()**把`data`对象中所有属性添加到`vm`上

   b.为每一个添加到`vm`上的属性，都指定一个`getter`  `setter`

   c.在`getter` `setter`内部去操作(读/写)`data`中对应的属性

![1679019465135](./assets\1.7.png)

`Vue` 将`data`中的数据拷贝了一份到 `_data` 属性中，又将`_data` 里面的属性提到`Vue实例`中(如name)，通过`defineProperty`实现数据代理，这样通过 `geter/setter` 操作 name，进而操作`_data` 中的name。而`_data`又对`data`进行数据劫持，实现响应式

