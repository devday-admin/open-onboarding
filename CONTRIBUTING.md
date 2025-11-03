# Contributing to Open Onboarding

Thank you for contributing to Open Onboarding! This repository helps companies onboard new developers using AI-powered tools. Your contributions help improve the onboarding experience for developers worldwide.

## 🎯 What We're Looking For

We especially welcome:

- **Onboarding-specific AI configs** for popular tools (Claude Code, Cursor, Windsurf, Devin, etc.)
- **First-week/first-month workflows** that help new developers learn faster
- **Mentorship and pair programming patterns** for using AI tools
- **Team onboarding playbooks** and standardization guides
- **New developer feedback** on what configs worked well during onboarding
- **Manager insights** on successful AI-assisted onboarding strategies
- **Documentation improvements** that help new developers understand AI tools

## ⚖️ Legal Requirements

Before contributing, ensure you meet these requirements:

### You Must Only Submit Configs That:

1. **You own** - Configs you personally created
2. **You have permission to share** - Configs where you have explicit authorization from your company/team
3. **Are publicly available** - Configs already shared publicly (with proper attribution)
4. **Contain no confidential information** - No proprietary onboarding docs, company-specific data, or trade secrets
5. **Contain no PII** - No personally identifiable information, team member names, or private details
6. **Are compatible with GPL-3.0** - Content that can be licensed under GPL-3.0

### You Must NOT Submit:

- ❌ Company-specific onboarding configs without authorization
- ❌ Configs marked as confidential or proprietary
- ❌ Configs containing API keys, credentials, or secrets
- ❌ Configs with restrictive licenses incompatible with GPL-3.0
- ❌ Personal information about team members or new hires
- ❌ Configs you found but don't have permission to share
- ❌ Internal company documentation or processes

## 📝 How to Contribute

### Step 1: Choose the Right Category

Determine which tool and category your config belongs to:

**Onboarding-Specific Categories:**
- `claude/onboarding/` - Onboarding configs for Claude Code
- `cursor/.cursorrules/` - Onboarding-focused Cursor rules
- `docs/` - Onboarding guides, checklists, and documentation
- `templates/` - Team customization templates

**General Categories:**
- `claude/general/` - Standard Claude Code configs
- `codex/general/` - Codex autonomous agent configs
- `cline/.clinerules/` - Cline memory bank configs
- Other tools as applicable

### Step 2: Add Metadata Header

Every config must include a metadata header:

```markdown
# ---
# name: your_config_name.md
# tool: Claude Code | Cursor | Windsurf | etc.
# purpose: Brief description focused on onboarding use case (1-2 sentences)
# source: inspired by onboarding experiences at [company type] | original work for this repo
# license: GPL-3.0
# ---
```

**Metadata Guidelines for Onboarding Configs:**

- **name**: Descriptive filename indicating onboarding stage (e.g., `first_week_developer.md`, `pair_programming_mentor.md`)
- **tool**: Which AI tool this config is for
- **purpose**: Clear description of onboarding use case (e.g., "Helps new developers explore codebase safely during first week")
- **source**:
  - `inspired by onboarding experiences` - Based on real onboarding practices
  - `inspired by onboarding at [startup/enterprise/team]` - General company type (never specific names)
  - `original work for this repo` - Completely original creation
- **license**: Always use `GPL-3.0`

**Important**: Generalize from specific experiences. If you learned something from onboarding at a specific company, create an original implementation that captures the pattern without revealing proprietary information.

### Step 3: Format Your Config

**For Onboarding Configs:**

- Use clear, beginner-friendly language
- Include explanatory comments for complex sections
- Add learning objectives or goals where appropriate
- Specify which onboarding stage this config targets (week 1, month 1, etc.)
- Include safety guardrails for new developers
- Test the config with actual new developers if possible
- Remove any company-specific paths, names, or references

**Example Onboarding Section:**

```markdown
## Onboarding Context

**Target Audience**: New developers in their first week
**Learning Focus**: Safe codebase exploration and understanding architecture
**Prerequisites**: Basic git knowledge, development environment setup complete
**Expected Outcome**: Ability to navigate codebase and understand major components

## Safety Guardrails

- Emphasize read-only exploration initially
- Request confirmation before making changes
- Encourage asking questions before implementing
- Provide detailed explanations of code patterns
```

### Step 4: Update Documentation

When adding a new config:

1. Add an entry to `index.yml` with onboarding-focused tags (see format below)
2. Update the tool-specific README (e.g., `claude/README.md`)
3. Update main `README.md` if adding a new onboarding category
4. Consider adding to `docs/` if it's a guide rather than a config

### Step 5: Submit a Pull Request

1. Fork the repository
2. Create a feature branch: `git checkout -b add-onboarding-config-name`
3. Add your config file with metadata header
4. Update `index.yml` and relevant READMEs
5. Commit with clear message: `git commit -m "Add: onboarding config for [use case]"`
6. Push and create a pull request
7. In PR description, explain the onboarding scenario and expected outcomes

## 📋 index.yml Format for Onboarding

Add an entry to `index.yml` for your config:

```yaml
- name: first_week_developer.md
  tool: Claude Code
  category: onboarding
  path: claude/onboarding/first_week_developer.md
  purpose: Simplified AI assistance for new developers during their first week, focusing on safe exploration and learning
  license: GPL-3.0
  tags:
    - onboarding
    - first-week
    - new-developer
    - learning
    - safe-exploration
    - mentoring
```

**Onboarding-Specific Tags:**
- **Stage**: `first-day`, `first-week`, `first-month`, `onboarding`
- **Role**: `new-developer`, `junior-developer`, `intern`, `mentor`, `manager`
- **Activity**: `pair-programming`, `code-review`, `codebase-exploration`, `learning`
- **Focus**: `mentoring`, `teaching`, `safe-exploration`, `gradual-learning`

## 🔍 Review Process

Your contribution will be reviewed for:

1. **Legal compliance** - Proper licensing, no confidential info, no PII
2. **Onboarding relevance** - Clear value for onboarding scenarios
3. **Quality** - Well-documented, beginner-friendly, tested
4. **Metadata** - Complete and accurate headers
5. **Formatting** - Follows repository conventions
6. **Safety** - Includes appropriate guardrails for new developers
7. **Generalizability** - Not too company-specific

We may ask for:
- Clarification on onboarding stage or use case
- Removal of company-specific details
- Additional explanatory comments
- Safety guardrails for new developers

## ⚠️ Protecting Company Information

When contributing configs based on your company's onboarding:

### Do:
- ✅ Generalize the patterns and approaches
- ✅ Create original implementations of concepts you learned
- ✅ Use generic examples and placeholder names
- ✅ Focus on the "what" and "why", not company specifics
- ✅ Note it's "inspired by onboarding experiences at a [startup/enterprise]"

### Don't:
- ❌ Copy internal onboarding documentation
- ❌ Include company-specific processes or proprietary methods
- ❌ Name your company or team members
- ❌ Reveal competitive advantages or trade secrets
- ❌ Share internal tooling or infrastructure details

### Example Transformation:

❌ **Bad (Too Specific)**:
```markdown
## Acme Corp Onboarding Process
1. Clone the acme-platform repo from github.com/acme/platform
2. Install our proprietary WidgetBuilder tool
3. Read Sarah's architecture doc at /docs/internal/arch-2024.md
```

✅ **Good (Generalized)**:
```markdown
## First Week Onboarding Pattern
1. Clone the main application repository
2. Install required development tools (check team's README)
3. Read architecture documentation to understand system components
```

## 🛡️ Security & Privacy Checklist

Before submitting, review for:

- [ ] No API keys, credentials, or secrets
- [ ] No internal company URLs, paths, or infrastructure details
- [ ] No personally identifiable information (names, emails, etc.)
- [ ] No proprietary algorithms or business logic
- [ ] No customer data or real user examples
- [ ] No .env file contents or configuration values
- [ ] No database schemas or connection strings
- [ ] No company-specific tooling or processes
- [ ] No competitive information or trade secrets

### Use Generic Examples:

❌ **Bad**: `Meet with your mentor John Smith (john.smith@acme.com) on Monday`
✅ **Good**: `Schedule introductory meeting with your assigned mentor`

❌ **Bad**: `Our monorepo at /Users/shared/acme-monorepo has 47 services`
✅ **Good**: `Navigate the codebase structure, typically organized into services/components`

## 🎓 Special: New Developer Contributions

If you recently joined a company and used AI tools during onboarding:

**Your Fresh Perspective is Valuable!** You can contribute:

1. **Feedback on existing configs**
   - What worked well?
   - What was confusing?
   - What would you change?

2. **New config ideas**
   - What did you wish you had?
   - What configs would have helped?
   - What patterns emerged?

3. **Documentation improvements**
   - What was unclear?
   - What explanations would have helped?
   - What examples were missing?

**How to contribute as a new developer:**
- Open an issue describing your onboarding experience
- Suggest improvements to existing configs
- Propose new onboarding scenarios to address
- Share (generalized) patterns that worked for you

## 🤝 Code of Conduct

When contributing:

- Be respectful and professional
- Provide constructive, beginner-friendly feedback
- Remember your audience includes new developers
- Focus on the content, not the person
- Help others learn and improve
- Be patient with questions
- Foster an inclusive, welcoming environment

## 💡 Contribution Ideas

Need inspiration? Consider contributing:

### Configs
- First-day setup configs for different tools
- Pair programming configs for mentor/mentee scenarios
- Codebase exploration configs with guardrails
- Week-by-week progression configs
- Language/framework-specific onboarding configs

### Documentation
- Onboarding checklists for different company sizes
- AI tool comparison for new developers
- Troubleshooting guides for common setup issues
- Best practices for managers onboarding with AI tools

### Templates
- Team-specific onboarding workflow templates
- Personal learning path templates
- Mentor guide templates
- Progress tracking templates

## 📧 Questions?

If you're unsure about:
- Whether your config is appropriate for this repo
- How to generalize from your company's onboarding
- Licensing or attribution requirements
- What constitutes confidential information
- Anything else

Open an issue tagged `question`, `licensing`, or `onboarding-feedback` and we'll help clarify.

## 🙏 Recognition

All contributors will be recognized in:
- Git commit history
- GitHub contributors page
- NOTICE.md attribution file (for significant contributions)
- Release notes (for major contributions)

Thank you for helping improve developer onboarding with AI tools! ✨

---

**License Note**: By contributing to this repository, you agree to license your contributions under GPL-3.0. You certify that you have the right to submit the contribution and that it complies with all requirements above.
