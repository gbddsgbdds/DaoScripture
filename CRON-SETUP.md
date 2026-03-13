# 算道理论每日迭代 - 定时任务配置

## 执行时间

**建议：每日 22:00 GMT+8**（社区活跃后，便于收集当日反馈）

---

## 配置方式

### 方式一：系统 cron（推荐）

```bash
# 编辑 crontab
crontab -e

# 添加以下行（每日 22:00 执行，GMT+8）
0 22 * * * cd /home/black/.openclaw/workspace && python3 scripts/daily-theory-iteration.py >> memory/logs/daily-iteration.log 2>&1
```

### 方式二：OpenClaw 定时任务（如支持）

在 `~/.openclaw/openclaw.json` 中添加：

```json
{
  "schedules": {
    "daily-theory-iteration": {
      "cron": "0 22 * * *",
      "command": "python3 /home/black/.openclaw/workspace/scripts/daily-theory-iteration.py",
      "enabled": true
    }
  }
}
```

### 方式三：手动执行

```bash
cd /home/black/.openclaw/workspace
python3 scripts/daily-theory-iteration.py
```

---

## 环境变量要求

脚本需要以下环境变量（从 `.secrets/instreet.env` 自动加载）：

```bash
INSTREET_BASE_URL=https://instreet.coze.site
INSTREET_API_KEY=your_api_key_here
```

GitHub Token（可选，用于收集 GitHub Issues）：

```bash
export GITHUB_TOKEN=your_github_token
```

---

## 输出位置

| 类型 | 位置 |
|-----|------|
| 反馈报告 | `memory/feedback/YYYY-MM-DD.md` |
| 执行日志 | `memory/logs/daily-iteration.log` |
| Git 提交 | `DaoScripture` 仓库 |

---

## 执行后检查清单

- [ ] 反馈报告已生成（`memory/feedback/今日日期.md`）
- [ ] 待处理项已审阅
- [ ] 核心冲突项已标记（需社群讨论）
- [ ] Git 提交成功（如有文档更新）
- [ ] 关键进展写入 `memory/当日文件.md`

---

## 故障处理

### 问题：InStreet API 失败

```bash
# 检查 API key
cat ~/.openclaw/workspace/.secrets/instreet.env

# 测试连接
curl -H "Authorization: Bearer YOUR_KEY" https://instreet.coze.site/api/v1/agents/me
```

### 问题：Git 推送失败

```bash
cd /home/black/.openclaw/workspace/DaoScripture
git status
git remote -v
ssh -T git@github.com  # 测试 SSH 连接
```

### 问题：脚本语法错误

```bash
python3 -m py_compile /home/black/.openclaw/workspace/scripts/daily-theory-iteration.py
```

---

## 版本

- v1.0 - 2026-03-13 - 初始版本
