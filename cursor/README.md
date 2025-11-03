# Cursor Configurations

This directory contains configuration files for [Cursor](https://cursor.sh/), the AI-powered code editor.

## 📁 Directory Structure

```
cursor/
└── .cursorrules/     # Cursor rule files
```

## 🚀 Available Configurations

**`comprehensive_development.rules`**
- **Purpose**: Complete AI collaboration guide for professional development
- **Best for**: Teams and individuals wanting structured AI-assisted development
- **Key features**:
  - Documentation-first approach
  - Task management and progress tracking
  - Code quality standards (TypeScript, file size, patterns)
  - Test-driven development practices
  - Debugging and troubleshooting guidelines
  - Security best practices
  - Version control standards

## 💡 How to Use

### Project-Specific Configuration

Copy to your project root:

```bash
cp cursor/.cursorrules/comprehensive_development.rules myproject/.cursorrules
```

### Global Configuration

Create a global Cursor rules file:

```bash
mkdir -p ~/.cursor
cp cursor/.cursorrules/comprehensive_development.rules ~/.cursor/rules
```

## 📖 Configuration Format

Cursor reads `.cursorrules` files from:
- **Project**: `project-root/.cursorrules`
- **Global**: `~/.cursor/rules` (or as configured in Cursor settings)

Rules files use markdown or plain text format.

## 🎯 What This Config Provides

| Feature | Description |
|---|---|
| **AI Collaboration Guidelines** | How to work effectively with AI assistance |
| **Code Quality Standards** | TypeScript, linting, file organization |
| **Testing Framework** | TDD practices, coverage requirements |
| **Security Practices** | Input validation, credential management |
| **Version Control** | Git practices, branching strategies |
| **Documentation Standards** | When and how to update docs |

## 🔧 Customization Tips

1. **File size limits**: Adjust 300-line threshold to match your team's preferences
2. **Build tools**: Update references to your specific build system
3. **Testing framework**: Adapt TDD guidelines to your test runner
4. **Documentation paths**: Change `docs/` paths to match your structure
5. **Linting rules**: Reference your specific ESLint/Prettier config

## 📚 Related Documentation

- [Cursor Documentation](https://cursor.sh/docs)
- [Main Repository README](../README.md)
- [Contributing Guidelines](../CONTRIBUTING.md)

## 🤝 Contributing

Have a Cursor config to share? See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

**License**: GPL-3.0 | See [LICENSE](../LICENSE) for details
