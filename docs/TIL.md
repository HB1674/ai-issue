# TIL - Today I Learned (14 Days)

## Days 1-2: Repository & GitHub CLI Foundation
- **Why**: New project needed issue tracking setup from scratch
- **What**: Learned `gh repo create`, `gh issue create`, and Git initialization workflow
- **How**: Used `gh repo create ai-issue --public` for repo setup, `gh issue create` for issue generation, `git init` + `git commit` + `git push` for version control
- **Key takeaway**: GitHub CLI automates repo/issue creation; git workflow requires init → add → commit → push sequence

## Days 3-4: Project Structure & Documentation
- **Why**: Repository needed proper project description and structure
- **What**: Created README.md with Python statistics project overview, learned markdown formatting for technical docs
- **How**: Wrote project description, setup instructions, and usage guidelines in README.md
- **Key takeaway**: Clear README sets project tone; markdown is essential for GitHub documentation

## Days 5-6: Label Management
- **Why**: Issues need categorization for better triage and milestone tracking
- **What**: Created 7 labels (bug, enhancement, question, statistics, data-analysis, visualization, documentation) with specific colors
- **How**: Used `gh label create` commands with color codes and descriptions for each label
- **Key takeaway**: Consistent labeling system enables filter-based workflow and milestone assignment

## Days 7-8: Milestone Planning
- **Why**: Need structured sprint timelines for 2-week development cycles
- **What**: Created Sprint 1 (due 2026-11-19) and Sprint 2 (due 2026-11-26) milestones
- **How**: Used `gh api repos/:owner/:repo/milestones` with title, description, and due_date parameters
- **Key takeaway**: API-driven milestone creation allows precise date planning; 2-sprint structure provides clear short-term goals

## Days 9-10: Issue Creation & Assignment
- **Why**: Concrete tasks needed for sprint execution
- **What**: Created 4 example issues covering bug fixes, feature enhancements, and documentation
- **How**: Used `gh issue create` with titles, bodies, labels, and milestone assignments
  - Issue #2: bug + Sprint 1 (data calculation error)
  - Issue #3: enhancement+visualization + Sprint 2 (histogram feature)
  - Issue #4: enhancement+statistics + Sprint 1 (statistics module)
  - Issue #5: documentation + Sprint 2 (user guide)
- **Key takeaway**: Label + milestone combination enables progress tracking and prioritization

## Days 11-12: Git Workflow Integration
- **Why**: All changes need to be persisted and shared
- **What**: Mastered git add/commit/push cycle for repository maintenance
- **How**: `git add step1.md step2.md README.md`, `git commit -m "description"`, `git push -u origin main`
- **Key takeaway**: Consistent git workflow ensures local changes reflect on remote; CRLF warnings are normal on Windows

## Days 13-14: Documentation & Reflection
- **Why**: Process needs to be recorded for future reference and team onboarding
- **What**: Created step1.md (repository creation process) and step2.md (command log)
- **How**: Wrote comprehensive markdown files documenting each phase with commands and outcomes
- **Key takeaway**: Structured documentation (step1/step2.md) captures learning and serves as reference; TIL pattern builds individual knowledge base

---

## Summary of 14 Days
- **Core skills**: GitHub CLI automation, git version control, issue/label/milestone management
- **Project setup**: Complete workflow from repo creation to issue tracking
- **Documentation habit**: Daily TIL entries + structured step files
- **Result**: ai-issue repository fully set up with 5 issues, 7 labels, 2 milestones, and comprehensive process documentation