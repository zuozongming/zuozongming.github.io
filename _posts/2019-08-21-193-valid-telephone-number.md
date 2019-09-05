---
layout: post
title: 193-valid-telephone-number
date: 2019-08-21 15:39:58
categories: linux shell leetcode
tags: 小技巧 刷题 代码
excerpt: 193-valid-telephone-number
mathjax: true
---

[TOC]

# 193-valid-telephone-number
## 题目
给定一个包含电话号码列表（一行一个电话号码）的文本文件 file.txt，写一个 bash 脚本输出所有有效的电话号码。

你可以假设一个有效的电话号码必须满足以下两种格式： (xxx) xxx-xxxx 或 xxx-xxx-xxxx。（x 表示一个数字）

你也可以假设每行前后没有多余的空格字符。

示例:

假设 file.txt 内容如下：
`
987-123-4567
123 456 7890
(123) 456-7890
`
你的脚本应当输出下列有效的电话号码：
`
987-123-4567
(123) 456-7890
`
## 代码
```shell
awk --re-interval '/^([0-9]{3}-|\([0-9]{3}\) )[0-9]{3}-([0-9]{4})$/' file.txt
```
## 注意事项
awk 版本不同 部分版本需--re-interval 正则才能生效
       -W re-interval
       --re-interval
              Enable the use of interval expressions in regular expression matching (see Regular Expressions, below).  Interval expressions were not traditionally available in the AWK language.  
              The POSIX standard added them, to  make  awk  and
              egrep consistent with each other.  However, their use is likely to break old AWK programs, so gawk only provides them if they are requested with this option, or when --posix is specified.
## 链接
[有效电话号码](https://leetcode-cn.com/problems/valid-phone-numbers)
