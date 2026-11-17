---
name: zhin-code-review
description: "围绕代码变更检查实际缺陷、资源释放和兼容性问题，并给出可定位的建议。"
metadata:
  display-name: "代码审查"
  category: development
  version: "1.0.0"
---

# Code review

Read repository instructions and inspect the diff before reviewing callers and tests. Prioritize reproducible behavior defects, data loss, authorization errors and lifecycle leaks. For each finding, state the trigger, impact, file and relevant lines. Verify assumptions against the actual implementation. Avoid speculative warnings and style-only complaints. Run focused checks when practical. Do not edit code unless asked. If no actionable defects are found, state that and summarize the remaining verification limits.
