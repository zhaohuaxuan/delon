---
type: CURD
title: view
subtitle: 查看
cols: 1
order: 2
module: NaViewModule
config: NaViewConfig
---

查看栅格系统是在原 [Grid 栅格](https://ng.ant.design/components/grid/zh) 基础上构建更高阶的组件，用于简化查看页布局。

## API

### na-view-wrap

| 参数           | 说明                 | 类型                    | 默认值       |
| -------------- | -------------------- | ----------------------- | ------------ |
| `[size]`       | 大小                 | `small | large`         | `large`      |
| `[layout]`     | 布局                 | `horizontal | vertical` | `horizontal` |
| `[gutter]`     | 间距                 | `number`                | `32`         |
| `[col]`        | 指定信息最多分几列展示，最终一行几列由 col 配置结合[响应式规则](#响应式规则)决定         | `number(0 < col <= 6)`                | `3`          |
| `[labelWidth]` | 默认标签文本宽度     | `number`                | `null`       |
| `[default]`    | 默认是否显示默认文本 | `boolean`               | `true`       |

### na-view

| 参数           | 类型                                  | 说明                                   |默认值       |
| -------------- | ------------------------------------- | -------------------------------------- |
| `[col]`        | 指定信息最多分几列展示，最终一行几列由 col 配置结合[响应式规则](#响应式规则)决定，继承 `na-view-wrap`         | `number(0 < col <= 6)`                               | - |
| `[label]`      | 标签                                  | `string | TemplateRef<any>`            | - |
| `[labelWidth]` | 标签文本宽度，继承 `na-view-wrap`     | `number`                               | - |
| `[default]`    | 是否显示默认文本，继承 `na-view-wrap` | `boolean`                              | - |
| `[type]`       | 类型                  | `primary | success | danger | warning` | - |

### na-view-title

用于展示标题，单独一行。

## 响应式规则

假如指定 `col: 6` 时，按以下规则显示列数：

| 窗口宽度  | 展示列数 |
| --------- | -------- |
| `≥1600px` | `12`     |
| `≥1200px` | `6`      |
| `≥992px`  | `4`      |
| `≥768px`  | `3`      |
| `≥576px`  | `2`      |
| `<576px`  | `1`      |