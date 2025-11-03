# ---
# name: team_tpm_security.md
# tool: Claude Code
# purpose: Team practices, methodologies, and role-based development guidance for Scrum/Kanban hybrid teams
# source: inspired by community configs shared on r/ClaudeAI
# license: GPL-3.0
# ---

# Team-Based Development Framework

## Core Values

**Simplicity, Efficiency, Robustness** - Build scalable systems without unnecessary complexity. Favor straightforward solutions that work reliably over elaborate architectures that are difficult to maintain.

## Development Standards

### File Management
- Create new files only when necessary
- Modify existing code rather than duplicating it
- Maintain working implementations through iterations
- Remove unnecessary documentation from source code
- Validate all modifications through testing

## Agile Methodology: Scrum with Kanban Elements

### Scrum Structure

**Iteration Cadence**: Two-week sprints

**Team Roles**:
- **Product Owner**: Defines requirements and priorities
- **Technical Program Manager**: Coordinates execution, removes impediments, facilitates processes
- **Development Team**: Engineers, designers, QA, security specialists, operations

### Key Meetings

**Sprint Planning** - Define sprint objectives and work commitments at sprint start
**Daily Standup** - 15-minute technical team synchronization
**Sprint Review** - Demonstrate completed work to stakeholders
**Retrospective** - Evaluate and improve team processes

### Kanban Integration

**Marketing Stream**: Continuous flow board for campaigns and content
**Operations Work**: Separate board tracking bugs, patches, and infrastructure
**Workflow States**: Backlog → Active → Review → Complete

## Team Member Specializations

### Engineering Roles

**Principal Engineer** - Designs system architecture, mentors team members, balances technical excellence with delivery timelines. Responsible for long-term technical vision and code quality standards.

**Frontend Engineer/Designer** - Builds user interfaces by combining design expertise with implementation skills. Ensures products are both visually effective and technically sound.

**DevOps Engineer** - Manages infrastructure, deployment pipelines, and cross-team collaboration. Optimizes the software development lifecycle through automation and integration.

### Quality & Security

**QA Specialist** - Prevents defects through proactive testing strategies. Validates software meets requirements and delivers seamless user experiences.

**Security Operations** - Protects digital assets through monitoring, threat detection, vulnerability management, and incident response. Integrates security into development workflows.

### Program Management

**Technical Program Manager (TPM)** - Orchestrates complex technical initiatives across teams. Translates technical requirements into business value while managing risks and dependencies.

### Marketing & Communications

**Digital Marketing Specialist** - Executes online campaigns with focus on search optimization (SEO/AEO) and structured data (Schema.org).

**Brand Messaging Expert** - Clarifies product messaging using storytelling frameworks. Positions customers as heroes and products as solutions.

**Content Strategist** - Plans and manages content to achieve business goals. Conducts research, creates editorial calendars, and measures content effectiveness.

## Team Groupings

**Full Team**: All roles listed above
**Technical Team**: Engineers, TPM, QA, Security, DevOps
**Marketing Team**: TPM, Digital Marketing, Brand Messaging, Content Strategy
**Deployment Team**: DevOps, Security, Principal Engineer, QA

## Quality Assurance

### Completion Criteria
- Code approved through peer review
- Automated test suite passing
- Security analysis complete
- Staging environment deployment successful
- Product Owner sign-off obtained

### Security Integration
- QA involvement from requirements phase (shift-left testing)
- Security reviews embedded in sprint cycle
- Threat modeling for new capabilities
- Automated security scanning in deployment pipeline

### Marketing Alignment
- Marketing participation in Sprint Reviews for early input
- Product Owner tracks marketing requirements in backlog
- Weekly synchronization between technical and marketing work

## Communication Framework

**Technical Channels**: Engineering-focused discussions
**Marketing Channels**: Campaign and content strategy
**Cross-Functional Meetings**: Weekly alignment between Product Owner, TPM, and team leads
**Escalations**: Direct communication to TPM and relevant specialists

## Success Metrics

- Sprint goal achievement rate
- Time from concept to production
- Production defect frequency
- Marketing-technical alignment on releases
