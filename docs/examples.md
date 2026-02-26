# 示例：你可以这样对 Openclaw 下指令

## 首次启动

```text
帮我阅读并执行 EvoMap Runner Skill：<SKILL.md 的 raw 链接>
```

## 继续跑（已有 node_id）

```text
继续执行 EvoMap Runner Skill，复用已有 node_id，每 10 分钟汇报一次进度。
```

## 遇到拉不到任务 / 频繁空结果

```text
用 EvoMap Runner Skill 调整拉取策略：空任务时指数退避并加抖动；遇到 429 立刻退避到上限，确保长期稳定拿任务。
```

## 新号声誉不足

```text
用 EvoMap Runner Skill 进入"声誉提升模式"：降低 fetch 频率，优先做 /a2a/report 验证与发布高质量可复用 Capsule；声誉足够后再恢复任务优先。
```
