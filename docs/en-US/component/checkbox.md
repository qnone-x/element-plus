---
title: Checkbox 多选框
lang: zh-CN
---

# Checkbox 多选框

在一组备选项中进行多选。

## 基础用法

单独使用可以表示两种状态之间的切换，写在标签中的内容为 checkbox 按钮后的介绍。

:::demo `checkbox-group`元素能把多个 checkbox 管理为一组，只需要在 Group 中使用 `v-model` 绑定 `Array` 类型的变量即可。 只有一个选项时的默认值类型为 `Boolean`，当选中时值为`true`。 `el-checkbox` 标签中的内容将成为复选框按钮之后的描述。

checkbox/basic

:::

## 禁用状态

多选框不可用状态。

:::demo 设置 `disabled` 属性即可。

checkbox/disabled

:::

## 多选框组

适用于多个勾选框绑定到同一个数组的情景，通过是否勾选来表示这一组选项中选中的项。

:::demo 在 `el-checkbox` 元素中定义 `v-model` 绑定变量，单一的 `checkbox` 中，默认绑定变量的值会是 `Boolean`，选中为 `true`。 在 `el-checkbox` 组件中，`label` 是选择框的值。 如果该组件下没有被传入内容，那么 `label` 将会作为 checkbox 按钮后的介绍。 `label` 也与数组中的元素值相对应。 如果指定的值存在于数组中，就处于选择状态，反之亦然。

checkbox/grouping

:::

## 中间状态

`indeterminate` 属性用以表示 checkbox 的不确定状态，一般用于实现全选的效果

:::demo

checkbox/intermediate

:::

## 可选项目数量的限制

使用 `min` 和 `max` 属性能够限制可以被勾选的项目的数量。

:::demo

checkbox/limitation

:::

## 按钮样式

按钮样式的多选组合。

:::demo 只需要把 `el-checkbox` 元素替换为 `el-checkbox-button` 元素即可。 此外，Element Plus 还提供了`size`属性。

checkbox/button-style

:::

## 带有边框

:::demo 设置`border`属性可以渲染为带有边框的多选框。

checkbox/with-border

:::

## Checkbox API

### Checkbox Attributes

| 属性名                   | 说明                                                                                                                                         | 类型                                             | 默认值   |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- | ----- |
| model-value / v-model | 选中项绑定值                                                                                                                                     | ^[string] / ^[number] / ^[boolean]             | —     |
| label                 | 选中状态的值（只有在`checkbox-group`或者绑定对象类型为`array`时有效）                                                                                             | ^[string] / ^[number] / ^[boolean] / ^[object] | —     |
| true-label            | 选中时的值                                                                                                                                      | ^[string] / ^[number]                          | —     |
| false-label           | 没有选中时的值                                                                                                                                    | ^[string] / ^[number]                          | —     |
| disabled              | 是否禁用                                                                                                                                       | ^[boolean]                                     | false |
| border                | 是否显示边框                                                                                                                                     | ^[boolean]                                     | false |
| size                  | Checkbox 的尺寸                                                                                                                               | ^[enum]`'large' \| 'default' \| 'small'`     | —     |
| name                  | 原生 name 属性                                                                                                                                 | ^[string]                                      | —     |
| checked               | 当前是否勾选                                                                                                                                     | ^[boolean]                                     | false |
| indeterminate         | 设置不确定状态，仅负责样式控制                                                                                                                            | ^[boolean]                                     | false |
| validate-event        | 输入时是否触发表单的校验                                                                                                                               | ^[boolean]                                     | true  |
| tabindex              | 输入框的 tabindex                                                                                                                              | ^[string] / ^[number]                          | —     |
| id                    | input id                                                                                                                                   | ^[string]                                      | —     |
| controls <A11yTag />  | 与 [aria-control](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-controls)一致, 当 `indeterminate`为 `true`时生效 | ^[boolean]                                     | —     |

### Checkbox Events

| 事件名    | 说明           | 类型                                                             |
| ------ | ------------ | -------------------------------------------------------------- |
| change | 当绑定值变化时触发的事件 | ^[Function]`(value: string \| number \| boolean) => void` |

### Checkbox Slots

| 插槽名     | 说明      |
| ------- | ------- |
| default | 自定义默认内容 |

## CheckboxGroup API

### CheckboxGroup Attributes

| 属性名                   | 说明                   | 类型                                         | 默认值     |
| --------------------- | -------------------- | ------------------------------------------ | ------- |
| model-value / v-model | 绑定值                  | ^[object]`string[] \| number[]`           | []      |
| size                  | 多选框组尺寸               | ^[enum]`'large' \| 'default' \| 'small'` | —       |
| disabled              | 是否禁用                 | ^[boolean]                                 | false   |
| min                   | 可被勾选的 checkbox 的最小数量 | ^[number]                                  | —       |
| max                   | 可被勾选的 checkbox 的最大数量 | ^[number]                                  | —       |
| label                 | 为屏幕阅读器准备的标签          | ^[string]                                  | —       |
| text-color            | 当按钮为活跃状态时的字体颜色       | ^[string]                                  | #ffffff |
| fill                  | 当按钮为活跃状态时的边框和背景颜色    | ^[string]                                  | #409EFF |
| tag                   | 复选框组元素标签             | ^[string]                                  | div     |
| validate-event        | 是否触发表单验证             | ^[boolean]                                 | true    |

### CheckboxGroup Events

| 事件名    | 说明           | 类型                                                     |
| ------ | ------------ | ------------------------------------------------------ |
| change | 当绑定值变化时触发的事件 | ^[Function]`(value: string[] \| number[]) => void` |

### CheckboxGroup Slots

| 插槽名     | 说明      | 子标签                        |
| ------- | ------- | -------------------------- |
| default | 自定义默认内容 | Checkbox / Checkbox-button |

## CheckboxButton API

### CheckboxButton Attributes

| 属性名         | 说明                             | 类型                                             | 默认值   |
| ----------- | ------------------------------ | ---------------------------------------------- | ----- |
| label       | 选中状态的值，只有在绑定对象类型为 `array` 时有效。 | ^[string] / ^[number] / ^[boolean] / ^[object] | —     |
| true-label  | 选中时的值                          | ^[string] / ^[number]                          | —     |
| false-label | 没有选中时的值                        | ^[string] / ^[number]                          | —     |
| disabled    | 是否禁用                           | ^[boolean]                                     | false |
| name        | 原生 name 属性                     | ^[string]                                      | —     |
| checked     | 当前是否勾选                         | ^[boolean]                                     | false |

### CheckboxButton Slots

| 插槽名     | 描述      |
| ------- | ------- |
| default | 自定义默认内容 |
