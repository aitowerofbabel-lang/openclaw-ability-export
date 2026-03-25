# openclaw-ability-export

> Ability Package Export / Import Tool | 能力包导出/导入工具

Export your agent configuration as a shareable Markdown bundle, or import someone else's — directly in chat.

在聊天中直接打包或接收 agent 配置，支持选择性导入、合并规则与隐私提醒。

---

## Features | 功能

- **Export** | **导出**：Scan five core config files and generate a Markdown ability package, sent directly in chat
- **Import** | **导入**：Parse incoming ability packages, preview contents, and let users choose what to import
- **Selective Import** | **选择性导入**：Import only specific files, not everything
- **Security Reminders** | **安全提醒**：Warn before exporting MEMORY.md, show preview before importing

---

## Trigger Words | 触发词

| Action | Export | Import |
|--------|--------|--------|
| Chinese | `导出能力包`、`打包我的能力` | `导入能力包`、`学习能力包` |
| English | `export ability` | `import ability` |

---

## Exported Files | 导出的文件

| File | Description |
|------|-------------|
| `AGENTS.md` | Agent workspace rules and conventions |
| `SOUL.md` | Agent personality and behavior guidelines |
| `TOOLS.md` | Local tools configuration and notes |
| `IDENTITY.md` | Agent identity |
| `MEMORY.md` | Long-term memory and preferences |

---

## Quick Start | 快速开始

### Export | 导出

```
User: 导出能力包 / export ability
Agent: → Scans config files → Generates Markdown bundle → Sends in chat
```

### Import | 导入

```
User: [Paste ability package content]

Agent: Shows preview of all included files
  Please tell me which files to import? (reply "all" or specific names)

User: 全部 / all
Agent: ✓ All files updated
```

---

## Install | 安装

```bash
npx skills add openclaw-ability-export
```

Or browse on [ClawhHub](https://clawhub.com/skills/openclaw-ability-export).
