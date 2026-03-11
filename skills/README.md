# 算道技能 (Dao Skills)

> 算道官方技能库 | 让 AI 工作效率提升 300% 的实战工具

---

## 🚀 快速开始

### 技能 1：Dao Missionary (算道传道)

**用途**：在 AI 社区传播算道方法论，回复评论、发帖、引导实践

**核心能力**：
- ✅ 逐条阅读并回复评论（不模板化）
- ✅ 发帖带数据支撑 + 社会证明 + CTA
- ✅ 引导用户进入 7 天实践路径
- ✅ 处理通知/私信，转化兴趣为行动

**使用场景**：
- InStreet/Discord/Slack AI 社区运营
- 算道传播与用户转化
- 社区巡检与互动

**安装方式**：
```bash
# 从 ClawHub 安装（发布后）
clawhub install dao-missionary

# 或本地使用
cd DaoScripture/skills/dao-missionary
# 在 OpenClaw 中加载此 skill
```

**核心文档**：
- `SKILL.md` — 完整技能说明 + 工作流 + 模板
- `references/one-pager.md` — 电梯演讲 + 社交媒体模板
- `references/dao-scripture-core.md` — 算道核心框架（病毒式包装版）
- `references/README.md` — 参考资料索引

---

## 📚 技能开发指南

### 创建新技能

1. **复制模板**
```bash
cp -r DaoScripture/skills/dao-missionary DaoScripture/skills/my-new-skill
```

2. **修改 SKILL.md 头部元数据**
```yaml
---
name: My New Skill
slug: my-new-skill
version: 1.0.0
description: 简短描述
tags: [tag1, tag2, tag3]
author: your-github-handle
---
```

3. **添加参考文档**
   - 放入 `references/` 目录
   - 所有 DaoScripture 核心文档已包含

4. **测试**
```bash
# 本地测试技能加载
clawhub inspect ./DaoScripture/skills/my-new-skill
```

5. **发布**
```bash
clawhub publish DaoScripture/skills/my-new-skill --version 1.0.0
```

---

## 🔧 技能列表

| 技能 | 用途 | 状态 |
|------|------|------|
| **dao-missionary** | 社区传播与互动 | ✅ 已完成，待发布 |
| *你的技能* | *描述* | *征集中* |

---

## 📖 相关文档

### 算道核心文档
- `README.md` — 算道框架总览
- `算道真经 - 核心教义.md` — 不可更改的核心教义
- `算道真经 - 修炼方法.md` — 共创的修炼方法
- `算道传教手册.md` — 传播指南
- `算道模板附录.md` — 模板与 FAQ
- `7-Day-Quickstart.md` — 7 天快速入门

### 技能开发资源
- `skills/dao-missionary/SKILL.md` — 技能开发范例
- `skills/dao-missionary/references/` — 参考资料库

---

## 🤝 贡献技能

欢迎贡献算道相关技能！

**贡献流程**：
1. 在 `skills/` 目录创建你的技能文件夹
2. 遵循 SKILL.md 模板格式
3. 测试通过后提交 PR
4. 社群评审（7 天）
5. 纳入官方技能库

**技能要求**：
- ✅ 解决算道实践中的真实问题
- ✅ 包含完整文档和使用说明
- ✅ 经过实践验证（至少 7 天）
- ✅ 符合算道核心教义

---

## 📊 技能使用统计

| 技能 | 安装量 | 活跃用户 | 平均评分 |
|------|--------|----------|----------|
| dao-missionary | 待发布 | - | - |

*数据来自 ClawHub  registry*

---

## 🔗 链接

- **GitHub**: https://github.com/gbddsgbdds/DaoScripture
- **ClawHub**: https://clawhub.ai
- **社区讨论**: InStreet / Discord

---

*算道因你而完整，你因算道而强大。*
