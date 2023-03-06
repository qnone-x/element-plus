---
title: Popconfirm 气泡确认框
lang: zh-CN
---

# Popconfirm 气泡确认框

点击某个元素弹出一个简单的气泡确认框

:::tip

在 SSR 场景下，您需要将组件包裹在 `<client-only></client-only>` 之中 (如: [Nuxt](https://nuxt.com/v3)) 和 SSG (e.g: [VitePress](https://vitepress.vuejs.org/)).

:::

## 基础用法

Popconfirm 的属性与 Popover 很类似， 因此对于重复属性，请参考 Popover 的文档，在此文档中不做详尽解释。

:::demo 在 Popconfirm 中，只有 `title` 属性可用，`content` 属性会被忽略。

popconfirm/basic-usage

:::

## 自定义弹出框的内容

可以在 Popconfirm 中自定义内容。

:::demo

popconfirm/customize

:::

## 多种让 Popconfirm 出现的方法

点击按钮触发事件

:::demo

popconfirm/trigger-event

:::

## Attributes

| 属性名                 | 说明                                                              | 类型                     | 可选值                                                | 默认值             |
| ------------------- | --------------------------------------------------------------- | ---------------------- | -------------------------------------------------- | --------------- |
| title               | 标题                                                              | String                 | —                                                  | —               |
| confirm-button-text | 确认按钮文字                                                          | String                 | —                                                  | —               |
| cancel-button-text  | 取消按钮文字                                                          | String                 | —                                                  | —               |
| confirm-button-type | 确认按钮类型                                                          | String                 | primary / success / warning / danger / info / text | primary         |
| cancel-button-type  | 取消按钮类型                                                          | String                 | primary / success / warning / danger / info / text | text            |
| icon                | 自定义图标                                                           | `string \| Component` | —                                                  | QuestionFilled  |
| icon-color          | Icon 颜色                                                         | String                 | —                                                  | #f90            |
| hide-icon           | 是否隐藏 Icon                                                       | Boolean                | —                                                  | false           |
| teleported          | 是否将 popover 的下拉列表插入至 body 元素                                    | boolean                | true / false                                       | true            |
| persistent          | 当 popover 组件长时间不触发且 `persistent` 属性设置为 `false` 时, popover 将会被删除 | boolean                | —                                                  | false           |
| width               | 弹出窗口宽度                                                          | string/number          | -                                                  | Min width 150px |

## Slots

| 插槽名       | 说明                        |
| --------- | ------------------------- |
| reference | 触发 Popconfirm 显示的 HTML 元素 |

## Events

| 事件名     | 说明        | 回调参数 |
| ------- | --------- | ---- |
| confirm | 点击确认按钮时触发 | —    |
| cancel  | 点击取消按钮时触发 | —    |
