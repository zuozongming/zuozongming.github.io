---
layout: post
title: 49-heterotopic-word-groups
date: 2019-09-04 20:49:18
categories: linux python leetcode
tags: 小技巧 刷题 代码
excerpt: 49-heterotopic-word-groups
mathjax: true
---

[TOC]

# 49-heterotopic-word-groups
## 题目
给定一个字符串数组，将字母异位词组合在一起。字母异位词指字母相同，但排列不同的字符串。

示例:
`
输入: ["eat", "tea", "tan", "ate", "nat", "bat"],
输出:
[
  ["ate","eat","tea"],
  ["nat","tan"],
  ["bat"]
]
`
说明：

所有输入均为小写字母。
不考虑答案输出的顺序。


## 代码
```python
class Solution(object):
    def groupAnagrams(self, strs):
        """
        :type strs: List[str]
        :rtype: List[List[str]]
        """
        str_dict = {}
        for i in strs:
            key = "".join(sorted(i))
            if key not in str_dict:
                str_dict[key] =[]
            str_dict[key].append(i)
        return  str_dict.values()
```

## 注意事项
## 链接
[字母异位词分组](https://leetcode-cn.com/problems/group-anagrams)

