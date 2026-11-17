# 我的技能仓库

保存自建 Skill，供 DSH 的 skill市场插件展示和安装。当前包含 6 个 MIT 入门示例和 ASCII 码翻译技能。

## 目录

- `catalog.json`：市场清单，包含名称、中文/英文介绍、分类和相对目录。
- `skills/<name>/SKILL.md`：技能的完整指令，可在同目录添加 `scripts/`、`references/` 等资源。

## 添加技能

1. 新建 `skills/my-skill/SKILL.md`，开头填写 YAML 配置中的 `name: my-skill` 和 `description`，正文填写操作指令。
2. 在 `catalog.json` 的 `skills` 数组增加一项，填写 `name`、`path: skills/my-skill`、`category`、`zh` 和 `en`（各含 `name`、`description`）。`letter` 和 `version` 可选。
3. 将技能文件和清单一起提交到 `main`。用户重新打开市场页面后即可看到。

名称使用小写字母、数字和单个连字符；目录名、清单 name 与 SKILL.md name 保持一致。分类可用 frontend、data、document、office、development，或自定义分类文字。清单 version 固定为 1。

新增条目的示例：

```json
{
  "name": "zhin-frontend-design",
  "path": "skills/zhin-frontend-design",
  "category": "frontend",
  "letter": "F",
  "version": "1.0.0",
  "zh": {
    "name": "前端界面设计",
    "description": "设计并实现网页、组件和管理界面，关注布局、视觉层级、响应式与可访问性。"
  },
  "en": {
    "name": "Frontend design",
    "description": "Plan and build responsive interfaces with clear hierarchy and accessible interactions."
  }
}
```

## 同步与安装

打开市场只同步清单，不会安装技能。点击安装后下载该清单对应的 Git 提交中的完整技能目录，保存到 DSH_HOME/skills。提交新版本不会自动覆盖用户已安装的版本。

技能是供模型遵循的指令，不附带模型或额外运行环境；需要的外部工具、依赖和权限应在技能说明中写明。
