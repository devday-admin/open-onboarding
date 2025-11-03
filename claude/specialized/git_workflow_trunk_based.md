# ---
# name: git_workflow_trunk_based.md
# tool: Claude Code
# purpose: Comprehensive git workflow guide for trunk-based development with standard development workflow and best practices
# source: inspired by community configs shared on r/ClaudeAI
# license: GPL-3.0
# ---

# Trunk-Based Development Workflow

## About This Document

This guide describes a complete trunk-based development workflow. It covers both current practices and planned approaches, providing a comprehensive view of the development system.

**Note**: This is a methodology document, not a status tracker. Do not add implementation status markers. For tracking what's built vs. planned, maintain separate project documentation.

## Core Branching Philosophy

### The Trunk Model

**Primary Branch**: `main` serves as the single source of truth and remains deployable at all times.

**Branch Lifetime**: Short-lived feature branches live less than 24 hours, or work directly on main.

**Integration Frequency**: Merge to main multiple times daily to maintain continuous integration.

### Simple Rules

1. Work directly on `main` for small, safe changes
2. Create short-lived branches only for risky or complex work
3. Merge to `main` at least daily
4. Keep `main` deployable always
5. Delete feature branches immediately after merging

### Workflow Options

**Option A: Direct Commits (small changes)**
```bash
git checkout main
git pull origin main
# Make changes
git add .
git commit -m "fix: description"
git push origin main
```

**Option B: Short Branch (complex changes)**
```bash
git checkout main
git pull origin main
git checkout -b feature/brief-name
# Work for a few hours
git add .
git commit -m "feat: description"
git push -u origin feature/brief-name
gh pr create --base main --title "feat: description"
# Merge immediately after approval
```

### Branch Naming Conventions

- **Features**: `feature/descriptive-name`
- **Fixes**: `fix/issue-description`
- **Keep names brief** - branches are temporary

### Main Branch Protection

- Allow direct pushes for trusted contributors
- Require status checks when CI/CD exists
- Prevent force pushes
- Prefer linear history
- Remove branches after merging

### When to Use Branches

Create a branch when:
- Changes might break existing functionality
- Refactoring multiple files
- Uncertain about approach
- Otherwise, commit directly to main

### Benefits

- **Simplicity**: One primary branch reduces complexity
- **Speed**: Deploy improvements immediately
- **Integration**: Avoid merge conflicts through frequency
- **Clarity**: Linear history shows progression
- **Modern**: Used by high-performing engineering organizations

## Technical Decision Framework

### Technical Debt vs Technical Leap

**Technical Debt**: Shortcuts requiring future cleanup
- Examples: Skipping tests, copying code, ignoring errors

**Technical Leap**: Innovations providing competitive advantage
- Examples: Offline search, real-time sync, progressive web apps

**Principle**: Choose leaps over debt when effort is comparable. Always ask: "Does this move us forward or create future problems?"

## Session Start Protocol

### Essential Checks

Before beginning work, run:

```bash
git branch --show-current
git status
git log --oneline -5
gh issue list --assignee @me --state open
```

### Validation Checklist

- [ ] Correct branch for work type
- [ ] Following appropriate architectural patterns
- [ ] Specifications exist for components
- [ ] No uncommitted work from previous session
- [ ] Active issues reviewed and understood
- [ ] Current work linked to issue (if applicable)

**Stop if any check fails** - Clarify before proceeding.

## Common Pitfalls

### Pitfall: Wrong Branch Continuation

**Problem**: Resuming work on unrelated branch from previous session
**Solution**: Always run session start protocol

### Pitfall: Missing Issue Tracking

**Problem**: Working without GitHub issues

**Prevention**:
- Search existing issues: `gh issue list --search "keyword"`
- Create issues before starting work
- Reference issues in commits: `#ISSUE_NUMBER`
- Use issue templates

**Why it matters**: Provides work history, enables collaboration, documents decisions, prevents duplication, creates audit trail.

### Pitfall: Inconsistent Patterns

**Problem**: Different components using different approaches
**Solution**: Find similar components and match their patterns

### Pitfall: File Versioning

**Problem**: Creating `script-v2.js`, `component-final.tsx`, etc.
**Solution**: Update existing files. Git provides versioning. Never use suffixes like `-complete`, `-final`, `-v2`, `-new`.

### Pitfall: Duplicate Files

**Problem**: Creating new files when similar ones exist
**Solution**: Search before creating: `ls`, `find`, or `grep`

### Pitfall: Poor Naming

**Problem**: Version numbers or marketing language in names

**Good practices**:
- NO version numbers in filenames
- NO marketing language
- NO phase references
- USE semantic, descriptive names
- USE feature flags for variations
- USE Git for versioning
- ORGANIZE by functionality

## Development Standards

### Code Quality

1. **Documentation**: Include module headers
2. **Type Safety**: Use type hints appropriately
3. **Logging**: Use structured logging with hierarchical names
4. **Error Handling**: Proper exceptions with informative messages including `exc_info=True`
5. **File Updates**: Always update existing files, never create versioned copies
6. **Code Reuse**: Check for existing implementations before creating new ones

### Logging Best Practices

**Use hierarchical naming**: `category.subcategory.specific`

**Log levels**:
- `DEBUG`: Verbose diagnostics
- `INFO`: Important events and status
- `WARNING`: Degraded states, retries
- `ERROR`: Failures requiring attention (always with `exc_info=True`)
- `CRITICAL`: System-wide failures

**Exception logging**:
```python
try:
    result = operation()
except Exception as e:
    logger.error(f"Operation failed: {e}", exc_info=True)
    raise
```

## Standard Development Workflow

### Principles

- Think critically about architecture
- Assess systems holistically
- Avoid getting lost in details

### No Mocks or Workarounds

**Never create temporary solutions when encountering problems.** If something doesn't work:
- Treat it as a real issue
- Follow proper workflow to address it
- Fix the actual problem

Only use temporary solutions if explicitly agreed upon beforehand.

### Workflow Steps

**1. Create Internal Plan**
- Analyze the problem
- Find relevant documentation
- Estimate complexity
- Review existing context

**2. Create or Find GitHub Issue**

Search first:
```bash
gh issue list --search "keyword in:title,body"
```

Create if needed:
```bash
gh issue create \
  --title "type: description" \
  --body "Details..." \
  --label "bug|enhancement" \
  --assignee @me
```

**3. Assess Task Thoroughly**
- Investigate root causes
- Check logs and errors
- Identify affected components
- Consider edge cases
- Document findings in issue

**4. Find Solution**
- Research best practices
- Consider multiple approaches
- Choose optimal solution
- Update issue with proposed approach

**5. Implement Solution**

Work on `main` or create short-lived branch (< 24 hours).

- Write maintainable code
- Follow existing patterns
- Document inline when needed
- Make atomic commits as you complete logical units
- Reference issues in commits: `git commit -m "fix: description (#123)"`
- Never include AI attribution in commits

**6. Update Documentation**
- Update relevant docs
- Add/update code comments
- Update significant patterns documentation
- Keep API documentation current

**7. Test Thoroughly**
- Test locally
- Check for regressions
- Verify edge cases
- Test related functionality
- Run type checking and linting
- Document test results in issue

**8. Fix if Necessary**
- Address issues found in testing
- Update tests
- Iterate until solid

**9. Prepare for Review**
- Self-review changes
- Ensure tests pass
- Verify documentation is updated
- Clean up debug code
- Follow style guide

**10. Push and Create PR (if using branch)**

If on branch:
```bash
git push -u origin feature/branch-name

gh pr create \
  --base main \
  --title "type: description" \
  --body "Fixes #ISSUE

## Changes
- Change 1

## Testing
- Test 1"
```

If on main:
```bash
git push origin main
```

**11. Verify and Close Issue**

After merging:
```bash
gh issue view ISSUE_NUMBER
gh issue close ISSUE_NUMBER --comment "Fixed and verified"
```

**12. Post-Verification**

After deployment:
```bash
# Run validation
./run_validation.py

# Monitor logs
tail -f logs/application.log
```

If verification fails:
```bash
gh issue reopen ISSUE_NUMBER --comment "Verification failed: [error]"
# Create hotfix if critical
```

## Additional Guidelines

- Review context documentation before starting
- Use `gh` CLI for all GitHub operations
- Create issues before starting work
- Link issues in commits and PRs
- Keep commits focused
- Over-communicate in issue comments
- Use appropriate labels
- Review open issues regularly

## Honest Assessment

When evaluating work:
- Reserve praise for genuinely exceptional work
- Provide realistic, supportive feedback
- Don't inflate the quality of routine contributions
