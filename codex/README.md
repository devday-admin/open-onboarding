# Codex Configurations

This directory contains configuration files for Codex and similar autonomous coding agents.

## 📁 Directory Structure

```
codex/
├── README.md
├── general/          # General-purpose configs for autonomous agents
└── specialized/      # Specialized configs for specific workflows
```

## 🚀 Available Configurations

### General Purpose

**`autonomous_agent_style.md`**
- **Purpose**: Autonomous agent operating principles for persistent, thorough coding work
- **Best for**: Coding agents that work independently for extended periods
- **Key features**:
  - Persistent execution until blocked
  - Intelligent debugging with logging
  - Continuous verification of work
  - Safe terminal command handling
  - Work handoff documentation protocol

## 💡 How to Use

### Project Configuration

Copy to your project's agent configuration location (varies by tool):

```bash
# For Codex-style agents
cp codex/general/autonomous_agent_style.md myproject/.codex/agents.md

# Or as project documentation
cp codex/general/autonomous_agent_style.md myproject/AGENT_INSTRUCTIONS.md
```

### Global Configuration

The specific location depends on your agent tool. Common patterns:

```bash
# Generic location
~/.config/codex/agents.md

# Or tool-specific
~/.codex/agents.md
```

## 📖 Configuration Philosophy

These configs focus on **autonomous operation** rather than collaborative dialogue:

**Key Differences from Claude Code configs:**
- Emphasis on working independently for long periods
- Explicit handoff protocols for context management
- Focus on process safety (background jobs, timeouts)
- Verification and testing as first-class concerns

**Similarities:**
- Clear documentation and standards
- Thoughtful problem-solving approaches
- Quality and testing requirements

## 🎯 When to Use Codex-Style Configs

Use these configurations when:

- You want the agent to work autonomously for extended periods
- Tasks involve multiple steps that build on each other
- You need comprehensive verification at each stage
- Context management and handoffs are important
- The agent should exhaust options before stopping

## 🔧 Customization Tips

1. **Notification scripts**: Update paths to your notification system
2. **Handoff format**: Adjust `handoff.md` template to your needs
3. **Process management**: Adapt commands to your preferred tools (pm2, systemctl, etc.)
4. **Verification steps**: Add project-specific testing requirements
5. **Logging standards**: Define your preferred logging format

## ⚠️ Important Notes

**Context Management:**
These configs emphasize handoff documentation because autonomous agents often work through long sessions that may exceed context limits.

**Process Safety:**
Autonomous agents can accidentally launch runaway processes. The config includes specific guidance on handling long-running commands safely.

**Verification Requirements:**
Unlike interactive agents, autonomous agents must verify their own work continuously since they can't rely on immediate human feedback.

## 📚 Related Documentation

- [Main Repository README](../README.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Claude Code Configs](../claude/) - For interactive development style

## 🤝 Contributing

Have a Codex or autonomous agent config to share? See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

**License**: GPL-3.0 | See [LICENSE](../LICENSE) for details
