# AI 工作流维护指南 (AI Workflow Maintenance Guide)

> **⚠️ 重要复盘与约束 (Critical Constraints & Post-Mortem)**
>
> *以下规则是本仓库的核心维护准则，用于防止历史错误重演：*
>
> 1.  **路径铁律 (Path Discipline)**:
>     *   **现状**: 本仓库定义了 `specs/` 作为标准目录。
>     *   **禁止**: 严禁在任何文档或代码中引用 `.ai-specs/steering/`。这是旧版本的路径，必须彻底废弃。
>     *   **强制**: 所有生成的 Skills 必须指向 `specs/` 下的文档（如 `specs/GUARDRAILS.md`）。
>
> 2.  **UI 开发闭环 (UI Development Loop)**:
>     *   在定义 `feature-tech-design` Skill 时，必须强制其读取 `*.html` 原型。
>     *   严禁引用不存在的 `1.5_UI设计.md`。
>     *   **目的**: 确保工作流中的技术方案是基于视觉原型设计的。
>
> 3.  **链接有效性 (Link Validity)**:
>     *   在编写 `AGENT.md` 模板或 `SKILL.md` 时，引用的 Skill 路径必须真实存在。
>     *   例如：引用 `feature-requirements-clarification` 时，路径必须是 `.ai-specs/skills/feature-requirements-clarification/SKILL.md`。
>
> 4.  **目录结构完整性 (Structure Integrity)**:
>     *   工作流定义中必须包含 `specs/` 目录的创建逻辑。
>     *   严禁保留无用的空目录（如 `project-ui-style-guide`）。
>
> ---
>
> ## 你的职责 (Your Role)
>
> 你正在维护 **AI Workflow Definition** 仓库。这个仓库本身**就是**工作流的定义集合，而不是一个使用该工作流的软件项目。
>
> **核心指令**:
> 1.  **全局读取**: 接手工作时，请务必读取项目中的所有文件（特别是 `工作流介绍/` 和 `.ai-specs/skills/`），以建立完整的上下文模型。
> 2.  **一致性维护**: 确保 `工作流介绍` 中的文档描述与 `.ai-specs/skills/` 中的实际 Prompt 实现保持高度一致。
>
> ## 仓库结构 (Repository Structure)
>
> *   **`.ai-specs/skills/`**: 核心资产。包含了所有 AI 技能的定义文件 (`SKILL.md`)。这是工作流的“源代码”。
> *   **`工作流介绍/`**: 对应的人类阅读文档（如 `project_workflow.md`, `feature_workflow.md`）。这是工作流的“说明书”。
> *   **`specs/`**: 存放全局规则文件（如 `GUARDRAILS.md`）。
>
> ## 维护任务 (Maintenance Tasks)
>
> *   **修改规则**: 如果修改了 `GUARDRAILS.md`，必须同步更新所有 Skills 中的引用。
> *   **新增技能**: 如果新增了一个 Skill，必须在 `project-agent-docs` 的模板中添加对应导航，并在 `工作流介绍` 中更新流程图。
> *   **修复 Bug**: 遇到路径错误或逻辑漏洞时，请参考顶部的【重要复盘与约束】进行修复。
