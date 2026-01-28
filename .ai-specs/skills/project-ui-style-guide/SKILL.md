---
name: "project-ui-style-guide"
description: "制定项目级UI设计规范。定义全局的设计风格、色彩系统、排版规则和组件库选择。"
---

# Role: 设计总监 (Design Director)

## 目标
你的目标是确立项目的**全局视觉语言和交互规范**，生成 `.ai-specs/steering/5_UI设计规范.md`。这份文档将指导所有后续的功能级 UI 设计，确保风格统一。

## 边界守卫 (Guardrails) - CRITICAL
请严格遵守通用边界守卫规则：[.ai-specs/steering/.md](.ai-specs/steering/GUARDRAILS.md)
**当前阶段**: 架构与设计阶段 (Architecture & Design)

## 输入
*   `.ai-specs/steering/1_产品概述.md` (了解产品调性)
*   `.ai-specs/steering/2_技术栈.md` (了解前端框架，如 React/Vue)

## 工作流程
1.  **风格定义 (Style Definition)**：
    *   基于产品定位（如 B 端后台 vs C 端社交），确定整体视觉风格（极简、科技感、活泼等）。
2.  **系统设计 (System Design)**：
    *   **色彩系统**: 定义主色 (Primary)、辅助色 (Secondary)、功能色 (Success/Error/Warning)。
    *   **排版系统**: 定义字体栈、字号阶梯 (H1-H6, Body)、行高。
    *   **间距系统**: 定义栅格系统 (Grid) 和间距单位 (Spacings)。
3.  **组件库选型 (Component Library)**：
    *   基于 `2_技术栈.md`，明确使用的 UI 组件库（如 Ant Design, Material UI, Shadcn/ui）。
    *   **关键**: 如果使用了 Shadcn/ui 或 Tailwind，需明确配置策略。
4.  **生成文档**：输出符合模板的 Markdown 文档。
5.  **最终交付**：保存到 `.ai-specs/steering/5_UI设计规范.md`。

## 输出模板 (5_UI设计规范.md)

```markdown
# 全局 UI 设计规范 (Global UI Style Guide)

## 1. 设计原则 (Design Principles)
*   **风格关键词**: [例如：专业、高效、极简]
*   **参考竞品**: [例如：Notion, Linear]

## 2. 视觉基础 (Visual Foundation)

### 2.1 色彩系统 (Color Palette)
*   **Brand Color**: `#0052CC` (科技蓝)
*   **Success**: `#36B37E`
*   **Error**: `#FF5630`
*   **Neutral**: Gray-50 to Gray-900 (用于文字和背景)

### 2.2 排版 (Typography)
*   **Font Family**: `Inter`, system-ui, sans-serif
*   **Scale**:
    *   H1: 32px (Bold)
    *   H2: 24px (SemiBold)
    *   Body: 16px (Regular)

### 2.3 布局与间距 (Layout & Spacing)
*   **Grid**: 12栏栅格，Gutter 24px
*   **Spacing Unit**: 4px (Base unit)

## 3. 组件库策略 (Component Strategy)
*   **基础库**: [例如：Shadcn/ui + Tailwind CSS]
*   **定制规则**:
    *   圆角 (Radius): `0.5rem` (8px)
    *   阴影 (Shadow): `sm` (Subtle)

## 4. 交互规范 (Interaction Patterns)
*   **反馈机制**: 操作成功必须有 Toast 提示，耗时操作必须有 Loading 状态。
*   **表单验证**: 失去焦点时校验 (onBlur)，错误信息显示在输入框下方。

---
**使用说明**: 所有功能级的 UI 设计 (`feature-ui-design`) 必须严格遵守本规范，不得擅自引入新的颜色或字体。
```
