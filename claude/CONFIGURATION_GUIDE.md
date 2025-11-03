# Claude Code Configuration for New Developers

**Essential reading for anyone new to Claude Code during onboarding.**

This guide explains how Claude Code configurations work and how to use them effectively during your onboarding. Understanding these concepts will help you avoid confusion and get the most out of AI assistance.

*Simplified and adapted for new developers from community research shared on r/ClaudeCode*

---

## Why This Matters for Onboarding

During your first weeks, you'll be learning:
- How your team's codebase works
- Development workflows and practices
- Where to find information
- How to make your first contributions

Claude Code can accelerate this learning, but **only if configured correctly**. Using the wrong configuration or overloading context can cause:
- Confusing or inconsistent AI responses
- Slow performance
- Ignored instructions
- Wasted time troubleshooting

**5 minutes reading this guide = Hours saved during onboarding.**

---

## The Five Configuration Mechanisms

Claude Code offers 5 different ways to customize its behavior. As a new developer, **you'll primarily use #1 (CLAUDE.md)** and occasionally #3 (Slash Commands).

### 1. CLAUDE.md - Your Primary Configuration ⭐

**What it is:** A markdown file that gets included in every conversation with Claude.

**Where it lives:**
- **Project-specific**: `your-project/.claude/CLAUDE.md` (only applies to that project)
- **Global**: `~/.claude/CLAUDE.md` (applies to ALL projects)

**How it works:**
Every time you send a message to Claude, the contents of CLAUDE.md are automatically included. Think of it like a set of instructions that Claude sees every time.

**For onboarding, use this to:**
- Set your learning mode (first week, pair programming, etc.)
- Tell Claude you're new to the codebase
- Request detailed explanations
- Establish safety guardrails (confirm before changes)

**Example - First Week Config:**
```markdown
# Onboarding Context

I am a new developer in my first week on this team. I'm learning the codebase and development practices.

Please:
- Provide detailed explanations of code and patterns
- Ask for confirmation before making changes
- Explain "why" not just "how"
- Help me discover relevant documentation
- Teach best practices as we go
```

**⚠️ Context Impact:** HIGHEST - Included in EVERY message

**Start here:** Use one of the onboarding configs from this repo:
```bash
cp claude/onboarding/first_week_developer.md ~/.claude/CLAUDE.md
```

---

### 2. Output Styles - Communication Mode (Optional)

**What it is:** Changes how Claude communicates for your entire session.

**Command:** `/output-style <style-name>`

**Examples:**
- `/output-style concise` - Shorter, more direct responses
- `/output-style verbose` - Detailed, explanatory responses
- `/output-style software-architect` - High-level design focus

**For onboarding:**
- You probably won't need this initially
- CLAUDE.md is better for consistent onboarding behavior
- Output Styles can conflict with your CLAUDE.md config

**When to use:**
- Temporarily need more/less detail
- Switching between learning mode and "just do it" mode

**⚠️ Context Impact:** MEDIUM - Lasts until you change it

**Gotcha:** Easy to forget which style is active! Can cause unexpected behavior.

**Our recommendation:** Skip this during your first few weeks. Stick to CLAUDE.md.

---

### 3. Slash Commands - One-Time Workflows ✅

**What it is:** Pre-written prompts you can trigger with `/command-name`.

**How it works:**
Your team might have created custom commands like:
- `/review @file.js` - Code review this file
- `/explain @component` - Explain how this component works
- `/test @function` - Write tests for this function

**For onboarding:**
Ask your mentor if your team has onboarding-specific slash commands!

**When to use:**
- Running repeatable workflows
- Your team has standardized commands
- One-off specialized tasks

**⚠️ Context Impact:** LOW - Only affects that one message

**Safe to experiment:** Yes! Slash commands don't persist, so they're safe to try.

---

### 4. Skills - Autonomous Tools (⚠️ Advanced)

**What it is:** Claude automatically invokes tools based on what you ask.

**For onboarding:**
**Skip this.** This is an advanced feature you don't need during onboarding.

**Why skip:**
- Security concerns (can run arbitrary code)
- Complexity you don't need yet
- Better alternatives (MCP) for production use

**When you're ready:** After a few months, if interested, read the official docs.

---

### 5. Sub-Agents - Delegated Tasks (Optional)

**What it is:** Claude delegates complex tasks to specialized "sub-agents" that work independently.

**Examples:**
- Exploring how authentication works across the codebase
- Analyzing test coverage patterns
- Researching how a feature is implemented

**For onboarding:**
You probably won't use this directly. Claude might invoke sub-agents automatically when you ask complex questions like:
- "How does authentication work in this codebase?"
- "Where are API endpoints defined?"

**What you need to know:**
- Sub-agents automatically get your CLAUDE.md config
- They work independently and report back
- You don't need to do anything special

**⚠️ Context Impact:** ISOLATED - Separate conversation

**Our recommendation:** Don't worry about this during onboarding. It happens automatically.

---

## Quick Reference: What to Use When

| Situation | Use This | Example |
|-----------|----------|---------|
| **General onboarding** | CLAUDE.md | Copy `first_week_developer.md` |
| **Pair programming session** | CLAUDE.md | Copy `pair_programming_mentor.md` |
| **Exploring codebase** | CLAUDE.md | Copy `codebase_explorer.md` |
| **Running team workflow** | Slash Command | `/review @file.js` |
| **Need more detail temporarily** | Output Style | `/output-style verbose` |
| **Complex research question** | (Automatic) Sub-Agent | Just ask the question |

---

## For New Developers: Start Simple

### Week 1-2: CLAUDE.md Only

**Do this:**
1. Choose ONE onboarding config from this repo
2. Copy it to `~/.claude/CLAUDE.md` or your project's `.claude/CLAUDE.md`
3. Use it for all your work
4. Don't add anything else yet

**Example:**
```bash
# First week onboarding
cp claude/onboarding/first_week_developer.md ~/.claude/CLAUDE.md
```

**Don't:**
- ❌ Combine multiple configs
- ❌ Use Output Styles yet
- ❌ Try to create custom configs
- ❌ Use Skills
- ❌ Manually invoke Sub-Agents

### Week 3-4: Experiment Carefully

Once comfortable with CLAUDE.md:
1. Ask your mentor about team slash commands
2. Try different onboarding configs (pair programming, codebase explorer)
3. Consider switching to team's standard config if ready

### Month 2+: Standard Workflow

Transition to your team's standard configuration:
```bash
cp claude/general/global_development.md ~/.claude/CLAUDE.md
```

Learn about Output Styles and slash commands your team uses.

---

## Avoiding Context Pollution

**Context pollution** = Too many instructions that confuse Claude or slow it down

### Warning Signs

If Claude is:
- Giving unexpected or inconsistent responses
- Saying "I don't understand" frequently
- Responding slowly
- Ignoring your CLAUDE.md instructions

You might have context pollution.

### Prevention for New Developers

**Do:**
- ✅ Use ONE config at a time
- ✅ Start with provided onboarding configs (don't write your own yet)
- ✅ Keep configs focused and concise
- ✅ Remove configs you're no longer using

**Don't:**
- ❌ Copy-paste large documentation into CLAUDE.md
- ❌ Combine multiple CLAUDE.md files
- ❌ Add excessive team-specific instructions
- ❌ Use Output Styles + large CLAUDE.md together

### If You Hit Problems

1. **Check which config is active**: `cat ~/.claude/CLAUDE.md` or `cat .claude/CLAUDE.md`
2. **Check for Output Style**: Did you set one and forget?
3. **Simplify**: Remove config temporarily and test
4. **Ask your mentor**: They've probably seen this before

---

## Practical Examples for Onboarding

### Example 1: Setting Up First Week

**Goal:** Safe exploration and learning

**Action:**
```bash
cd your-project
mkdir -p .claude
cp /path/to/open-onboarding/claude/onboarding/first_week_developer.md .claude/CLAUDE.md
```

**Result:** Claude will now provide detailed explanations and ask before making changes.

### Example 2: Pair Programming Session

**Goal:** Learning through mentored coding

**Action:**
```bash
# Before session
cp /path/to/open-onboarding/claude/onboarding/pair_programming_mentor.md .claude/CLAUDE.md

# After session (if working solo)
cp /path/to/open-onboarding/claude/onboarding/first_week_developer.md .claude/CLAUDE.md
```

**Result:** Claude adapts between mentoring mode and standard learning mode.

### Example 3: Using Team Slash Commands

**Goal:** Running code review like the team does

**Action:**
```bash
# Your mentor shows you
/review @src/components/Button.jsx

# Claude runs the team's code review workflow
```

**Result:** Consistent code review feedback using team standards.

### Example 4: Graduating to Standard Config

**Goal:** Full team member workflow

**Action:**
```bash
# After 1-2 months
cp /path/to/open-onboarding/claude/general/global_development.md ~/.claude/CLAUDE.md
```

**Result:** You're now using the same Claude config as the rest of your team.

---

## Security Note: Why We Don't Use Skills

**Skills can execute arbitrary code on your machine.** This is a security risk, especially during onboarding when you're still learning what's safe.

**For onboarding:**
- Don't create Skills
- Don't install Skills from unknown sources
- Don't modify existing Skills unless your mentor approves

**Safe alternative:** If your team needs automation, they should use **MCP (Model Context Protocol)** which has proper security controls.

---

## FAQ for New Developers

**Q: Can I use multiple CLAUDE.md files?**
A: No. Claude uses the closest one (project > global). Don't try to combine them.

**Q: Should I create my own config?**
A: Not during onboarding. Use the provided configs first. After a month or two, you can customize.

**Q: What if my team has their own config?**
A: Great! Use theirs. These onboarding configs are for teams without existing configs.

**Q: Can I see what my CLAUDE.md is?**
A: Yes! Run:
```bash
cat ~/.claude/CLAUDE.md  # Global
cat .claude/CLAUDE.md     # Project (from project root)
```

**Q: How do I remove a config?**
A: Just delete the file:
```bash
rm ~/.claude/CLAUDE.md  # Remove global
rm .claude/CLAUDE.md     # Remove project
```

**Q: CLAUDE.md isn't working. Why?**
A: Check:
- Is the file actually at `~/.claude/CLAUDE.md` or `.claude/CLAUDE.md`?
- Is it valid markdown?
- Did you restart Claude after adding it?
- Is another config overriding it (project vs global)?

**Q: Can I use emojis in CLAUDE.md?**
A: Yes, but keep it professional and minimal.

---

## Onboarding Progression

### Day 1-3: Setup
- [ ] Install Claude Code
- [ ] Copy first-week config to `~/.claude/CLAUDE.md`
- [ ] Test it with simple questions
- [ ] Read this guide

### Week 1: Learn with Safety
- [ ] Use `first_week_developer.md` config
- [ ] Explore codebase with Claude
- [ ] Ask lots of "why" questions
- [ ] Let Claude explain patterns

### Week 2-4: Build Confidence
- [ ] Try `pair_programming_mentor.md` for tasks
- [ ] Learn team slash commands
- [ ] Make first contributions
- [ ] Get comfortable with workflow

### Month 2+: Standard Workflow
- [ ] Switch to `global_development.md` or team config
- [ ] Learn Output Styles (if your team uses them)
- [ ] Explore advanced features
- [ ] Help onboard the next new hire!

---

## Next Steps

1. **Choose your starting config:**
   - New to the team: `onboarding/first_week_developer.md`
   - Learning with mentor: `onboarding/pair_programming_mentor.md`
   - Exploring codebase: `onboarding/codebase_explorer.md`

2. **Copy it to CLAUDE.md:**
   ```bash
   cp claude/onboarding/first_week_developer.md ~/.claude/CLAUDE.md
   ```

3. **Start working:**
   Ask Claude questions, explore code, learn!

4. **After 2-4 weeks:**
   Evaluate if you're ready for the standard config

5. **Share feedback:**
   What worked? What didn't? Help improve these configs!

---

## Further Reading

**Essential:**
- [Claude Code Official Docs](https://docs.claude.com/en/docs/claude-code)
- [onboarding/first_week_developer.md](onboarding/first_week_developer.md) - Start here!

**When Ready:**
- [Output Styles Documentation](https://docs.claude.com/en/docs/claude-code/output-styles)
- [Community Analysis Repository](https://github.com/AgiFlow/claude-code-prompt-analysis)
- [MCP Documentation](https://modelcontextprotocol.io/) - For later

**Onboarding Resources:**
- [../docs/quickstart-guide.md](../docs/quickstart-guide.md)
- [../docs/onboarding-checklist.md](../docs/onboarding-checklist.md)
- [../docs/first-week-guide.md](../docs/first-week-guide.md)

---

**Remember:** Start simple. CLAUDE.md only. One config. Learn as you go.

*Last updated: 2025-11-03*
*Adapted for developer onboarding from community research*
