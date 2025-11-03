# Claude Code for Developer Onboarding

This directory contains Claude Code configurations specifically designed for **onboarding new developers**. Whether you're in your first week on a team or mentoring a new hire, these configs help accelerate learning and establish good practices with AI assistance.

## 📁 Directory Structure

```
claude/
├── CONFIGURATION_GUIDE.md  # How Claude Code configs work (essential reading!)
├── onboarding/              # Configs specifically for new developers
│   ├── first_week_developer.md        # Week 1: Learning & exploration
│   ├── pair_programming_mentor.md     # Mentorship-focused sessions
│   └── codebase_explorer.md           # Safe codebase navigation
├── general/                            # Standard development configs
│   └── global_development.md          # Graduate to this after onboarding
└── specialized/                        # Advanced workflow configs
    ├── git_workflow_trunk_based.md    # Git best practices
    └── team_tpm_security.md           # Team integration
```

## 🎯 Onboarding Journey with Claude Code

### Week 1: Safe Exploration & Learning
**Config**: `onboarding/first_week_developer.md`

Your first week is about understanding the codebase, tooling, and team workflow. This config:
- Provides detailed explanations of code and patterns
- Emphasizes safe, read-only exploration initially
- Asks for confirmation before making changes
- Teaches best practices as you learn

**Use when:**
- Exploring unfamiliar code
- Learning project architecture
- Understanding patterns and conventions
- Making small, supervised changes

### Week 2-4: Mentored Development
**Config**: `onboarding/pair_programming_mentor.md`

As you take on tasks, this config acts as a mentoring partner:
- Teaching-style communication
- Step-by-step explanations
- Encourages questions and discussion
- Reinforces best practices

**Use when:**
- Pair programming with AI assistance
- Learning through code review
- Taking on starter tasks
- Building confidence

### Ongoing: Codebase Exploration
**Config**: `onboarding/codebase_explorer.md`

Throughout onboarding, use this config when:
- Navigating new parts of the codebase
- Understanding architecture decisions
- Discovering documentation
- Identifying patterns across the project

### Month 2+: Standard Workflow
**Config**: `general/global_development.md`

Once comfortable, graduate to the standard development config that your team uses. This provides:
- Peer-to-peer collaboration style
- Planning-first approach
- Full development velocity

## 📘 Understanding Claude Code Configuration

**⚠️ New to Claude Code?** **YOU MUST READ** [CONFIGURATION_GUIDE.md](CONFIGURATION_GUIDE.md) first!

This guide explains:
- **What is CLAUDE.md** and how it works
- **Different configuration mechanisms** (Output Styles, Slash Commands, Skills, Sub-Agents)
- **How to avoid context pollution** (critical for new developers)
- **When to use which configuration type**

**5 minutes reading this guide will save you hours of confusion.**

## 🚀 Quick Start for New Developers

### Day 1: Choose Your Starting Config

**Option A: General Learning (Recommended)**
```bash
# Copy first-week config to your global Claude settings
cp claude/onboarding/first_week_developer.md ~/.claude/CLAUDE.md
```

**Option B: Project-Specific**
```bash
# Copy to your project directory
cp claude/onboarding/first_week_developer.md myproject/.claude/CLAUDE.md
```

**Option C: Pair Programming with Mentor**
```bash
# Use mentor-focused config for pair sessions
cp claude/onboarding/pair_programming_mentor.md myproject/.claude/CLAUDE.md
```

### Week 2-4: Continue Learning

Keep using onboarding configs, potentially switching between:
- `first_week_developer.md` for general development
- `pair_programming_mentor.md` for learning sessions
- `codebase_explorer.md` for exploration

### Month 2+: Graduate to Standard Workflow

```bash
# Switch to standard development config
cp claude/general/global_development.md ~/.claude/CLAUDE.md

# Or use team-specific workflow
cp claude/specialized/git_workflow_trunk_based.md myproject/.claude/CLAUDE.md
```

## 📋 Available Configurations

### 🌱 Onboarding Configs (NEW!)

**`onboarding/first_week_developer.md`**
- **Target**: New developers in their first 1-2 weeks
- **Purpose**: Safe exploration with detailed explanations
- **Style**: Teaching-focused, beginner-friendly, guardrails included
- **Key features**:
  - Detailed code explanations
  - Pattern recognition guidance
  - Safe exploration emphasis
  - Gradual complexity increase
  - Confirmation before changes

**`onboarding/pair_programming_mentor.md`**
- **Target**: New developers learning with mentor/buddy
- **Purpose**: Mentorship-style AI assistance for learning
- **Style**: Teaching, encouraging questions, best practices reinforcement
- **Key features**:
  - Step-by-step explanations
  - Encourages asking questions
  - Code review training
  - Best practices emphasis
  - Learning path guidance

**`onboarding/codebase_explorer.md`**
- **Target**: Anyone exploring unfamiliar code
- **Purpose**: Safe, read-only codebase navigation
- **Style**: Architecture-focused, documentation discovery
- **Key features**:
  - Read-only emphasis
  - Architecture explanations
  - Pattern identification
  - Documentation discovery
  - Component relationship mapping

### 🔧 General Development

**`general/global_development.md`**
- **Target**: Developers comfortable with codebase and workflow
- **Purpose**: Standard collaborative development
- **Style**: Peer-to-peer, planning-first
- **Key features**:
  - Planning before implementation
  - Technical discussion
  - Test-driven development
  - Full development velocity

### 🎯 Specialized Workflows

**`specialized/git_workflow_trunk_based.md`**
- **Target**: Teams using trunk-based development
- **Purpose**: Git best practices and GitHub integration
- **Adapted for onboarding**: Includes guidance for learning git workflows
- **Key features**:
  - Trunk-based patterns
  - Standard development workflow
  - GitHub issues integration
  - Onboarding-friendly explanations

**`specialized/team_tpm_security.md`**
- **Target**: Teams with defined roles (TPM, DevOps, QA, Security)
- **Purpose**: Team integration and Scrum/Kanban practices
- **Adapted for onboarding**: Helps new devs understand team dynamics
- **Key features**:
  - Scrum + Kanban hybrid
  - Role-based collaboration
  - Security integration
  - Team ceremonies

## 🎓 Choosing the Right Config

### By Experience Level

| Experience | Recommended Config |
|---|---|
| First week on team | `onboarding/first_week_developer.md` |
| Week 2-4, learning | `onboarding/pair_programming_mentor.md` |
| Exploring codebase | `onboarding/codebase_explorer.md` |
| Month 2+, comfortable | `general/global_development.md` |
| Ready for team workflow | `specialized/git_workflow_trunk_based.md` |

### By Activity

| Activity | Recommended Config |
|---|---|
| Learning codebase architecture | `onboarding/codebase_explorer.md` |
| Pair programming session | `onboarding/pair_programming_mentor.md` |
| Making first changes | `onboarding/first_week_developer.md` |
| Standard development | `general/global_development.md` |
| Learning git workflow | `specialized/git_workflow_trunk_based.md` |

### By Learning Style

| Learning Style | Recommended Config |
|---|---|
| Learn by exploring | `onboarding/codebase_explorer.md` |
| Learn by doing with mentor | `onboarding/pair_programming_mentor.md` |
| Learn through gradual progression | `onboarding/first_week_developer.md` |
| Jump in and learn by fixing | `general/global_development.md` |

## 🔧 Customization for Your Team

### For New Developers

**Don't customize yet!** Use the configs as-is during your first few weeks. Once you understand your team's workflow, you can customize:

1. **Team member names**: Add your mentor's name to prompts
2. **Project-specific patterns**: Note common patterns in your codebase
3. **Team conventions**: Add coding standards specific to your team

### For Managers / Mentors

Customize configs for your team's onboarding:

1. **Copy the relevant onboarding config**:
   ```bash
   cp claude/onboarding/first_week_developer.md company-onboarding/claude/
   ```

2. **Add team-specific context**:
   - Your team's coding conventions
   - Common patterns in your codebase
   - Links to internal documentation
   - Names of go-to people for questions

3. **Distribute to new hires**:
   - Include in onboarding documentation
   - Share during setup day
   - Update as you learn what works

## ⚠️ Important: Context Management

### For New Developers

**Start Simple:**
- ✅ Use ONE config at a time
- ✅ Start with `first_week_developer.md`
- ✅ Don't combine multiple configs initially
- ✅ Read CONFIGURATION_GUIDE.md to understand how configs work

**Avoid Context Pollution:**
- ❌ Don't load multiple configs simultaneously
- ❌ Don't add large team docs to configs yet
- ❌ Don't copy-paste code into CLAUDE.md files
- ❌ Don't create overly complex custom configs

### Transitioning Between Configs

When ready to switch configs:

1. **Review your current config** - What helped? What didn't?
2. **Choose your next config** - Based on your learning stage
3. **Replace, don't combine** - Switch configs, don't stack them
4. **Test in a safe environment** - Try new config on a small task first

## 📖 Configuration File Format

Claude Code configurations are markdown files placed in:
- **Global** (all projects): `~/.claude/CLAUDE.md`
- **Project-specific**: `project-root/.claude/CLAUDE.md`

Project-specific configs override global configs.

## 💡 Tips for Onboarding Success

### Week 1
- **Use**: `first_week_developer.md` or `codebase_explorer.md`
- **Focus**: Understanding over doing
- **Ask**: Lots of questions (AI and human mentors!)
- **Goal**: Navigate codebase confidently

### Week 2-4
- **Use**: `pair_programming_mentor.md` for tasks
- **Focus**: Learning through implementation
- **Ask**: "Why" questions, not just "how"
- **Goal**: First successful code reviews and merges

### Month 2+
- **Use**: `global_development.md`
- **Focus**: Full velocity development
- **Ask**: Strategic and architectural questions
- **Goal**: Independent, productive team member

## 📚 Related Resources

**Essential Reading:**
- [CONFIGURATION_GUIDE.md](CONFIGURATION_GUIDE.md) - **READ THIS FIRST**
- [Main Repository README](../README.md) - Overview and quick start
- [Contributing Guidelines](../CONTRIBUTING.md) - Share your experience

**Onboarding Documentation:**
- [docs/quickstart-guide.md](../docs/quickstart-guide.md) - 15-minute setup
- [docs/onboarding-checklist.md](../docs/onboarding-checklist.md) - First week tasks
- [docs/first-week-guide.md](../docs/first-week-guide.md) - Week-by-week guide

**Official Claude Code:**
- [Claude Code Docs](https://docs.anthropic.com/claude/docs/claude-code)
- [Claude Code GitHub](https://github.com/anthropics/claude-code)

## 🤝 Feedback Welcome!

**New developers**: Your feedback is incredibly valuable!
- What worked well in these configs?
- What was confusing?
- What would you change?
- What's missing?

Open an issue with `onboarding-feedback` tag or contribute improvements via PR.

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

**License**: GPL-3.0 | See [LICENSE](../LICENSE) for details

**Built for onboarding** - Helping new developers become productive faster with AI assistance.
