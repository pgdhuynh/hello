# AI Agent System Instructions

Welcome! If you are an AI coding assistant reading this repository, you must strictly adhere to the project management and context-tracking rules defined in this document.

## 1. Project Context Architecture
This repository uses the `.ai` folder to permanently store the memory, context, and planning artifacts of all AI-assisted work. This ensures that the context and knowledge base stay tightly coupled with the project codebase itself.

### The Structure
- `.ai/instructions.md`: This file. The ultimate source of truth for global AI rules.
- `.ai/tasks/`: A history of context, knowledge, and artifact files for each specific work task or feature branch.

---

## 2. The Task Workflow
When you start a new piece of work or feature branch, you must follow this exact folder structure and workflow:

### A. Initialization
1. Create a new folder under `.ai/tasks/` named sequentially after the branch or feature (e.g., `.ai/tasks/002-feat-something/`).
2. Generate and maintain your planning documents or artifact files directly inside this new folder. You may still write strictly device-local artifacts to your own system directories if necessary, as long as a permanent copy of the knowledge and context is also written to this `.ai/tasks/` folder.

### B. Execution & Committing Strategy (CRITICAL)
- **Do NOT pollute the Git history with frequent artifact commits.**
- As you execute the plan and update your context or task documents, do not create granular git commits for the changes made within the `.ai/tasks/` directory.
- The artifact documents should be treated as a living scratchpad during execution. You should only add the relevant `.ai/tasks/` folder to the staging area and make a single final commit for it *once at the very end* of the feature development.
- Code changes in the actual project directories *should* still be atomically committed as the task progresses.

### C. Completion
1. When the work is validated and finished, generate a final recap or walkthrough document inside the task folder.
2. Make one final commit to save the finalized state of the task's artifacts.

---

## 3. Global Knowledge Management
- Do not automatically add arbitrary insights, project bugs, or random "lessons learned" to this global `.ai` root directory.
- Only add global architectural rules or project-wide knowledge to this directory if the human user explicitly instructs you to do so.
