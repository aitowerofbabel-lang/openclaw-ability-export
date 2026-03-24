---
name: openclaw-ability-export
description: |
  能力包导出/导入工具。用于将当前 agent 的配置打包分享，或从他人的能力包导入配置。
  触发场景：
  - 导出："导出能力包"、"打包我的能力"、"export ability"
  - 导入："导入能力包"、"学习能力包"、"import ability"
---

# Ability Package - 能力包工具

在聊天中直接导出/导入能力包，无需文件传输。

## 核心文件

需要导出/导入的核心配置文件：
- AGENTS.md
- SOUL.md
- TOOLS.md
- IDENTITY.md
- MEMORY.md

---

## 导出 (Export)

### 触发词
"导出能力包"、"打包我的能力"、"export ability"

### 执行步骤

1. **扫描核心文件**：读取 workspace 根目录下的核心配置文件
2. **生成 .md 格式**：按以下模板生成能力包

```markdown
# 能力包：{名称}
- 版本：1.0
- 导出时间：{时间}
- 来源：{agent 标识}

---

## AGENTS.md
{文件完整内容}

---

## SOUL.md
{文件完整内容}

---

## TOOLS.md
{文件完整内容}

---

## IDENTITY.md
{文件完整内容}

---

## MEMORY.md
{文件完整内容}
```

3. **发送到聊天**：直接发送生成的 .md 内容给用户

### 示例

```
用户：导出能力包
→ 扫描 AGENTS.md、SOUL.md、TOOLS.md、IDENTITY.md、MEMORY.md
→ 生成 .md 格式能力包
→ 直接发送到聊天窗口
```

---

## 导入 (Import)

### 触发词
"导入能力包"、"学习能力包"、"import ability"

### 执行步骤

1. **读取能力包**：用户发送 .md 格式的能力包内容（或提供文件路径）
2. **解析内容**：识别各个 section（AGENTS.md、SOUL.md 等）
3. **展示选项**：告诉用户这个包包含哪些内容，询问要导入哪些

示例回复：
> 这个能力包包含：
> - AGENTS.md ✓
> - SOUL.md ✓
> - TOOLS.md ✓
> - IDENTITY.md ✓
> - MEMORY.md ✓
>
> 你想导入哪些？（回复"全部"或具体名称，如"TOOLS.md 和 SOUL.md"）

4. **写入文件**：根据用户选择，将对应内容写入 workspace 根目录的同名文件
5. **确认完成**：告知用户导入结果

### 合并规则

- 如果文件已存在，**覆盖**写入
- 用户选择哪些，就写入哪些（不是全部）

---

## 注意事项

1. **纯文本传输**：直接在聊天中发送/接收 .md 内容，无需单独文件传输
2. **选择性导入**：不是全量覆盖，用户可以只选需要的部分
3. **安全考虑**：导出前可以提醒用户，MEMORY.md 可能包含隐私内容
