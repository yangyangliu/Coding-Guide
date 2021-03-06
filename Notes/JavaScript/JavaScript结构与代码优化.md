<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [文件结构优化](#%E6%96%87%E4%BB%B6%E7%BB%93%E6%9E%84%E4%BC%98%E5%8C%96)
- [代码优化](#%E4%BB%A3%E7%A0%81%E4%BC%98%E5%8C%96)
- [编码规范](#%E7%BC%96%E7%A0%81%E8%A7%84%E8%8C%83)
- [webpack配置](#webpack%E9%85%8D%E7%BD%AE)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---
title: JavaScript结构与代码优化
date: 2016-03-05 09:25:28
tags: JavaScript
---

> 程序是给人读的，只是偶尔让计算机执行一下

在网站构建过程中，随着其功能的逐步增加，代码量和复杂深度也成倍增加。随之而来的是维护难度和开发成本。修改麻烦不说，更有可能会误伤友军。因此首先探讨一下js的优化方案。

## 文件结构优化

- 相关的文件按照功能/web-page分类
- 一个文件只包含一个对象

## 代码优化

- 编写通用类函数
  - 抽离类似UI层，作为模板
  - 抽离工具类函数
  - 通用函数内use let instead of var，避免全局变量污染
  - 高内聚，仅暴露接口
- 配置数据分离
  - 静态常量增加统一入口，export出去
- 隔离应用逻辑
  - 函数拆分，各个函数独立负责自己本身的职能
  - 应用逻辑是和应用功能相关的功能性代码，而不是和用户行为相关的
  - 交互->分发交互函数->触发应用逻辑函数

## 编码规范

- 命名规范
  - 小驼峰式命名法（首字母小写）命名函数/变量
  - 大驼峰式命名法（全大写）命名文件
  - 全大写+单词之间下划线连接（MAX_COUNT）命名常量
- 注释文档
  - 中大型函数前使用注释说明参数

## webpack配置

---

to be continue...