---
title: vue-gun-ui说明文档：ScrollContainer 滚动容器
date: 2020-05-06 18:05:18
tag: vue-gun-ui
---
<!-- --------------------分割线-------------------- -->
<!-- updated:2020/04/13 -->

参考了 [Element UI](https://element.eleme.cn/#/zh-CN) 的scrollbar(官方文档中没有)，自己试着写了一个。
和el不同的是，el的高度定义为100%，所以需要一个定义了高度的外容器包裹，然后作为内容器包裹内容。gun则是自己作为容器来包裹内容，<font color=red>需要定义自己的高度</font>。
当然，如果想用原生js实现，我这样的思路可能不行。

``` html
<gun-scroll-container style="height: 200px">
    <div>...</div>
</gun-scroll-container>
```
<!-- --------------------分割线-------------------- -->
## Props
| 属性名称 | 说明 | 类型 | 默认值 | 可选值 |
| :- | :- | :- | :- | :- |
| showX | 显示X滚动条； | Boolean | false | - |

## Events
| 事件名称 | 说明 | 返回值 |
| :- | :- | :- |
| scroll | 滚动时的触发 | 原生Event事件对象 |

## Slots
| 插槽名称 | 说明 |
| :- | :- |
| - | 默认。容器中的内容 |