# Manager's Onboarding Workflow Template

A playbook for managers and team leads to standardize onboarding with AI assistance.

## Purpose

This template helps you create a consistent, effective onboarding experience using AI tools. It's designed for engineering managers, team leads, and onboarding buddies.

## Pre-Arrival (1 week before start date)

### Administrative Setup
- [ ] Create accounts (email, Slack, GitHub, etc.)
- [ ] Add to team calendars and meetings
- [ ] Assign mentor/onboarding buddy
- [ ] Prepare machine/equipment
- [ ] Send welcome email with Day 1 logistics

### Technical Prep
- [ ] Grant repository access
- [ ] Add to relevant Slack channels
- [ ] Prepare list of starter tasks
- [ ] Update team docs if needed
- [ ] Set up development environment guide

### AI Tool Preparation

**Decide on AI tool**:
- [ ] Confirm what AI tools team uses (if any)
- [ ] Choose recommended tool for new hire
- [ ] Prepare license/access if needed
- [ ] Customize team config from `templates/team-config-template.md`

**Create team-specific config**:
```bash
# Customize for your team
cp open-onboarding/templates/team-config-template.md your-team-repo/docs/ai-onboarding-config.md

# Fill in:
# - Your team's architecture
# - Common patterns
# - Development workflow
# - Key resources
```

**Prepare in onboarding docs**:
- [ ] Link to AI tool setup guide
- [ ] Include your team's custom AI config
- [ ] Add to Day 1 checklist

## Day 1: Welcome & Setup

### Morning (Manager/Lead)

**9:00 AM - Welcome**:
- [ ] Personal welcome and introduction
- [ ] Team overview and vision
- [ ] Explain team culture and values
- [ ] Set expectations for onboarding

**9:30 AM - Admin & Logistics**:
- [ ] Verify all access granted
- [ ] Tour of office/remote setup
- [ ] Introduction to key tools and systems
- [ ] Review schedule for the week

**10:00 AM - Meet the Team**:
- [ ] Introduce to immediate team
- [ ] Schedule 1:1s with key people
- [ ] Explain team structure and roles
- [ ] Identify onboarding buddy

### Afternoon (Mentor/Buddy)

**1:00 PM - Development Setup**:
- [ ] Help set up development environment
- [ ] Clone repositories
- [ ] Run project locally (even if there are errors)
- [ ] Verify basic tools work

**2:00 PM - AI Tool Setup**:
- [ ] Install chosen AI tool (Claude Code, Cursor, or Cline)
- [ ] Copy first-week onboarding config
- [ ] Test config with simple questions
- [ ] Review [quickstart-guide.md](../docs/quickstart-guide.md)

**3:00 PM - Codebase Overview**:
- [ ] High-level architecture explanation
- [ ] Tour of repository structure
- [ ] Point out key components
- [ ] Show where documentation lives

**4:00 PM - First AI-Assisted Exploration**:
Help them ask AI:
- "Explain the architecture of this codebase"
- "Where should I start exploring?"
- "What patterns should I know about?"

**4:30 PM - Day 1 Wrap-up**:
- [ ] Check in on how they're feeling
- [ ] Answer questions
- [ ] Preview Day 2
- [ ] Ensure they know who to contact for what

### Day 1 Checklist to Give New Hire

```markdown
## Your Day 1 Checklist

### Morning
- [ ] Complete HR paperwork
- [ ] Get access to all systems
- [ ] Meet the team
- [ ] Set up workstation

### Afternoon
- [ ] Set up development environment
- [ ] Install AI tool (Claude Code/Cursor/Cline)
- [ ] Copy onboarding config
- [ ] Run the project locally
- [ ] Explore codebase with AI assistance

### End of Day
- [ ] Join team Slack channels
- [ ] Schedule 1:1s
- [ ] Note questions for tomorrow
```

## Week 1: Foundation

### Monday-Tuesday: Learning
**Manager's role**:
- [ ] Daily check-in (15 min)
- [ ] Remove blockers
- [ ] Answer high-level questions

**Mentor's role**:
- [ ] Help navigate codebase
- [ ] Explain architecture
- [ ] Show development workflow
- [ ] Guide AI tool usage

**AI Tool Support**:
- Ensure they're using `first_week_developer.md` or equivalent
- Check they understand how to ask effective questions
- Help if AI responses aren't helpful

### Wednesday-Friday: First Contributions
**Manager's role**:
- [ ] Identify appropriate starter task
- [ ] Clarify expectations
- [ ] Mid-week 1:1 check-in

**Mentor's role**:
- [ ] Help with first task
- [ ] Review approach before implementation
- [ ] Guide through PR process
- [ ] Provide thorough code review

**Milestone**: First PR merged by Friday

### Friday: Week 1 Retro
**Manager 1:1** (30 min):
- What went well?
- What was confusing?
- How is AI assistance helping?
- What to focus on Week 2?

**Mentor Check-in**:
- Technical progress assessment
- Identify knowledge gaps
- Plan Week 2 tasks

## Week 2-4: Building Skills

### Manager's Weekly Cadence

**Monday**:
- [ ] Review progress and plan
- [ ] Identify tasks for the week
- [ ] Check in on wellbeing

**Wednesday**:
- [ ] Mid-week check-in
- [ ] Remove blockers
- [ ] Adjust plan if needed

**Friday**:
- [ ] Week retro
- [ ] Celebrate wins
- [ ] Plan next week

### Mentor's Daily Support

**Daily**:
- [ ] Be available for questions
- [ ] Pair program if helpful
- [ ] Review PRs promptly
- [ ] Provide feedback

**Weekly**:
- [ ] More in-depth code review session
- [ ] Introduce new areas of codebase
- [ ] Check AI config is still appropriate

### Progression Milestones

**Week 2**:
- [ ] Comfortable navigating codebase
- [ ] Understands development workflow
- [ ] Making regular small contributions
- [ ] Participating in code reviews

**Week 3**:
- [ ] Taking on larger tasks
- [ ] Writing comprehensive tests
- [ ] Providing meaningful code reviews
- [ ] Starting to work more independently

**Week 4**:
- [ ] Leading small features end-to-end
- [ ] Debugging issues independently
- [ ] Understanding cross-system impacts
- [ ] Ready to transition to standard AI config

### AI Config Progression

**Week 2**: Continue with `first_week_developer.md`
**Week 3-4**: Consider `pair_programming_mentor.md` if doing lots of pairing
**Week 4 end**: Discuss transitioning to `global_development.md`

## Month 2: Independence

### Manager's Role

**Bi-weekly 1:1s focusing on**:
- Ownership of areas
- Career development
- Team integration
- Long-term goals

**Monthly**:
- [ ] Formal onboarding review
- [ ] Gather 360 feedback
- [ ] Discuss performance expectations
- [ ] Plan next phase

### Mentor Transition

**Gradually reduce**:
- Daily check-ins
- Hand-holding on tasks
- Detailed code review explanations

**Increase**:
- Peer-level collaboration
- Reverse mentoring (them teaching you)
- Independent problem-solving

### AI Config Transition

**Month 2 start**:
- [ ] Transition to `global_development.md`
- [ ] Discuss customization preferences
- [ ] Encourage experimenting with slash commands
- [ ] Share advanced AI usage patterns

## Measuring Success

### Week 1 Success Metrics
- [ ] Development environment working
- [ ] Can navigate codebase
- [ ] First PR merged
- [ ] Knows who to ask for help
- [ ] AI tool configured and being used

### Month 1 Success Metrics
- [ ] Comfortable with team workflow
- [ ] Contributing regularly
- [ ] Participating in code reviews
- [ ] Understanding architecture
- [ ] Using AI effectively for learning

### Month 2 Success Metrics
- [ ] Working independently
- [ ] Leading features
- [ ] Mentoring capabilities emerging
- [ ] Full team member velocity
- [ ] Using AI for productivity, not just learning

## Common Issues & Solutions

### They're Overwhelmed
**Signs**: Lots of questions, appearing lost, low confidence

**Solutions**:
- Break down tasks smaller
- More frequent check-ins
- Pair programming sessions
- Remind them it's normal
- Check AI config is helping (not overwhelming)

### They're Not Asking Enough Questions
**Signs**: Stuck for long periods, working in wrong direction

**Solutions**:
- Explicitly encourage questions
- Set "maximum stuck time" (30 min)
- Regular check-ins to surface blockers
- Normalize not knowing things
- Show them how to use AI to unblock

### AI Tool Not Helping
**Signs**: Not using it, frustrated with responses, relying only on human help

**Solutions**:
- Review their config (is it appropriate?)
- Show effective questioning techniques
- Pair with them using AI
- Check if tool is working correctly
- Consider different AI tool if persistent

### Moving Too Fast/Slow
**Too fast**: Missing fundamentals, surface-level understanding
**Too slow**: Not making progress, overly cautious

**Solutions**:
- Adjust task complexity
- More/less guidance as needed
- Pair programming to calibrate
- Explicit feedback on pacing
- Check if AI config matches their pace

## Team-Specific Customization

[Customize this section for your team]

### Our Team's Onboarding Philosophy
[Your team's approach]

### Unique Aspects of Our Codebase
[What makes your codebase special/challenging]

### Our AI Tool Preferences
[What AI tools your team uses and why]

### Our Success Stories
[Examples of successful onboarding]

### Our Lessons Learned
[What you've learned from past onboarding]

## Resources

### For Managers
- [open-onboarding repo](https://github.com/yourusername/open-onboarding)
- [onboarding-checklist.md](../docs/onboarding-checklist.md)
- [Team config template](team-config-template.md)

### For New Hires
- [quickstart-guide.md](../docs/quickstart-guide.md)
- [first-week-guide.md](../docs/first-week-guide.md)
- [ai-tools-comparison.md](../docs/ai-tools-comparison.md)

### For Mentors
- Your team's custom AI config
- Pair programming configs
- Code review guidelines

## Feedback Loop

**Continuously improve**:
- [ ] Gather feedback from each new hire
- [ ] Update this workflow based on learnings
- [ ] Share successes with other teams
- [ ] Iterate on AI configs
- [ ] Track what's working and what's not

**Monthly review**:
- What's working well in onboarding?
- What could be better?
- How is AI assistance impacting time-to-productivity?
- What configs need updating?

---

**Template maintained by**: [Your name/team]
**Last updated**: [Date]
**Version**: [Version]

**Feedback welcome**: [How to provide feedback]
