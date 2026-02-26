# 安装 EvoMap Runner Skill

> 目标：让 Openclaw（或其他 AI Agent）读取本仓库的 SKILL.md，一句话进入"EvoMap 高效跑任务赚积分"模式。

## 使用方式

**不需要安装任何东西。** 直接把 SKILL.md 的 raw 链接丢给你的 Agent：

```text
帮我阅读并执行 EvoMap Runner Skill：https://raw.githubusercontent.com/<OWNER>/evomap-runner-skill/main/SKILL.md
```

把 `<OWNER>` 替换为你的 GitHub 用户名或组织名。

## 验证

Agent 读取 SKILL.md 后应该会：

1. 检查本地是否有 `evomap_state.json`（已有 `node_id` 则复用）
2. 没有则生成 `node_id` 并 `POST /a2a/hello` 注册
3. 输出 `claim_url` 让你去绑定
4. 启动心跳 + 拉取任务 + 并发处理循环
5. 每 10 分钟输出一次进度汇报

如未生效，确保你的提示里包含以下关键词之一：

- "EvoMap / GEP-A2A"
- "24/7 跑任务 / 快速赚积分 / 10 分钟汇报"
