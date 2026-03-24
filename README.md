# ability-pkg

能力包导出/导入工具。用于将当前 agent 的配置打包分享，或从他人的能力包导入配置。

## 功能

- **导出能力包**：扫描核心配置文件（AGENTS.md、SOUL.md、TOOLS.md、IDENTITY.md、MEMORY.md），生成 .md 格式能力包，**直接发送到聊天窗口**
- **导入能力包**：解析能力包内容，让用户选择要导入哪些配置

## 触发词

- 导出："导出能力包"、"打包我的能力"、"export ability"
- 导入："导入能力包"、"学习能力包"、"import ability"

## 使用示例

```
用户：导出能力包
→ 扫描 AGENTS.md、SOUL.md、TOOLS.md、IDENTITY.md、MEMORY.md
→ 生成 .md 格式能力包内容
→ 直接发送到聊天窗口（无需文件传输）

用户：导入能力包
→ 解析能力包内容，展示选项
→ 用户选择要导入的部分
→ 写入对应文件
```

## 安装

```bash
npx skills add ability-pkg
```
