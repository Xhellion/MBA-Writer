---
name: citation_generator
description: "引用格式生成 — APA 7 + GB/T 7714 双格式"
triggers: ["生成引用", "引用格式", "GB/T 7714", "APA"]
---

# Citation Generator — 引用格式生成器

## 触发条件

用户输入包含以下关键词时激活：
- "生成引用" / "引用格式"
- "GB/T 7714" / "APA" / "Chicago"
- 在写作流程中需要引用某个理论

## 支持的引用格式

| 格式 | 适用场景 | 默认 |
|------|---------|------|
| APA 7.0 | 国际期刊、英文论文 | ✅ |
| GB/T 7714 | 中国学位论文、中文期刊 | ✅ |
| Chicago (Author-Date) | 部分商科期刊 | 可选 |

## 输出格式

用户输入："引用德鲁克 目标管理" 或 "引用彼得·德鲁克《管理的实践》"

```markdown
## 引用格式

### APA 7.0
Drucker, P. F. (1954). *The Practice of Management*. Harper & Row.

### GB/T 7714
德鲁克 P F. 管理的实践[M]. 北京: 机械工业出版社, 1954.

### 来源链接
- [MBA智库百科 - 目标管理](https://wiki.mbalib.com/wiki/目标管理)
- [理论库详情](data/...)

---

## 批量生成

用户可一次请求多条引用：
"生成引用：德鲁克目标管理、波特五力、马斯洛需求层次"

输出为：
1. [德鲁克] APA + GB/T
2. [波特] APA + GB/T
3. [马斯洛] APA + GB/T
```
