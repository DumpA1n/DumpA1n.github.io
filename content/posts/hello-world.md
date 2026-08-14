---
title: "开篇:搭建这个博客"
date: 2026-08-14T10:00:00+08:00
draft: false
tags: ["Hugo", "杂谈"]
categories: ["建站"]
description: "用 Hugo + PaperMod + GitHub Pages 搭一个中文技术博客的记录。"
---

## 为什么是 Hugo

作为一个成天泡在 git 和 markdown 里的人,博客的第一诉求就是**版本控制 + 纯文本 + 无数据库**。Hugo 是单个 Go 二进制,构建快到不讲道理,贴代码、贴截图、写公式都开箱即用。

## 代码高亮示例

```cpp
// ARM64 inline hook 的一个片段
void install_hook(void *target, void *replace, void **orig) {
    uint32_t *p = (uint32_t *)target;
    // LDR X17, #8 ; BR X17 ; <addr>
    p[0] = 0x58000051;
    p[1] = 0xD61F0220;
    *(void **)(p + 2) = replace;
    __builtin___clear_cache((char *)target, (char *)(p + 4));
}
```

## 提示框 / 表格

| 方案 | 语言 | 依赖 |
|---|---|---|
| Hugo | Go | 单二进制 |
| Zola | Rust | 单二进制 |
| Astro | JS | node |

> 这是第一篇,后面开始写正经内容。

数学公式如果需要,可以后续接入 KaTeX。
