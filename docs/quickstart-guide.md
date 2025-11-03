# Quick Start Guide - 15 Minutes to AI-Assisted Onboarding

Get started with AI tools for your developer onboarding in 15 minutes.

## Prerequisites

- [ ] Development environment set up (IDE, git, etc.)
- [ ] Access to your team's codebase
- [ ] One AI tool installed (Claude Code, Cursor, or Cline)

## Step 1: Choose Your AI Tool (2 min)

**Already have Claude Code?** → Use Claude Code configs
**Using Cursor Editor?** → Use Cursor configs
**Using VSCode with Cline?** → Use Cline configs
**Not sure?** → See [ai-tools-comparison.md](ai-tools-comparison.md)

## Step 2: Copy Your First Config (3 min)

### For Claude Code:

```bash
# Clone this repository
cd ~
git clone https://github.com/yourusername/open-onboarding.git

# Copy first-week config
cd open-onboarding
cp claude/onboarding/first_week_developer.md ~/.claude/CLAUDE.md
```

### For Cursor:

```bash
# From your project directory
cp /path/to/open-onboarding/cursor/.cursorrules/onboarding_buddy.rules .cursorrules
```

### For Cline (VSCode):

```bash
# From your project directory
cp /path/to/open-onboarding/cline/.clinerules/default_cline.md .clinerules
```

## Step 3: Understand How It Works (5 min)

**For Claude Code users** - READ THIS:
- [claude/CONFIGURATION_GUIDE.md](../claude/CONFIGURATION_GUIDE.md)
- Explains how CLAUDE.md works
- Shows you how to avoid common mistakes
- **Essential reading** - 5 minutes that save hours

**For Cursor users**:
- .cursorrules files configure Cursor's AI behavior
- The onboarding_buddy.rules file teaches while you code

**For Cline users**:
- .clinerules files help maintain context across sessions
- Useful for tracking your onboarding progress

## Step 4: Test It Out (5 min)

Try these commands to verify it's working:

### Claude Code:
```bash
# Start Claude Code in your project
cd your-project
claude

# Ask: "Explain the architecture of this codebase"
# Ask: "Where should I start exploring?"
# Ask: "What patterns should I know about?"
```

### Cursor:
- Open a file
- Use Cmd+K (Mac) or Ctrl+K (Windows) to chat
- Ask: "Explain what this component does"
- Notice the teaching-style responses

### Cline:
- Open VSCode
- Use the Cline extension
- Ask about the codebase
- Your context will be maintained across sessions

## What's Next?

### This Week:
- [ ] Read [onboarding-checklist.md](onboarding-checklist.md) for your first week tasks
- [ ] Read [first-week-guide.md](first-week-guide.md) for detailed guidance
- [ ] Explore the codebase with AI assistance
- [ ] Ask lots of questions!

### Week 2-4:
- [ ] Try the pair programming config (if using Claude/Cursor)
- [ ] Make your first contributions
- [ ] Learn team workflows

### Month 2+:
- [ ] Transition to standard team configs
- [ ] Share feedback on what helped
- [ ] Help onboard the next new hire!

## Troubleshooting

**Config isn't working?**
- Claude Code: Check file is at `~/.claude/CLAUDE.md` or `.claude/CLAUDE.md`
- Cursor: Check file is named `.cursorrules` in project root
- Cline: Check file is named `.clinerules` in project root

**AI responses seem generic?**
- Ensure you copied the onboarding config correctly
- Restart your AI tool
- Check for other configs that might conflict

**Have questions?**
- Read [claude/CONFIGURATION_GUIDE.md](../claude/CONFIGURATION_GUIDE.md)
- Check [docs/glossary.md](glossary.md)
- Ask your mentor
- Open an issue in this repository

## Success!

You're now set up with AI-assisted onboarding. Your AI tool is configured to:
- Provide detailed explanations
- Teach best practices
- Help you explore safely
- Guide your learning

Happy onboarding! 🚀
