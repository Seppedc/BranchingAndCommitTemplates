# Git Commit Message

To maintain a clean and readable commit history, we follow the [**Conventional Commits**](https://www.conventionalcommits.org/en/v1.0.0/) specification. This standard helps define a consistent commit message format, making it easier to understand the history, automate versioning, and generate changelogs.

## Conventional Commits Overview

A **Conventional Commit** message is structured to clearly identify the nature of the change and the part of the codebase it affects. This convention helps automate release management, as tools like [`semantic-release`](https://medium.com/agoda-engineering/automating-versioning-and-releases-using-semantic-release-6ed355ede742) can generate changelogs and manage versioning based on commit messages.

The general structure of a commit message is:

**`<type>(<scope>):<description>`**

---

## Git Commit Types

| **Commit Type** | **Naming Convention**       | **Purpose**                                                                                       | **Example**                                       |
| --------------- | --------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| **Feature**     | `feat(<scope>): <desc>`     | For new features or enhancements.                                                                 | `feat(dice): add dice grid api`                   |
| **Bugfix**      | `fix(<scope>): <desc>`      | For bug fixes or resolving issues.                                                                | `fix(dice): grid generation not being consistent` |
| **Chore**       | `chore(<scope>): <desc>`    | For routine tasks like updating dependencies or build adjustments.                                | `chore(tests): update test dependencies`          |
| **Docs**        | `docs(<scope>): <desc>`     | For documentation changes or updates.                                                             | `docs: add dice core internal documentation`      |
| **Style**       | `style(<scope>): <desc>`    | For code formatting, linting, or styling changes (no functionality change).                       | `style: resolve prettier styling errors`          |
| **Refactor**    | `refactor(<scope>): <desc>` | For code changes that neither fix a bug nor add a feature, but improve code quality or structure. | `refactor(persistence): make entities standalone` |
| **Test**        | `test(<scope>): <desc>`     | For adding or updating tests.                                                                     | `test(login): add unit tests for password reset`  |
| **Performance** | `perf(<scope>): <desc>`     | For improving performance (e.g., speed, memory, etc.).                                            | `perf(persistence): optimize query performance`   |
| **Build**       | `build(<scope>): <desc>`    | For changes related to the build system or external dependencies.                                 | `build(deps): update dotnet to v8`                |
| **CI**          | `ci(<scope>): <desc>`       | For changes to Continuous Integration (CI) configurations.                                        | `ci(github-actions): add linting step`            |
| **Revert**      | `revert: <desc>`            | To revert a previous commit.                                                                      | `revert: undo "feat(dice): add dice grid api"`    |

---

## Commit Message Structure

### **1. Commit Type**

Defines the purpose of the commit.

- **`feat`**: New feature or enhancement.
- **`fix`**: Bug fix.
- **`chore`**: Routine tasks or maintenance.
- **`docs`**: Documentation changes.
- **`style`**: Code formatting changes (e.g., whitespace, indentation).
- **`refactor`**: Code changes that improve structure or quality but do not alter functionality.
- **`test`**: Adding or modifying tests.
- **`perf`**: Performance improvements.
- **`build`**: Changes related to build tools or dependencies.
- **`ci`**: Changes related to Continuous Integration pipelines.
- **`revert`**: Reverting a previous commit.

### **2. Scope** _(Optional)_

The **scope** is the area of the code affected by the change, typically indicating the module or feature. This part is optional but can provide clarity.  
Examples: `auth`, `ui`, `login`, `api`.

### **3. Description**

A brief summary of what the commit does. The description should be in the present tense (e.g., "Add user authentication" instead of "Added user authentication"). Keep the description concise (around 50-72 characters).

---

## Commit Message Example

In the example above:

- **Type**: `feat` (New feature)
- **Scope**: `auth` (Authentication module)
- **Description**: `add JWT token authentication` (Brief and clear description)
- **Body** (optional): Explanation of the change and its impact.
- **Footer** (optional): Marks a breaking change with `BREAKING CHANGE:`.

---

## Commit Message Guidelines

- **Imperative Mood**: Use the imperative mood in the commit message description. For example:

  - "Fix typo in header" instead of "Fixed typo in header".
  - "Add user authentication" instead of "Added user authentication".

- **Short and Descriptive**: Keep the commit message short and to the point, ideally within 50-72 characters for the description. If necessary, use the body section for further details.

- **Consistency**: Use the same format and style across all commit messages to ensure clarity and consistency across the project.

---

## Additional Notes

- **Breaking Changes**: If a commit introduces a breaking change (e.g., a change that breaks backward compatibility), add the following in the **footer**:
  This helps to version tools like `semantic-release` recognize the change and automatically increment the version number.

- **Issue References**: If a commit fixes or relates to a specific issue, reference the issue in the **footer**:

---