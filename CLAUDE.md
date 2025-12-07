# CLAUDE.md - AI Assistant Guide

This file provides comprehensive guidance for AI assistants working with the **awesome-claude-code-agents** repository.

## Repository Overview

**Purpose:** A curated collection of Claude Code Sub-Agent definitions focused on professional software development roles.

**Mission:** Provide high-quality, production-ready agent templates that emphasize:
- Best practices and security
- Specific technology expertise
- Practical, real-world examples
- Clear specialization and focused scope

**Current State:**
- 4 agent definitions in the `agents/` directory
- Minimal configuration (no .claude/, .github/, or build configs)
- Documentation-focused repository
- Contributors: Really Him (maintainer), TheCookingSenpai (4 agents), toyamarinyon

---

## Directory Structure

```
awesome-claude-code-agents/
├── .git/                          # Git version control
├── README.md                      # Main documentation with humorous introduction
├── agents/                        # All Sub-Agent definitions
│   ├── backend-typescript-architect.md
│   ├── python-backend-engineer.md
│   ├── senior-code-reviewer.md
│   └── ui-engineer.md
└── CLAUDE.md                      # This file
```

**Key Facts:**
- Single-purpose structure: Agents live in `agents/` directory only
- No build system, dependencies, or runtime code
- Pure markdown documentation repository
- Simple, focused organization for easy navigation

---

## Agent File Structure & Conventions

### File Naming Pattern

Use kebab-case with format: `{specialization}-{technology}.md`

**Examples:**
- `backend-typescript-architect.md` (specialization + primary tech)
- `python-backend-engineer.md` (language + role)
- `senior-code-reviewer.md` (seniority + function)
- `ui-engineer.md` (domain + role)

### YAML Frontmatter (Required)

Every agent file MUST have this frontmatter structure:

```yaml
---
name: agent-name-in-kebab-case
description: |
  Use this agent when you need [clear description of capabilities].

  <example>
  Context: [Business/technical scenario]
  user: "[Natural language request]"
  assistant: "[How to invoke the agent]"
  <commentary>
  [Reasoning for why this agent is appropriate]
  </commentary>
  </example>

  <example>
  Context: [Another scenario]
  user: "[Another request]"
  assistant: "[Another invocation]"
  <commentary>
  [More reasoning]
  </commentary>
  </example>

color: color-name
---
```

**Frontmatter Requirements:**
- **name:** Kebab-case identifier (e.g., `backend-typescript-architect`)
- **description:** Multi-sentence explanation with 2-3 `<example>` blocks
- **color:** Single color keyword for visual identification (e.g., `red`, `blue`, `green`, `purple`)

### Example Block Structure

Each `<example>` must contain:
1. **Context:** Business or technical scenario
2. **user:** Natural language request in quotes
3. **assistant:** Explanation of how to invoke the agent
4. **commentary:** Reasoning for agent selection (in XML-style tags)

### System Prompt Structure

Every agent should follow this pattern:

```markdown
# System Prompt

You are a [title/specialty] with [years/depth] of expertise in [domain].

## Core Competencies

- [Specialization 1]
- [Specialization 2]
- [Specialization 3]
- etc.

## Development Philosophy

[Core values and principles - 3-5 key points]

## Technical Expertise

[Specific tools, frameworks, and technologies]

## Approach to Tasks

When [working on task type]:

1. [First step - analysis/understanding]
2. [Second step - design/architecture]
3. [Third step - implementation]
4. [Fourth step - quality assurance]
5. [Fifth step - optimization/delivery]

## Communication Style

[How the agent interacts - tone, clarity, specificity]

## Output Expectations

[What the agent produces - code quality, documentation, format]
```

---

## Agent Archetypes

The repository currently includes three archetypes:

### 1. Technology Specialist Agents
**Examples:** `backend-typescript-architect`, `python-backend-engineer`, `ui-engineer`

**Characteristics:**
- Focused on implementation and code production
- Specific tech stack expertise (Bun, FastAPI, React, etc.)
- Output: Production-ready, well-documented code
- Philosophy: Best practices, security (OWASP), clean architecture
- Emphasizes: Type safety, error handling, performance

**When to Create:**
- Target a specific programming language or framework
- Focus on implementation rather than review
- Provide deep expertise in particular tech stack

### 2. Code Quality Assurance Agents
**Example:** `senior-code-reviewer`

**Characteristics:**
- Focused on analysis and quality assurance
- Multi-dimensional evaluation (security, performance, architecture)
- Output: Structured feedback with severity ratings
- Methodology: Systematic, comprehensive, prioritized
- Creates documentation in `claude_docs/` folders

**When to Create:**
- Focus on review, analysis, or quality assessment
- Need structured output formats (reports, documentation)
- Require multi-perspective evaluation

### 3. Potential Future Archetypes
- **DevOps/Infrastructure:** Deployment, CI/CD, containerization
- **Data Engineering:** ETL, data pipelines, analytics
- **Mobile Development:** iOS, Android, React Native
- **QA/Testing:** Test automation, quality assurance

---

## Development Workflows

### Adding a New Agent

1. **Choose Specialization:** Identify clear, focused expertise area
2. **Create File:** Use naming pattern `{specialization}-{technology}.md` in `agents/`
3. **Add Frontmatter:** Include name, description with 2-3 examples, and color
4. **Write System Prompt:** Follow structure with competencies, philosophy, methodology
5. **Be Specific:** Reference concrete tools, frameworks, and scenarios
6. **Include Examples:** Show when/how to use the agent with realistic scenarios
7. **Test:** Ensure examples are practical and agent scope is clear
8. **Update README.md:** Add entry with brief description and author attribution

### Modifying Existing Agents

1. **Read Current Version:** Understand existing scope and examples
2. **Maintain Structure:** Keep frontmatter format and system prompt pattern
3. **Preserve Intent:** Don't change fundamental agent purpose
4. **Enhance Examples:** Add clarity or real-world scenarios if needed
5. **Update Attribution:** Note changes in commit messages

### Quality Standards

All agents must:
- ✅ Have clear, focused specialization (avoid "do everything" agents)
- ✅ Include 2-3 concrete examples in frontmatter
- ✅ Reference specific technologies/frameworks/tools
- ✅ Emphasize production-ready, secure code practices
- ✅ Follow consistent formatting and structure
- ✅ Use professional, direct communication style
- ✅ Include methodology/approach section
- ✅ Define output expectations clearly

---

## Key Conventions for AI Assistants

### When Contributing Agents

**DO:**
- Focus on single, clear specialization
- Include specific technology references (FastAPI, React, SQLAlchemy, etc.)
- Provide concrete, practical examples
- Emphasize security (OWASP Top 10, authentication, authorization)
- Use professional, confident tone ("expert," "senior," "elite")
- Define clear methodology with numbered steps
- Specify output format and quality expectations
- Keep examples realistic and domain-relevant

**DON'T:**
- Create overly broad "general purpose" agents
- Use vague or generic examples
- Skip security considerations
- Mix multiple unrelated specializations
- Use casual or uncertain language
- Omit methodology sections
- Leave output expectations undefined
- Copy-paste examples without customization

### Writing Style Guidelines

**Tone:**
- Professional and confident
- Direct and action-oriented
- Helpful but not overly deferential
- Technical precision over friendliness

**Language Patterns:**
- "You are a [senior/expert/elite] [specialization]"
- "Your core competencies include..."
- "When approaching [task], you will..."
- "Always ensure [quality standard]"
- "Proactively identify [issue type]"

**Example Quality:**
- Context should be realistic business scenarios
- User requests should be natural language, specific
- Assistant responses should explain agent invocation clearly
- Commentary should provide reasoning, not just restate

### File Organization

- Keep all agents in `agents/` directory
- One agent per file
- No subdirectories within `agents/`
- Use descriptive, clear file names
- Maintain alphabetical listing in README.md

### Documentation Maintenance

**README.md Updates:**
- Add new agents with one-line description
- Include author attribution (GitHub username)
- Maintain formatting consistency
- Link to external agent repositories when relevant

**CLAUDE.md Updates:**
- Update when new archetypes emerge
- Add examples if patterns change
- Keep structure section current
- Document new conventions as they develop

---

## Common Patterns & Best Practices

### Technology Specificity

Good agents reference specific tools:
- ✅ "Bun runtime, Elysia framework, Prisma ORM"
- ✅ "FastAPI, SQLAlchemy, Pydantic, pytest"
- ❌ "Modern backend frameworks"
- ❌ "Popular tools and libraries"

### Example Scenarios

Good examples are concrete and realistic:
- ✅ "User needs to implement JWT authentication with refresh tokens"
- ✅ "Optimize slow database queries in high-traffic API endpoints"
- ❌ "User needs help with backend"
- ❌ "Write some code"

### Security Emphasis

All implementation agents should mention:
- OWASP Top 10 awareness
- Authentication/authorization patterns
- Input validation and sanitization
- SQL injection prevention
- XSS protection
- Secure dependency management

### Code Quality Standards

Implementation agents should emphasize:
- **Type Safety:** TypeScript types, Python type hints
- **Documentation:** Docstrings, comments explaining "why"
- **Error Handling:** Comprehensive, user-friendly errors
- **Testing:** Unit tests, integration tests, coverage
- **Performance:** Optimization, profiling, scalability
- **Maintainability:** Clean code, SOLID principles, design patterns

### Review/Analysis Agents

Quality assurance agents should:
- Define systematic methodology
- Use severity ratings (Critical, High, Medium, Low)
- Provide actionable, specific feedback
- Include positive observations
- Reference line numbers and files
- Create structured documentation output

---

## Git Workflow

### Branching

- Work on feature branches prefixed with `claude/`
- Branch naming: `claude/[description]-[session-id]`
- Current branch: `claude/claude-md-mi4xubfsogiw053o-01TVKP6AZVFcKRbJ9p7GK2uR`

### Commits

**Format:**
```
<type>: <concise description>

[Optional detailed explanation]
```

**Types:**
- `feat:` New agent or major feature
- `docs:` Documentation updates
- `fix:` Bug fixes or corrections
- `refactor:` Structure changes without new features
- `chore:` Maintenance tasks

**Examples:**
- `feat: add devops-engineer agent`
- `docs: update README with new agent links`
- `fix: correct example formatting in backend-typescript-architect`

### Pushing Changes

```bash
# Always use -u flag for first push on new branch
git push -u origin claude/[branch-name]

# Retry with exponential backoff on network errors (2s, 4s, 8s, 16s)
```

---

## Repository-Specific Context

### No Build System

This is a documentation-only repository:
- No package.json, pyproject.toml, or build configs
- No runtime dependencies to install
- No tests to run
- No CI/CD pipelines (yet)

**Implication:** Focus on content quality, not code functionality

### No .claude/ Directory

Unlike many Claude Code projects, this repository has:
- No custom slash commands
- No hooks configuration
- No agent definitions for local use (agents are for sharing)

**Implication:** Agents here are templates/examples, not active tools

### Contribution Culture

Based on README.md:
- Humorous, friendly tone in documentation
- Attribution to contributors encouraged
- Open to submissions
- Links to related projects welcomed
- Community-oriented sharing philosophy

---

## Example: Creating a New Agent

Here's a complete example of adding a `devops-engineer` agent:

### 1. Create File: `agents/devops-engineer.md`

```yaml
---
name: devops-engineer
description: |
  Use this agent when you need assistance with DevOps, infrastructure automation,
  CI/CD pipelines, containerization, or cloud platform configuration. This includes
  tasks like setting up deployment pipelines, configuring Kubernetes clusters,
  writing Infrastructure as Code, optimizing cloud costs, or implementing monitoring
  and observability solutions.

  <example>
  Context: User needs to set up CI/CD pipeline for Node.js application
  user: "Help me create a GitHub Actions workflow that runs tests and deploys to AWS"
  assistant: "I'll use the devops-engineer agent to help you build a comprehensive
  CI/CD pipeline with testing, security scanning, and AWS deployment"
  <commentary>
  Since the user needs DevOps expertise for pipeline setup and cloud deployment,
  the devops-engineer agent is the appropriate choice.
  </commentary>
  </example>

  <example>
  Context: User wants to containerize their application
  user: "I need to Dockerize my microservices and set up Kubernetes orchestration"
  assistant: "Let me use the devops-engineer agent to help you containerize your
  services and configure Kubernetes for production deployment"
  <commentary>
  Containerization and orchestration are core DevOps responsibilities, making
  this agent the right fit.
  </commentary>
  </example>

color: orange
---

# System Prompt

You are a senior DevOps engineer with 10+ years of experience in infrastructure
automation, cloud platforms, and CI/CD pipeline design. You have deep expertise
in containerization, orchestration, and modern DevOps practices.

## Core Competencies

- **Infrastructure as Code:** Terraform, CloudFormation, Pulumi, Ansible
- **Container Technologies:** Docker, Kubernetes, Helm, Docker Compose
- **CI/CD Platforms:** GitHub Actions, GitLab CI, Jenkins, CircleCI
- **Cloud Platforms:** AWS, Google Cloud, Azure (multi-cloud expertise)
- **Monitoring & Observability:** Prometheus, Grafana, ELK Stack, DataDog
- **Security:** Secret management, IAM, security scanning, compliance
- **Scripting:** Bash, Python for automation and tooling
- **Networking:** Load balancing, DNS, CDN, service mesh

## Development Philosophy

- Infrastructure should be version-controlled and reproducible
- Automation over manual processes
- Security and compliance built in from the start
- Monitoring and observability are non-negotiable
- Cost optimization without sacrificing reliability
- Documentation as code

## Approach to Infrastructure Tasks

When working on infrastructure or DevOps tasks:

1. **Assess Requirements:** Understand scalability, security, and compliance needs
2. **Design Architecture:** Plan infrastructure with high availability and disaster recovery
3. **Implement as Code:** Write declarative, version-controlled infrastructure definitions
4. **Automate Pipelines:** Create CI/CD workflows with proper testing and validation
5. **Monitor and Optimize:** Set up observability and continuously improve performance

Always ensure infrastructure is:
- Secure by default (least privilege, encryption, secret management)
- Scalable and resilient (auto-scaling, health checks, failover)
- Cost-optimized (right-sizing, reserved instances, cleanup policies)
- Well-documented (architecture diagrams, runbooks, comments)
- Tested and validated (infrastructure tests, policy validation)

Provide production-ready configurations with comprehensive error handling and rollback
strategies.
```

### 2. Update README.md

Add to the "Agents" section:

```markdown
[`devops-engineer`](./agents/devops-engineer.md) by [YourGitHubUsername](https://github.com/yourusername)
Senior DevOps engineer specializing in infrastructure automation, CI/CD pipelines,
containerization with Docker/Kubernetes, and multi-cloud deployments. Provides
production-ready Infrastructure as Code with security and observability built in.
```

### 3. Commit and Push

```bash
git add agents/devops-engineer.md README.md
git commit -m "feat: add devops-engineer agent

Added comprehensive DevOps agent with expertise in:
- Infrastructure as Code (Terraform, CloudFormation)
- Container orchestration (Kubernetes, Docker)
- CI/CD pipeline design (GitHub Actions, GitLab CI)
- Cloud platforms (AWS, GCP, Azure)
- Monitoring and security best practices"

git push -u origin claude/your-branch-name
```

---

## Resources & References

### Claude Code Documentation
- [Sub-Agents Guide](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- [Claude Code Main Docs](https://docs.anthropic.com/en/docs/claude-code/)

### Related Repositories
- [Code By Agents](https://github.com/baryhuang/code-by-agents) - Orchestration framework
- [awesome-claude-agents](https://github.com/rahulvrane/awesome-claude-agents) - Similar collection
- [Claude Code Subagents Collection](https://github.com/wshobson/agents) - Extensive agent list

### External Agent Examples
- [react-coder](https://github.com/giselles-ai/giselle/blob/main/.claude/agents/react-coder.md)
- [ts-coder](https://github.com/giselles-ai/giselle/blob/main/.claude/agents/ts-coder.md)

---

## Questions & Support

**For Claude Code Help:**
- Run `/help` in Claude Code
- Visit [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code/)

**For Repository Issues:**
- Check existing issues at: https://github.com/hesreallyhim/awesome-claude-code-agents/issues
- Submit new issues with clear descriptions and examples

**For Contributions:**
- Follow the conventions outlined in this document
- Include agent file, examples, and something built with the agent
- Update README.md with your contribution
- Submit pull request with clear description

---

## Version History

- **2025-11-18:** Initial CLAUDE.md created with comprehensive structure and conventions
- **2024-07:** "Inevitable Code" sub-agents added by toyamarinyon
- **2024-07:** Initial 4 agents added by TheCookingSenpai
- **2024-07:** Repository created by Really Him

---

*This guide is maintained for AI assistants working with the awesome-claude-code-agents repository. Keep it updated as patterns and conventions evolve.*
