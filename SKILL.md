---
name: mba-writing-pod
description: "MBA 论文全流程写作舱 — 12 代理 8 阶段流水线 + 194 条管理理论库 + 6 大特色模块。基于 academic-paper 的学术论文能力，叠加 MBA 学科特化。"
---

# MBA 写作舱 — MBA 论文全流程写作 Skill

> 集成 academic-paper v3.2+ 的 12 代理论文流水线，叠加 MBA 学科特化和 194 条管理理论库
> 技能版本: v1.0 | 更新日期: 2026-06-17

**Depends on:** academic-paper (≥ v3.2.0)

## 快速开始

**全流水线写作：**
```
帮我写一篇MBA论文，题目是XX公司的XX问题研究
帮我规划MBA论文——我想研究新能源车企的用户运营
```

**单模块调用：**
```
推荐理论——我在写第三章用户运营现状分析
检查逻辑——[粘贴草稿]
用波特五力分析华为手机业务
大师怎么看——员工流失率居高不下
查重——[粘贴内容]
生成引用——德鲁克 目标管理 1954
```

## 操作模式

| 模式 | 触发词 | 说明 |
|------|--------|------|
| `full` | "写MBA论文"、"写MBA案例分析" | 8 阶段全流水线，继承 academic-paper，MBA 学科特化 |
| `plan` | "规划MBA论文"、"帮我规划MBA" | Socratic 逐步引导，MBA 论文逐章规划 |
| `theory` | "推荐理论"、"用什么理论" | ①理论推荐引擎——场景→理论匹配 |
| `logic` | "检查逻辑"、"帮我审一段" | ②段落逻辑检查——论证完整度检测 |
| `template` | "生成分析框架"、"用XX分析XX" | ③分析模板生成——结构化表格 |
| `master` | "大师怎么看"、"视角匹配" | ④大师视角匹配——管理问题→理论视角 |
| `plagiarism` | "查重"、"检查抄袭" | ⑤查重预警——百科内容相似度检测 |
| `cite` | "生成引用"、"引用格式" | ⑥引用格式生成——GB/T 7714 + APA |
| `revision` | "修改MBA论文" | revision 模式，MBA 特化版 |
| `format` | "转PDF"、"转学校格式" | format-convert 模式，含学校模板 |
| `abstract` | "写MBA摘要" | abstract-only 模式，商务双语 |

**模式选择规则：**
1. 触发词在 6 个模块范围内 → 单模块调用
2. "写"/"规划"/"修改" → 全流水线
3. 同时满足 → 询问用户

## 8 阶段流水线

```
Phase 0 ─── MBA Intake Agent         (配置面谈：论文类型/学校/格式)
Phase 1 ─── MBA Literature Strategist (商业文献 + 理论库检索)
Phase 2 ─── MBA Structure Architect   (7章论文/案例分析/商业报告)
Phase 3 ─── MBA Argument Builder      (理论-数据-实践三元论证)
Phase 4 ─── MBA Draft Writer          (实战风格/案例驱动)
Phase 5ab ─ MBA Citation + Abstract   (APA7+GB7714/商务双语)
Phase 6 ─── MBA Peer Reviewer         (MBA 论文五维评分)
Phase 7 ─── MBA Formatter             (学校模板/答辩PPT)
```

## 6 大特色模块

详见 `agents/modules/` 目录：
- [theory_recommender.md](agents/modules/theory_recommender.md) — 场景→理论自动匹配
- [logic_checker.md](agents/modules/logic_checker.md) — 段落逻辑+理论支撑检测
- [template_generator.md](agents/modules/template_generator.md) — 结构化分析表格生成
- [master_match.md](agents/modules/master_match.md) — 管理问题→大师视角
- [plagiarism_checker.md](agents/modules/plagiarism_checker.md) — 百科内容查重+改写
- [citation_generator.md](agents/modules/citation_generator.md) — GB/T 7714 + APA 格式

## 集成示例

```
academic-paper + mba-writing-pod  →  MBA 论文全流程写作 + 理论智能匹配
deep-research + mba-writing-pod   →  深度研究 → MBA 论文自动写作
mba-writing-pod + academic-paper-reviewer → MBA 论文同行评审
```

## 反模式

| # | 反模式 | 正确做法 |
|---|--------|---------|
| 1 | 使用 database/SQLite 存储理论 | 使用 `data/` 目录下的 Markdown 文件 |
| 2 | 修改 academic-paper 原始文件 | 所有修改在 MBA 适配层完成 |
| 3 | 忽略理论库的知识 | 理论库是 MBA 写作的核心竞争力，每个阶段都会用到 |
