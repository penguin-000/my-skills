---
name: zhin-skill-writing
description: "编写可复用的 SKILL.md，明确适用场景、输入输出、操作步骤与验证方法。"
metadata:
  display-name: "Skill 编写"
  category: development
  version: "1.0.0"
---

# Skill writing

Clarify the recurring task and when the skill should be invoked. Choose a lowercase kebab-case name. Create SKILL.md with YAML frontmatter containing name and a precise description, followed by concise task instructions. Include required inputs, steps, failure handling and verification. Put reusable scripts or references in separate files only when they are actually needed. Avoid embedding secrets or absolute machine paths. Check every referenced file exists and distinguish required tools from optional ones. Test with a realistic example and document any unresolved dependency.
