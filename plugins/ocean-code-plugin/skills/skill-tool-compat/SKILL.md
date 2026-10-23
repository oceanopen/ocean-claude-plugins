---
name: skill-tool-compat
description: 定义工具加载兼容性契约：未预加载工具经 ToolSearch 加载（默认检索不到时精确探测）、TODO 工具（TaskCreate/Get/List/Stop/Update）检索不到时的配置提示、Glob/Grep 收敛为 Bash 的等价执行规则，供各命令与技能引用
---

# 工具加载兼容性契约

## 1. 工具加载与探测

`AskUserQuestion` 等交互工具可能未在本会话预加载，调用前先经 `ToolSearch` 加载。默认方式（`|` 交替、宽泛关键词）检索不到 → 精确探测（如 `select:TaskCreate`）。以**调用结果**为最终判据，确认不可用才降级为正文选项提问并说明原因。

## 2. TODO 工具检索不到时的提示

`TaskCreate`/`TaskGet`/`TaskList`/`TaskStop`/`TaskUpdate` 精确探测仍检索不到时，正文提示用户：可在 `~/.claude/settings.json` 的 `env` 中增加以下配置，重启会话生效：

```json
{
  "env": {
    "CLAUDE_CODE_ENABLE_TODO_TOOLS": "1"
  }
}
```

## 3. Glob/Grep 收敛为 Bash

Glob/Grep 已收敛为 Bash：识别不到时直接用 `rg`/`grep`/`find` 等价执行，不中断流程。
