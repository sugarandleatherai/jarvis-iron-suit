# Team Playbook

Welcome to the Jarvis Iron Suit team! This playbook will guide you through our processes, tools, and team culture.

## Table of Contents
1. [Getting Started](#getting-started)
2. [Team Structure](#team-structure)
3. [Development Workflow](#development-workflow)
4. [Communication](#communication)
5. [Tools & Technologies](#tools--technologies)
6. [Best Practices](#best-practices)

## Getting Started

### First Day Checklist
- [ ] Complete HR onboarding
- [ ] Set up development environment
- [ ] Get access to GitHub organization
- [ ] Join Slack workspace
- [ ] Review project documentation
- [ ] Meet with your team lead
- [ ] Schedule 1:1s with team members

### Account Setup
1. **GitHub**: Request access to `sugarandleatherai` organization
2. **Slack**: Join the Jarvis workspace channels
3. **Email**: Configure your @sugarandleatherai.com email
4. **Calendar**: Sync team calendar for meetings and events

## Team Structure

### Core Team
- **Product Lead**: Strategic direction and roadmap
- **Engineering Lead**: Technical architecture and code quality
- **Automation Engineers**: Core automation development
- **Integration Specialists**: Slack and third-party integrations
- **DevOps**: Infrastructure and deployment

### Roles & Responsibilities

#### Automation Engineers
- Develop core automation features
- Write tests and documentation
- Code review and mentoring
- Participate in sprint planning

#### Integration Specialists
- Build and maintain Slack integrations
- API design and development
- Third-party service integration
- Integration testing

## Development Workflow

### Sprint Cycle
- **Duration**: 2 weeks
- **Sprint Planning**: Monday morning
- **Daily Standups**: 9:30 AM EST
- **Sprint Review**: Friday afternoon
- **Retrospective**: Following sprint review

### Git Workflow
1. Create feature branch from `main`
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make changes and commit regularly
   ```bash
   git commit -m "feat: add new feature"
   ```
3. Push to remote and create PR
   ```bash
   git push origin feature/your-feature-name
   ```
4. Request reviews from at least 2 team members
5. Address feedback and merge when approved

### Commit Message Convention
We follow [Conventional Commits](https://www.conventionalcommits.org/):
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks

### Code Review Guidelines
- Review within 24 hours
- Be constructive and respectful
- Focus on code quality, not coding style
- Test the changes locally when possible
- Approve only when you're confident

## Communication

### Channels

#### Slack Channels
- `#jarvis-general`: General team discussion
- `#jarvis-dev`: Development questions and updates
- `#jarvis-automation`: Automation core discussions
- `#jarvis-integrations`: Integration-specific topics
- `#jarvis-alerts`: Automated notifications

#### Meetings
- **Daily Standup**: Quick sync (15 min)
- **Sprint Planning**: Plan upcoming sprint (2 hours)
- **Sprint Review**: Demo completed work (1 hour)
- **Retrospective**: Process improvement (1 hour)
- **1:1s**: Individual meetings with lead (bi-weekly)

### Communication Best Practices
- Use threads to keep conversations organized
- Set status when away or focused
- Respond to mentions within business hours
- Use `@here` sparingly
- Document decisions in GitHub issues

## Tools & Technologies

### Development Tools
- **IDE**: VS Code (recommended), IntelliJ, or your preference
- **Version Control**: Git + GitHub
- **Package Manager**: npm/yarn (Node.js), pip (Python)
- **Testing**: Jest, Pytest, or language-specific frameworks

### Infrastructure
- **Cloud Provider**: AWS
- **CI/CD**: GitHub Actions
- **Monitoring**: CloudWatch, Datadog
- **Logging**: ELK Stack

### Project Management
- **Issues**: GitHub Issues
- **Projects**: GitHub Projects
- **Documentation**: Markdown in repo
- **Wiki**: GitHub Wiki

## Best Practices

### Code Quality
- Write self-documenting code
- Add comments for complex logic
- Follow language-specific style guides
- Keep functions small and focused
- Write unit tests for new features

### Security
- Never commit secrets or credentials
- Use environment variables for config
- Follow principle of least privilege
- Keep dependencies up to date
- Report security issues privately

### Documentation
- Update README for significant changes
- Document API endpoints and interfaces
- Add inline comments for complex code
- Keep architecture diagrams current
- Write clear commit messages

### Testing
- Write tests before fixing bugs
- Aim for >80% code coverage
- Test edge cases and error handling
- Run tests locally before pushing
- Keep tests fast and isolated

## Resources

### Learning Materials
- [Project Wiki](https://github.com/sugarandleatherai/jarvis-iron-suit/wiki)
- [API Documentation](./docs/api.md)
- [Architecture Guide](./docs/architecture.md)

### Support
- **Technical Questions**: `#jarvis-dev` on Slack
- **Process Questions**: Ask your team lead
- **HR/Admin**: hr@sugarandleatherai.com

## Offboarding
When a team member leaves:
- [ ] Complete knowledge transfer
- [ ] Document ongoing work
- [ ] See audrey-process-transfer.md for handoff process
- [ ] Revoke access to systems
- [ ] Archive communication channels

---

*Last Updated: 2025-11-13*
*Questions? Contact: team-lead@sugarandleatherai.com*
