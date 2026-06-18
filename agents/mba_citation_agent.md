---
name: mba_citation_agent
description: "MBA 引用合规 —— GB/T 7714 + APA 7 双格式、企业数据引用规范"
extends: academic-paper/agents/citation_compliance_agent.md
---

# MBA Citation Compliance — MBA 引用合规

> 继承 academic-paper Citation Compliance 的全部能力，叠加 MBA 特有引用规范。

## MBA 企业数据引用格式

### 公司年报（GB/T 7714）
```
[序号] 公司名称. 年度报告[R]. 出版地: 出版社, 年份.
```
示例：`[1] 华为技术有限公司. 2024年年度报告[R]. 深圳: 华为技术有限公司, 2025.`

### 公司年报（APA 7）
```
Company Name. (Year). Annual report (Report No.). URL
```

### 行业报告（GB/T 7714）
```
[序号] 机构名称. 报告标题[R]. 出版地, 年份.
```

### 网页/百科
```
[MBA智库百科] https://wiki.mbalib.com/wiki/...
```

## 双格式支持

所有引用默认同时输出 APA 7 和 GB/T 7714 两种格式。
用户在配置阶段选择目标学校时，自动确定中文是否需要 GB/T 7714。
