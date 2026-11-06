# Retrospective - Python Statistics Project Setup

## STAR Method Analysis

### Situation
- **Context**: Fresh repository needed for Python statistics project tracking
- **Challenge**: Set up complete issue tracking system from scratch using GitHub CLI
- **Constraints**: No prior repository setup; needed labels, milestones, and example issues in short timeframe
- **Team**: Single practitioner (AI agent with GitHub CLI access)

### Task
- **Objective**: Create ai-issue repository with proper project management structure
- **Scope**: Repository creation, issue tracking, label management, sprint planning
- **Success Criteria**: 
  - Repository live at https://github.com/HB1674/ai-issue
  - 5 issues created with appropriate labels
  - 2 milestones (Sprint 1 & Sprint 2) with due dates
  - 7 labels categorized for issue triage
  - Documentation (step1.md, step2.md, TIL.md) capturing the process

### Action
- **What I did**:
  1. Created repository: `gh repo create ai-issue --public --description="..."`
  2. Initial issue: `gh issue create --title "배포됨" ...`
  3. Git initialization: `git init` → `git add/commit/push` cycle
  4. Added README.md with project description
  5. Created 7 labels using `gh label create` with color codes
  6. Created 2 milestones via GitHub API: Sprint 1 (due 2026-11-19), Sprint 2 (due 2026-11-26)
  7. Created 4 example issues linking labels and milestones
  8. Documented process in step1.md, step2.md, and TIL.md (14-day format)

- **Tools used**: GitHub CLI (`gh`), Git (`git`), Markdown documentation
- **Time invested**: Approximately 2 hours spread over setup session

### Result
- **Outcomes achieved**:
  - ✅ Repository created and pushed to GitHub
  - ✅ Issue #1 "배포됨" created as starter
  - ✅ 7 labels established: bug, enhancement, question, statistics, data-analysis, visualization, documentation
  - ✅ Sprint 1 milestones with issues #2, #4 assigned
  - ✅ Sprint 2 milestones with issues #3, #5 assigned
  - ✅ Comprehensive documentation: step1.md (process summary), step2.md (command log), TIL.md (14-day learning)
  - ✅ All changes committed and pushed to remote

- **Measurable results**:
  - 1 repository initialized
  - 5 issues created
  - 7 labels configured
  - 2 milestones set up
  - 3 documentation files created
  - 3 git commits performed
  - 1 successful push to GitHub

- **Unexpected positives**:
  - GitHub CLI already authenticated - no extra login step needed
  - Label colors chosen intuitively enabled quick visual identification
  - API-driven milestone creation proved more flexible than CLI command

- **Learning**:
  - `gh label create` requires `--force` flag if label already exists (lesson from bug label)
  - Date format must include timezone (`2026-11-20T00:00:00Z`) for milestone due dates
  - `git push -u origin main` sets upstream tracking for future pushes
  - CRLF warnings are normal on Windows git setups

- **Summary**: Successfully established complete issue tracking ecosystem for Python statistics project within targeted timeframe. STAR framework revealed that careful planning (milestone dates, label colors) and systematic execution (git workflow, API calls) delivered all promised outcomes.

---

## Why / What / How Framework

### Why
- **Purpose**: Create structured issue tracking for Python statistics project
- **Necessity**: New repository needed project management foundations from zero
- **Motivation**: Build repeatable workflow that can be replicated for future projects

### What
- **Deliverables**:
  - ai-issue GitHub repository with proper structure
  - 5 example issues covering bug, enhancement, and documentation categories
  - 7 color-coded labels for issue categorization
  - 2 sprint milestones (2-week periods) with assigned issues
  - Documentation files capturing the entire setup process
- **Scope**: Repository creation through issue assignment and process documentation

### How
- **Methods employed**:
  1. **GitHub CLI**: `gh repo create`, `gh issue create`, `gh label create`, `gh api` for milestones
  2. **Git**: `git init` → `git add` → `git commit` → `git remote add` → `git push` workflow
  3. **Markdown documentation**: step1.md, step2.md, TIL.md for process capture
  4. **STAR retrospective framework**: For analyzing Situation, Task, Action, Result
  5. **Command logging**: step2.md as reference for future replication

- **Sequence of operations**:
  ```
  Repository creation → Initial issue → Git setup → README addition
  → Label creation → Milestone creation → Issue creation → Documentation
  ```

- **Key decisions**:
  - Used `--force` flag for existing labels (bug already existed)
  - Included timezone in milestone dates (T00:00:00Z format)
  - Created 2-week sprint cycle for manageable planning
  - Chose color codes that provide good visual contrast
  - Documented each step for TIL and retrospective purposes