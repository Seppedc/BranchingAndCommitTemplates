# Git Branching

To maintain clear and organized [Git branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell), we follow the [**Git Flow**](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) branching model. This branching model is designed for managing larger projects, particularly those involving multiple stages of software release. Git Flow helps keep development organized by defining clear roles for each type of branch.

---

## Git Branch Types

| **Branch Type** | **Naming Convention**     | **Purpose**                                                             | **Example**                      |
| --------------- | ------------------------- | ----------------------------------------------------------------------- | -------------------------------- |
| **Feature**     | `feature/<scope>-<desc>`  | For new features or enhancements being developed.                       | `feat/gamehub-core`              |
| **Bugfix**      | `bugfix/<scope>-<desc>`   | For fixing bugs or resolving issues in development.                     | `bugfix/dice-weight-calculation` |
| **Hotfix**      | `hotfix/<scope>-<desc>`   | For urgent fixes to critical production issues.                         | `hotfix/dice-calculation`        |
| **Chore**       | `chore/<scope>-<desc>`    | For routine tasks like dependency updates or code cleanup.              | `chore/update-dependencies`      |
| **Docs**        | `docs/<scope>-<desc>`     | For changes to documentation files or code comments.                    | `docs/add-dice-core`             |
| **Style**       | `style/<scope>-<desc>`    | For code formatting, linting, or styling changes.                       | `style/fix-code-formatting`      |
| **Refactor**    | `refactor/<scope>-<desc>` | For restructuring or improving code without changing its functionality. | `refactor/dice-core`             |
| **Test**        | `test/<scope>-<desc>`     | For adding or modifying tests.                                          | `test/dice-grid-integration`     |
| **Release**     | `release/<version>`       | For preparing a new release version.                                    | `release/v1.2.0`                 |
| **Main**        | `main` (or `master`)      | The production-ready branch that contains stable, released code.        | `main`                           |

---

### **Branch Name Structure**

- **`<scope>`**: This represents the module or feature the branch is related to (e.g., `dice-core`, `gamehub`, `jobs`).
- **`<desc>`**: A brief description of the branch's purpose (e.g., `add-dice-generation`, `add-signalR-integration`, `update-internal-docs`).

### **Description of Table Columns**

- **Branch Type**: Describes the type of branch (e.g., `Feat`, `Bugfix`).
- **Naming Convention**: The format used to name branches of this type.
- **Purpose**: Explains when and why this type of branch should be created.
- **Example**: A concrete example of a branch name.

---