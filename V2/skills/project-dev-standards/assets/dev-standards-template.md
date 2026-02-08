# 开发规范

## 1. 代码风格 (Code Style)
*   **核心原则**：[例如：Explicit is better than implicit]
*   **格式化工具**：[例如：Prettier / Black / Gofmt]
*   **命名规范**：
    *   **文件**: [例如: snake_case / kebab-case]
    *   **类**: [例如: PascalCase]
    *   **变量/函数**: [例如: camelCase]

## 2. Git 提交规范 (Commit Convention)
我们遵循 **Conventional Commits** 规范：
*   格式：`<type>(<scope>): <subject>`
*   示例：`feat(auth): add login page`
*   **常用 Type**:
    *   `feat`: 新功能
    *   `fix`: 修补 bug
    *   `docs`: 文档修改
    *   `refactor`: 重构（即不是新增功能，也不是修改bug的代码变动）
    *   `chore`: 构建过程或辅助工具的变动

## 3. AI 交互协议 (AI Interaction Protocol)
*为了保证代码质量，AI 助手必须遵守以下协议：*
1.  **阅读优先**：在编写新代码前，必须先阅读相关文件的上下文，以及 `specs/` 下的所有全局规则文档。
2.  **错题本机制**：每次任务开始前，必须检查 `docs/99-开发记录/AI错题本.md`，避免重复错误。
3.  **原子化提交与验证**：
    *   **步骤**：编写代码 -> 运行测试/预览 -> **确认无误** -> 提交。
    *   **禁止**：禁止在未经用户验证（或测试失败）的情况下直接提交代码。
4.  **自我审查**：代码生成后，必须进行一次 Self-Review，检查是否符合上述代码风格。
