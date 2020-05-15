---
title: vue-gun-ui说明文档：GunUtils 工具类方法集
date: 2020-05-15 14:57:28
tags: vue-gun-ui
---
<!-- --------------------分割线-------------------- -->
虽然是个UI组件库，想了想觉得加一个工具类方法集还是挺有必要的，哈哈哈，看着用吧。
vue-gun-ui抛出了GunUtils，可以在自己的项目的入口文件中全局挂载到Vue原型链下，也可以在页面中局部引用。

``` javascript
// main.js
import Vue from 'vue'
import gunui from 'vue-gun-ui'

// UI库的全局注册
Vue.use(gunui)
// GunUtils的全局挂载
Vue.prototype.GunUtils = gunui.GunUtils
// --------------------------------------------------
// xxxxx.vue
// 组件页面中的局部引用
import { GunUtils } from 'vue-gun-ui'
```

<!-- --------------------分割线-------------------- -->
### checkNotNull(targ, type) 校验非空
| 参数名称 | 说明 | 类型 | 默认值 | 可选值 |
| :- | :- | :- | :- | :- |
| targ | <font color=red>必传</font>；校验目标； | String / Number / Array / Object | - | - |
| type | 校验类型；如果没传则自动判断targ的数据类型； | String | - | string / number / array / object |

<font color=red>返回布尔</font>；

``` javascript
var a = '', b = 0, c = [], d = {}
GunUtils.checkNotNull(a) // false
GunUtils.checkNotNull(b) // true
GunUtils.checkNotNull(c) // false
GunUtils.checkNotNull(d) // false
```

<!-- --------------------分割线-------------------- -->
### createUUID(needLine) 生成UUID
| 参数名称 | 说明 | 类型 | 默认值 | 可选值 |
| :- | :- | :- | :- | :- |
| needLine | 需要'-'隔开； | Boolean | true | - |

<font color=red>返回32个字符的uuid</font>，由数字0-9、字母a-f组成；需要64个字符的可以执行2次进行拼接，其它个数字符的可以自行切割拼接；

``` javascript
GunUtils.createUUID() // 7335e58f-e6f4-149e-5d90-de128c9d7142
GunUtils.createUUID(false) // d6a458b8d2e12c7d13bcc27244c78f56
```