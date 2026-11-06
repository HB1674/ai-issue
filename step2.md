# Step 2: Command Log - Python Statistics Project Setup

## Repository & Issue Creation Commands

### 1. New Repository Creation
```bash
gh repo create ai-issue --public --description="AI Issue Tracking Repository"
```

### 2. Initial Issue Creation ('배포됨')
```bash
gh issue create --title "배포됨" --body "This is a test issue created by AI." --repo HB1674/ai-issue
```

### 3. Git Initialization & First Commit
```bash
git init
git add step1.md
git commit -m "Add step1.md - Repository and issue creation summary"
```

### 4. Git Remote & Push
```bash
git remote add origin https://github.com/HB1674/ai-issue.git
git branch -M main
git push -u origin main
```

## Project Setup Commands

### 5. README.md Creation
- Used write tool to create `README.md` with Python statistics project description
- Then git add/commit/push

### 6. Label Creation (7 labels)
```bash
# bug label (already existed, forced update)
gh label create bug --color "d73a4a" --description "Something isn't working" --repo HB1674/ai-issue --force

# enhancement label
gh label create enhancement --color "8e7ca4" --description "New feature request" --repo HB1674/ai-issue --force

# question label
gh label create question --color "c4e8e8" --description "Clarification needed" --repo HB1674/ai-issue --force

# statistics label
gh label create statistics --color "f6e05e" --description "Statistical analysis related" --repo HB1674/ai-issue --force

# data-analysis label
gh label create data-analysis --color "2a7f97" --description "Data analysis and processing" --repo HB1674/ai-issue --force

# visualization label
gh label create visualization --color "2b7a2b" --description "Chart and graph visualization" --repo HB1674/ai-issue --force

# documentation label
gh label create documentation --color "6e9fdf" --description "Documentation improvements" --repo HB1674/ai-issue --force
```

### 7. Milestone Creation (2-week sprints)
```bash
# Sprint 1 (due 2026-11-19)
gh api repos/HB1674/ai-issue/milestones -f title="Sprint 1" -f description="First 2-week sprint for Python statistics project" -f due_on="2026-11-20T00:00:00Z"

# Sprint 2 (due 2026-11-26)
gh api repos/HB1674/ai-issue/milestones -f title="Sprint 2" -f description="Second 2-week sprint for Python statistics project" -f due_on="2026-11-27T00:00:00Z"
```

### 8. Example Issue Creation (4 issues)

#### Issue #2: 데이터 누락 평균 계산 오류
```bash
gh issue create --title "데이터 누락으로 인한 평균 계산 오류" \
  --body "데이터 셋에서 누락된 값으로 인해 평균 계산이 잘못됩니다. 수치 통계 함수의 바그를 수정해주세요." \
  --label bug --milestone "Sprint 1" --repo HB1674/ai-issue
```

#### Issue #3: 데이터 시각화를 위한 히스토그램 기능 추가
```bash
gh issue create --title "데이터 시각화를 위한 히스토그램 기능 추가" \
  --body "데이터 분포를 시각화하기 위한 히스토그램 기능을 추가해주세요. matplotlib 또는 seaborn 통합을 고려합니다." \
  --label enhancement --label visualization --milestone "Sprint 2" --repo HB1674/ai-issue
```

#### Issue #4: 기술통계량 계산 모듈 완성
```bash
gh issue create --title "기술통계량 계산 모듈 완성" \
  --body "평균, 중앙값, 표준편차, 분산 등 기본 기술통계량 계산 기능을 완성해주세요. 결측치 처리 옵션을 추가해주세요." \
  --label enhancement --label statistics --milestone "Sprint 1" --repo HB1674/ai-issue
```

#### Issue #5: 통계 분석 사용 가이드 문서화
```bash
gh issue create --title "통계 분석 사용 가이드 문서화" \
  --body "Python 통계 분석 라이브러리 사용 방법을 설명하는 사용 가이드 문서를 작성해주세요. 설치 방법부터 기본 사용 예시까지 포함해주세요." \
  --label documentation --milestone "Sprint 2" --repo HB1674/ai-issue
```

## Git Operations Summary

### File Management Commands
```bash
# Check status
git status

# Add files
git add step1.md
git add README.md
git add -A  # Add all modified files

# Commit changes
git commit -m "Commit message describing changes"

# Push to remote
git push -u origin main
```

## Files Created/Modified

| File | Description |
|------|-------------|
| `step1.md` | Step 1 summary: Repository and issue creation process |
| `step2.md` | Step 2 summary: Command log for Python statistics project setup |
| `README.md` | Project description: Python statistics project overview |
| Issue #1 | "배포됨" - Initial deployment confirmation issue |
| Issues #2-5 | Example issues for Python statistics project |
| Labels | 7 category labels for issue tracking |
| Milestones | Sprint 1 & Sprint 2 (2-week periods) |

## Workflow Flow

```
Repository Creation
    ↓
Initial Issue Creation
    ↓
Git Init & First Commit
    ↓
Remote Setup & Push
    ↓
README.md Addition
    ↓
Label Creation (7 labels)
    ↓
Milestone Creation (2 sprints)
    ↓
Example Issue Creation (4 issues)
    ↓
step1.md & step2.md Documentation
    ↓
Final Push to GitHub
```

## Reference URLs

- Repository: https://github.com/HB1674/ai-issue
- Issues: https://github.com/HB1674/ai-issue/issues
- Milestones: https://github.com/HB1674/ai-issue/milestones
- Labels: https://github.com/HB1674/ai-issue/labels