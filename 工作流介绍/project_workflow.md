# 项目级工作流规范 (Project-Level Workflow)

## 1. 快速开始 (Quick Start)

想要启动一个新项目？请按顺序执行以下指令：

| 步骤 | 阶段 | 你的指令 (Trigger) | 产出文档 (在 `.ai-specs/steering/`) |
| :--- | :--- | :--- | :--- |
| **01** | **需求挖掘** | `project-requirements-clarification` | (对话中澄清需求) |
| **02** | **项目定义** | `project-product-overview` | `1_产品概述.md` |
| **03** | **技术选型** | `project-tech-stack` | `2_技术栈.md` |
| **04** | **架构设计** | `project-structure` | `3_项目结构.md` |
| **05** | **规范制定** | `project-dev-standards` | `4_开发规范.md` |
| **06** | **初始化计划** | `project-task-planning` | `5_初始化计划.md` |
| **07** | **路线规划** | `project-roadmap-planning` | `6_开发路线图.md` |

> **提示**: 完成上述所有步骤后，你将获得一个完整的项目蓝图。接下来请执行 `5_初始化计划.md` 中的任务，然后按照 `6_开发路线图.md` 开始功能开发。

---

## 2. 详细流程详解

### 阶段零：存量接入 (Legacy Onboarding)
*   **目标**: 快速让老项目适配 AI 工作流。
*   **如何触发**: 呼叫 `project-context-initialization`
*   **交互**: AI 扫描现有代码库，自动反向生成 `1_产品概述`, `2_技术栈`, `3_项目结构` 等文档。
*   **产出**: `.ai-specs/steering/` 下的全套文档。

### 阶段一：需求挖掘 (Requirements Elicitation)
*   **目标**: 把模糊的想法变成清晰的文字。
*   **如何触发**: 呼叫 `project-requirements-clarification`
*   **交互**: AI 会扮演产品经理，通过苏格拉底式提问，帮你梳理核心价值、用户群体和关键特性。
*   **产出**: 标准化的项目描述段落（用于下一步）。

### 阶段二：项目定义 (Project Definition)
*   **目标**: 确立项目的“宪法”。
*   **如何触发**: 呼叫 `project-product-overview`
*   **交互**: AI 将基于上一阶段的描述，生成正式的产品概述文档。
*   **产出**: `1_产品概述.md`

### 阶段三：技术选型与架构 (Tech Stack & Architecture)
*   **目标**: 打好地基。
*   **如何触发**:
    1.  呼叫 `project-tech-stack` -> 生成技术选型。
    2.  呼叫 `project-structure` -> 生成目录结构。
*   **产出**: `2_技术栈.md`, `3_项目结构.md`

### 阶段四：规范制定 (Standardization)
*   **目标**: 统一"语言"和代码风格。
*   **如何触发**: 呼叫 `project-dev-standards` -> 生成代码规范 (`4_开发规范.md`)。
*   **产出**: `4_开发规范.md`

### 阶段五：初始化规划 (Initialization Planning)
*   **目标**: 万事开头难？让 AI 帮你列清单。
*   **如何触发**: 呼叫 `project-task-planning`
*   **交互**: AI 会整合上述所有文档，列出“搭建脚手架”的具体步骤（Git init, npm install, 配置 Lint 等）。
*   **产出**: `5_初始化计划.md`

### 阶段六：开发路线规划 (Roadmap Planning)
*   **目标**: 解决“先做什么后做什么”的迷茫。
*   **如何触发**: 呼叫 `project-roadmap-planning`
*   **交互**: AI 会分析模块依赖，规划 MVP 和后续里程碑，告诉你功能的开发顺序。
*   **产出**: `6_开发路线图.md`

### 阶段七：复盘与进化 (Review & Evolution)
*   **目标**: 不在同一个坑里跌倒两次。
*   **如何触发**: 呼叫 `project-ai-mistakes`
*   **交互**: 在项目过程中，随时记录或查询 AI 犯过的错误。
*   **产出**: `7_AI错题本.md`

---

## 3. 文档管理
所有全局文档均存储于 `.ai-specs/steering/` 目录下。这些文档是 AI 理解项目的**唯一事实来源 (Single Source of Truth)**。
