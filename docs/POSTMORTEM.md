# Postmortem - Hypothetical Problem Analysis

## Situation: Data Calculation Inconsistency in Statistics Module

### Problem Overview
- **What happened**: Users reported inconsistent average calculations when datasets contained missing/NaN values
- **When discovered**: During Sprint 1 testing, Issue #2 was created to track this bug
- **Impact**: Statistical results became unreliable, potentially affecting downstream analysis
- **Severity**: High - core functionality compromised
- **Root cause hypothesis**: Missing value handling not implemented in mean() function

### Timeline
- **Day 1-2**: Repository setup and initial issue creation
- **Day 3-4**: Label and milestone establishment
- **Day 5-6**: Example issue creation including Issue #2: "데이터 누락으로 인한 평균 계산 오류"
- **Day 7**: First sign of issue when users began testing statistical functions
- **Day 8**: Bug report filed and labeled as `bug` + assigned to `Sprint 1`
- **Day 9-10**: Investigation and fix implementation
- **Day 11-12**: Testing and verification
- **Day 13-14**: Documentation of fix and retrospective

### Why (Root Cause Analysis - 5 Whys)

**Why 1**: Why did the average calculation produce wrong results?
- Because the mean() function didn't handle missing values (NaN/None)

**Why 2**: Why weren't missing values handled?
- The statistics module was designed for complete datasets only; edge case not considered

**Why 3**: Why was this edge case overlooked?
- Initial requirements focused on typical use cases; missing data scenario not in scope

**Why 4**: Why weren't edge cases included in requirements?
- Time pressure for MVP launch led to simplified initial scope

**Why 5**: Why was there time pressure?
- Project needed demonstration-ready structure within tight deadline

### What (Impact Assessment)

**Direct consequences**:
- Issue #2 created and assigned to Sprint 1
- User trust affected by unreliable calculations
- Additional time required for fix implementation

**Secondary effects**:
- Other statistical functions may have similar gaps
- Testing coverage needed expansion
- Documentation updated to include data quality warnings

**Opportunity cost**:
- Feature development delayed while bug fixed
- Other enhancement issues (histogram, user guide) slowed

### How (Resolution Path)

**Immediate fix**:
1. Update mean() function to detect and handle NaN/None values
2. Option: Skip missing values in calculation
3. Option: Return None when too many values missing
4. Option: Add parameter to control missing value behavior (skip, raise, ignore)

**Testing requirements**:
- Create test cases with complete datasets
- Test with single missing value
- Test with multiple missing values
- Test with all missing values
- Test edge cases (empty list, None inputs)

**Documentation updates**:
- Update README with data quality notes
- Add examples showing missing value handling
- Clarify function signatures and parameters
- Include warnings about dataset completeness

**Prevention for future**:
- Include edge case testing in definition of done
- Add requirements for data validation
- Create checklist for missing value handling
- Establish code review requirements for statistical functions

### What Went Well
- Issue tracking system caught problem early (Issue #2 created promptly)
- Label/milestone system enabled proper sprint prioritization
- Git workflow allowed quick iteration and rollback if needed
- Documentation already in place facilitated fix communication
- GitHub CLI streamlined all management tasks

### What Could Be Improved
- Earlier inclusion of edge case testing in requirements
- More comprehensive initial requirements gathering
- Automated test coverage for statistical functions from start
- Better communication about data quality expectations

### Action Items (for future sprints)
1. **Sprint 2**: Implement missing value handling in statistics module
   - Due: 2026-11-26
   - Assigned to: Issue #4 (technical통계량 계산 모듈 완성) or new sub-task

2. **Add automated tests**: Create test suite for statistical edge cases
   - Priority: High
   - Success criteria: 100% test coverage for mean() function

3. **Update requirements**: Include data validation as mandatory criteria
   - Apply to all future statistical function development

4. **Code review checklist**: Add missing value handling verification
   - Required for all PRs touching statistics module

5. **User documentation**: Write clear guidance on data quality expectations
   - Include in README and usage guide (Issue #5)

### Key Takeaways
- **Never assume complete datasets**: Always design for real-world data quality issues
- **Track everything**: Issue tracking system proved valuable for problem identification and resolution
- **Document as you go**: Existing TIL/retrospective documentation accelerated fix process
- **Iterate rigorously**: Testing multiple scenarios prevented regression
- **Balance speed and quality**: Tight deadlines require careful scope management, not skipping quality safeguards

### Conclusion
The data calculation bug served as valuable learning about statistical module design. While it delayed some feature work, the resulting improvements to data handling, testing practices, and documentation will pay dividends in future development. The STAR and Why-What-How frameworks provided structured analysis that transformed a problem into a process improvement opportunity.

**Next review**: Sprint 2 retrospective (2026-11-27) to assess missing value implementation and testing completeness.