# openclaw-ability-export

能力包导出 / 导入工具。在聊天中直接打包或接收 agent 配置，支持选择性导入、合并规则与隐私提醒。

## 功能

- **导出能力包**：扫描核心配置文件（AGENTS.md、SOUL.md、TOOLS.md、IDENTITY.md、MEMORY.md），生成 Markdown 格式能力包，直接发送到聊天窗口
- **导入能力包**：解析能力包内容，让用户选择要导入哪些配置
- **选择性导入**：支持部分导入，非全量覆盖
- **安全提醒**：导出时提醒 MEMORY.md 隐私风险，导入时展示预览

## 触发词

- 导出：`导出能力包`、`打包我的能力`、`export ability`
- 导入：`导入能力包`、`学习能力包`、`import ability`

## 导出的文件

| 文件 | 说明 |
|------|------|
| `AGENTS.md` | Agent 工作空间规则与约定 |
| `SOUL.md` | Agent 人格与行为准则 |
| `TOOLS.md` | 本地工具配置与笔记 |
| `IDENTITY.md` | Agent 身份标识 |
| `MEMORY.md` | 长期记忆与偏好记录 |

## 使用示例

```
用户：导出能力包
Agent：→ 生成 Markdown 格式能力包，直接发送

用户：[粘贴能力包内容]
Agent：→ 展示预览，告诉用户包含哪些文件
  请告诉我想导入哪些？（回复"全部"或具体文件名）
```

## 安装

```bash
npx skills add openclaw-ability-export
```
