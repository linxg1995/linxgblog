---
title: vue-gun-ui说明文档：Select 选择器
date: 2020-06-16 11:15:43
tags: vue-gun-ui
---
<!-- --------------------分割线-------------------- -->
实践了第一个版本，目前功能比较单一，跟el不同的是，el将option割出来作为一个独立的子组件，gun需要以后才能支持拓展。

``` html
<gun-select
    v-model="value"
    :options="options"
>
</gun-select>
```
<!-- --------------------分割线-------------------- -->
## Props
| 属性名称 | 说明 | 类型 | 默认值 | 可选值 |
| :- | :- | :- | :- | :- |
| v-model/value | 绑定值； | String / Number | - | - |
| options | 选项列表；可以是基本的<font color=red>String数组</font>或<font color=red>Number数组</font>，或<font color=red>Object数组</font>； | Array | [] | - |
| valueKey | 选中时绑定的值字段；提供给Object选项用的，如果选项是基本数据类型，则默认取自身； | String | value | - |
| labelKey | 选中时绑定的显示字段；提供给Object选项用的，如果选项是基本数据类型，则默认取自身； | String | label | - |
| placeholder | 占位符； | String | 请选择 | - |

## Events
| 事件名称 | 说明 | 返回值 |
| :- | :- | :- |
| toggleSelect | 菜单框切换显示时 | show：显示状态，Boolean类型； |
| change | 选择且绑定值改变时 | val：选中的绑定值；<br>info：包含选中的选项（如果该选项是基本数据类型，则和val相同）和下标； |