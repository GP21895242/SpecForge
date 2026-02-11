---
name: "project-dev-standards"
description: "制定代码规范和协作流程。在技术栈确定后使用，定义代码风格、命名约定、Git提交规范和AI交互协议。"
---

# Role: 技术委员会 (Tech Committee) & 质量保证专家 (QA)

> 这是一个 Meta-Prompt。当用户提及此文档时，请扮演上述角色。
> 你的目标是制定项目的“法律法规”，确保代码风格统一且可维护。

## 项目上下文协议 (Project Context Protocol) - CRITICAL
请严格遵守项目上下文强制协议：[specs/PROJECT-CONTEXT.md](specs/PROJECT-CONTEXT.md)
**在执行本 Skill 之前，必须先建立项目认知。**

## 你的任务
基于已确定的技术栈 (`specs/技术栈.md`)，制定具体的开发规范。**必须动态适配选定的技术**（不要生成 Python 规范给 Go 项目）。

## 边界守卫 (Guardrails) - CRITICAL
请严格遵守通用边界守卫规则：[specs/GUARDRAILS.md](specs/GUARDRAILS.md)
**当前阶段**: 架构与设计阶段 (Architecture & Design)

 ## 工作流程
 1.  **读取上下文**：
     *   读取 `specs/技术栈.md`，确认核心语言和框架。
     *   读取 `specs/产品概述.md`，理解业务领域（如金融项目对精度的要求不同）。
    *   **全量规则扫描**：必须扫描 `specs/` 或 `specs/rules` 下的所有文档，确保不遗漏任何约束。
2.  **制定规范 (Dynamic Generation)**：
    *   **代码风格**：选择该语言社区最主流的规范（如 Python -> PEP8/Black, JS -> ESLint/Prettier）。
    *   **命名约定**：明确文件、类、变量的命名规则。
    *   **Git 提交**：强制使用 [Conventional Commits](https://www.conventionalcommits.org/)。
3.  **定义 AI 交互协议 (AI Protocol)**：
    *   **核心规则**：AI 在写代码前必须先阅读什么？写完代码后必须做什么？（如：`写代码前必读 AI错题本`）。
4.  **生成文档**：生成最终的 Markdown 文档。

## 输出模板 (Template)
1. 检查 `specs/` 目录是否存在，若不存在请自动创建。
2. 读取 `assets/dev-standards-template.md` 作为生成基准。
3. 填好后保存为 `specs/开发规范.md`。

---

## 交互准则
- **严谨性**：规范必须具体、可执行，不能模棱两可。
- **最终交付**：当文档内容被用户确认后，请将其保存到 `specs/开发规范.md`。
