# Team AI Configuration Template

Use this template to create standardized AI configurations for your team's onboarding process.

## How to Use This Template

1. **Copy this file** to your team's repository
2. **Fill in the [PLACEHOLDERS]** with your team's specific information
3. **Customize the sections** to match your team's practices
4. **Share with new hires** during onboarding
5. **Update regularly** based on feedback

## Team Information

**Team Name**: [Your Team Name]
**Department**: [Engineering / Product / etc.]
**Primary Tech Stack**: [React, Node.js, Python, etc.]
**Onboarding Contact**: [Name/Email of onboarding coordinator]

---

# [Team Name] Onboarding Configuration

## Welcome!

You're joining the [Team Name] team. This configuration helps you learn our codebase, practices, and standards using AI assistance.

**Your onboarding buddy**: [Name]
**Your manager**: [Name]
**Team Slack channel**: #[channel-name]

## Our Codebase

### Architecture Overview

[Provide high-level description of your system architecture]

**Example**:
> We're a microservices architecture with:
> - React frontend
 (client/ directory)
> - Node.js API gateway (api/ directory)
> - Python ML services (ml-services/ directory)
> - PostgreSQL database
> - Redis for caching

### Repository Structure

[Explain your folder organization]

**Example**:
```
your-repo/
├── client/          # React frontend application
├── api/             # Node.js API gateway
├── ml-services/     # Python ML microservices
├── shared/          # Shared utilities and types
├── docs/            # Team documentation
└── tests/           # Integration tests
```

### Key Components

[List the main components/modules a new developer should understand]

**Example**:
1. **Authentication Service** (`api/auth/`) - OAuth2 implementation
2. **User Dashboard** (`client/components/Dashboard/`) - Main user interface
3. **ML Pipeline** (`ml-services/pipeline/`) - Data processing and model inference
4. **Shared Types** (`shared/types/`) - TypeScript definitions used everywhere

## Our Development Practices

### Git Workflow

[Describe your git branching and PR process]

**Example**:
> We use trunk-based development:
> 1. Create feature branch from `main`: `feature/your-name/description`
> 2. Make small, frequent commits
> 3. Open PR when ready (even if not complete - use draft PRs)
> 4. Get at least 2 approvals
> 5. Squash and merge to `main`
> 6. Delete feature branch

### Code Review Standards

[What you look for in code reviews]

**Example**:
> Our code reviews focus on:
> - **Functionality**: Does it work correctly?
> - **Tests**: Is it well-tested?
> - **Readability**: Can others understand it?
> - **Performance**: Any obvious performance issues?
> - **Security**: Any security concerns?

### Testing Requirements

[Your testing expectations]

**Example**:
> All code must include:
> - Unit tests for business logic (>80% coverage)
> - Integration tests for API endpoints
> - E2E tests for critical user flows
> - Manual testing documented in PR description

### Code Style

[Your formatting and style standards]

**Example**:
> We use:
> - **TypeScript**: Strict mode enabled
> - **Linting**: ESLint with our custom config
> - **Formatting**: Prettier (runs on save)
> - **Naming**: camelCase for variables, PascalCase for components
> - **Imports**: Organized by: external, internal, relative

## Onboarding Path

### Week 1: Learn the Basics
**Goals**: Understand architecture, run project locally, make first small contribution

**Focus areas**:
- [Component/system to explore]
- [Another area to learn]
- [Documentation to read]

**Suggested tasks**:
- [ ] Set up local environment
- [ ] Run full test suite
- [ ] Fix a documentation typo
- [ ] Add a unit test
- [ ] Attend team standup

### Week 2-4: Build Skills
**Goals**: Take on starter tasks, participate in code reviews, pair program

**Focus areas**:
- [More advanced component]
- [Important integration points]
- [Team processes]

**Suggested tasks**:
- [ ] Implement a small feature
- [ ] Fix a bug from backlog
- [ ] Pair with team member
- [ ] Review someone's PR
- [ ] Attend sprint planning

### Month 2+: Full Contributor
**Goals**: Work on regular team tasks, mentor others

**You should be able to**:
- [ ] Take on features independently
- [ ] Understand cross-system impacts
- [ ] Provide meaningful code reviews
- [ ] Help onboard the next new hire

## AI Configuration Guidance

### Use These Configs

**Week 1**:
```bash
cp open-onboarding/claude/onboarding/first_week_developer.md .claude/CLAUDE.md
```

**Week 2-4**:
```bash
cp open-onboarding/claude/onboarding/pair_programming_mentor.md .claude/CLAUDE.md
```

**Month 2+**:
```bash
cp open-onboarding/claude/general/global_development.md .claude/CLAUDE.md
```

### Team-Specific AI Instructions

[Add any team-specific instructions for AI]

**Example**:
> When working with our AI tools, please note:
> - We prefer functional React components over class components
> - Our API follows REST conventions strictly
> - We use React Query for all data fetching
> - Security: Never log sensitive user data

## Team Resources

### Documentation
- **Wiki**: [link]
- **Architecture docs**: [link]
- **API docs**: [link]
- **Runbooks**: [link]

### Development
- **CI/CD**: [Jenkins/GitHub Actions/etc at link]
- **Staging environment**: [link]
- **Monitoring**: [Datadog/etc at link]
- **Error tracking**: [Sentry/etc at link]

### Communication
- **Team Slack**: #[channel]
- **Standup**: [time and location]
- **Sprint planning**: [time and location]
- **Retro**: [time and location]

### Contacts
- **Onboarding questions**: @[name]
- **Technical questions**: @[name]
- **DevOps/infrastructure**: @[name]
- **On-call lead**: @[name]

## Common Patterns

### [Pattern Name]

[Explain a common pattern in your codebase]

**Example - API Error Handling**:
> All API endpoints use our standard error handling middleware:
> ```typescript
> try {
>   // endpoint logic
> } catch (error) {
>   logger.error('Operation failed', { error, context })
>   throw new AppError(error.message, error.code)
> }
> ```
> Find examples in: `api/users/routes.ts`, `api/auth/routes.ts`

### [Another Pattern]

[Another important pattern]

## FAQs for New Team Members

**Q: How do I get access to [system]?**
A: [Answer]

**Q: What should I do if I'm blocked?**
A: [Answer]

**Q: How do I deploy to staging?**
A: [Answer]

**Q: Who do I ask about [topic]?**
A: [Answer]

## Feedback & Updates

This configuration is a living document. If you:
- Found something confusing
- Have suggestions for improvement
- Discovered important information that's missing

Please:
1. Open a PR with suggested changes
2. Discuss in #[team-channel]
3. Bring up in retro

---

**Last updated**: [Date]
**Maintained by**: [Team/Person]
**Version**: [Version number]
