# How to Use Claude-Flow with Claude Code: Complete Workflow Guide

> **Transform your development workflow** by integrating claude-flow's AI orchestration into any project with Claude Code

---

## 🎯 What You'll Learn

This guide shows you how to:
- Set up claude-flow with Claude Code (5 minutes)
- Use natural language skills (no commands to memorize!)
- Apply it to ANY project type (frontend, backend, fullstack, mobile, etc.)
- Leverage advanced features (memory, hooks, swarms)
- Optimize your specific workflow

---

## ⚡ Quick Setup (5 Minutes)

### Step 1: Add MCP Server to Claude Code

Claude-Flow integrates with Claude Code through the Model Context Protocol (MCP). This gives Claude access to 100+ orchestration tools.

```bash
# Add claude-flow MCP server (REQUIRED)
claude mcp add claude-flow npx claude-flow@alpha mcp start

# Optional: Add enhanced coordination features
claude mcp add ruv-swarm npx ruv-swarm mcp start

# Optional: Add cloud features (sandboxes, templates)
claude mcp add flow-nexus npx flow-nexus@latest mcp start
```

**What this does:**
- Installs claude-flow as an MCP server
- Makes 100+ AI orchestration tools available to Claude
- Enables swarm coordination, memory systems, and automation

### Step 2: Install Skills in Any Project

Navigate to your project directory and initialize:

```bash
# Option A: Standard setup (recommended for most projects)
cd /path/to/your/project
npx claude-flow@alpha init --force

# Option B: Enterprise setup (complex projects, teams)
npx claude-flow@alpha init --enterprise

# Option C: Specific methodology (SPARC TDD workflow)
npx claude-flow@alpha init --sparc
```

**What this creates:**
```
your-project/
├── .claude/
│   ├── skills/          ← 25 AI skills (auto-activated by context)
│   ├── commands/        ← Legacy slash commands (optional)
│   └── hooks/           ← Automation hooks (auto-formatting, etc.)
├── .swarm/
│   └── memory.db        ← Persistent AI memory (ReasoningBank)
└── CLAUDE.md            ← Claude Code configuration
```

### Step 3: Verify Setup

```bash
# Check that MCP server is running
claude mcp list
# Should show: claude-flow ✓

# Test a simple skill activation
# Open Claude Code and say:
# "Let's pair program on this feature"
# The pair-programming skill should activate automatically!
```

---

## 🎨 Understanding the Skills System

### The Magic: Natural Language Activation

**No commands to memorize!** Just describe what you want in natural language, and claude-flow activates the right skills automatically.

| You Say | Skill Activated | What Happens |
|---------|----------------|--------------|
| "Build a login feature with tests" | `sparc-methodology` | SPARC TDD workflow: Spec → Pseudocode → Architecture → Refine → Complete |
| "Let's pair program this" | `pair-programming` | Driver/navigator mode with real-time quality checks |
| "Review this PR for security" | `github-code-review` | Comprehensive review with security scanning |
| "Find similar code patterns" | `agentdb-vector-search` | Semantic code search (96-164x faster) |
| "Create a swarm to build an API" | `swarm-orchestration` | Multi-agent coordination with specialized workers |
| "Optimize this function" | `performance-analysis` | Bottleneck detection and optimization |
| "Set up automated formatting" | `hooks-automation` | Pre/post hooks for auto-formatting |

### Available Skills (25 Total)

**Development & Methodology (5 skills):**
- `sparc-methodology` - Structured development workflow
- `pair-programming` - Driver/navigator collaboration
- `skill-builder` - Create custom skills
- `verification-quality` - Truth scoring & validation
- `stream-chain` - Multi-agent pipelines

**Intelligence & Memory (6 skills):**
- `agentdb-vector-search` - Semantic code search (150x faster)
- `agentdb-memory-patterns` - Persistent AI memory
- `agentdb-learning` - 9 reinforcement learning algorithms
- `agentdb-optimization` - Memory quantization (4-32x reduction)
- `agentdb-advanced` - Multi-database management
- `reasoningbank-agentdb` - Adaptive learning patterns

**Swarm Coordination (3 skills):**
- `swarm-orchestration` - Multi-agent coordination
- `swarm-advanced` - Research, development, testing swarms
- `hive-mind-advanced` - Queen-led collective intelligence

**GitHub Integration (5 skills):**
- `github-code-review` - AI-powered code review
- `github-workflow-automation` - CI/CD pipeline creation
- `github-release-management` - Automated releases
- `github-project-management` - Issue tracking & sprint planning
- `github-multi-repo` - Cross-repository coordination

**Automation & Quality (4 skills):**
- `hooks-automation` - Pre/post operation hooks
- `performance-analysis` - Performance monitoring
- `reasoningbank-intelligence` - Adaptive learning
- `verification-quality` - Quality assurance

**Cloud & Platform (2 skills):**
- `flow-nexus-platform` - Cloud sandboxes & deployment
- `flow-nexus-neural` - Distributed neural training

---

## 🚀 Workflow Examples by Project Type

### Frontend Project (React, Vue, Angular)

**Scenario:** Building a dashboard with authentication

```bash
# 1. Initialize in your frontend project
cd my-react-app
npx claude-flow@alpha init --force

# 2. Open Claude Code and say:
"Build a user dashboard with authentication using SPARC methodology.
Include:
- Login/signup components
- Protected routes
- User profile page
- Data visualization charts
- Unit tests with 90% coverage"

# What happens automatically:
✓ SPARC skill activates
✓ Specification agent analyzes requirements
✓ Architecture agent designs component structure
✓ Coder agent implements React components
✓ Tester agent writes Jest/RTL tests
✓ Reviewer agent checks code quality
✓ All work coordinated through memory system
```

**Skills used:**
- `sparc-methodology` (TDD workflow)
- `swarm-orchestration` (parallel development)
- `agentdb-memory-patterns` (shared context)

### Backend Project (Node.js, Python, Go)

**Scenario:** Building a REST API with database

```bash
# 1. Initialize in your backend project
cd my-api
npx claude-flow@alpha init --enterprise

# 2. Say to Claude:
"Create a REST API for a blog platform with:
- User authentication (JWT)
- CRUD endpoints for posts and comments
- PostgreSQL database with migrations
- OpenAPI documentation
- Integration tests
- Docker setup"

# What happens:
✓ Backend-dev agent designs API structure
✓ Database agent creates schema and migrations
✓ Coder agent implements endpoints
✓ API-docs agent generates OpenAPI spec
✓ Tester agent writes integration tests
✓ DevOps agent creates Dockerfile
✓ Security agent reviews authentication
```

**Skills used:**
- `sparc-methodology` (structured approach)
- `swarm-orchestration` (specialized agents)
- `verification-quality` (security checks)

### Full-Stack Project (MERN, Django+React, etc.)

**Scenario:** Building a complete application

```bash
# 1. Initialize at project root
cd fullstack-app
npx claude-flow@alpha init --enterprise

# 2. Say to Claude:
"Build a task management app with:
- React frontend (TypeScript)
- Node.js/Express backend
- MongoDB database
- Real-time updates (WebSocket)
- User authentication
- Responsive design
- Full test coverage
- CI/CD pipeline"

# What happens:
✓ System-architect agent designs full architecture
✓ Backend team (3 agents) builds API + database
✓ Frontend team (2 agents) creates React UI
✓ Tester team (2 agents) writes comprehensive tests
✓ DevOps agent sets up CI/CD
✓ All coordinated via hive-mind system
```

**Skills used:**
- `hive-mind-advanced` (queen-led coordination)
- `swarm-orchestration` (team coordination)
- `github-workflow-automation` (CI/CD)
- `agentdb-memory-patterns` (shared knowledge)

### Mobile Project (React Native, Flutter)

**Scenario:** Building a mobile app

```bash
# 1. Initialize in mobile project
cd my-mobile-app
npx claude-flow@alpha init

# 2. Say to Claude:
"Build a fitness tracking mobile app with:
- Cross-platform (iOS + Android)
- User onboarding
- Activity tracking screens
- Data visualization
- Local storage (SQLite)
- Push notifications
- E2E tests with Detox"

# What happens:
✓ Mobile-dev agent creates app structure
✓ UI agent designs screens and navigation
✓ Database agent implements local storage
✓ Tester agent writes E2E tests
✓ Platform-specific optimizations handled automatically
```

**Skills used:**
- `sparc-methodology`
- `swarm-orchestration`
- Mobile-specific agents

### Data Science / ML Project

**Scenario:** Building a machine learning pipeline

```bash
# 1. Initialize ML project
cd ml-project
npx claude-flow@alpha init

# 2. Say to Claude:
"Create a sentiment analysis pipeline with:
- Data preprocessing (pandas)
- Feature engineering
- Model training (scikit-learn)
- Hyperparameter tuning
- Model evaluation
- API deployment (FastAPI)
- Monitoring dashboard"

# What happens:
✓ ML-developer agent designs pipeline
✓ Data agent handles preprocessing
✓ Neural agent trains models
✓ Backend-dev agent creates API
✓ Monitor agent sets up metrics
```

**Skills used:**
- `flow-nexus-neural` (distributed training)
- `sparc-methodology`
- `performance-analysis`

### Legacy Codebase (Refactoring & Modernization)

**Scenario:** Improving an existing codebase

```bash
# 1. Initialize in existing project
cd legacy-app
npx claude-flow@alpha init --force

# 2. Say to Claude:
"Analyze this codebase and help me:
- Identify performance bottlenecks
- Refactor to modern patterns
- Add missing tests
- Improve error handling
- Update dependencies
- Add TypeScript types"

# What happens:
✓ Code-analyzer agent scans codebase
✓ Performance-analysis skill identifies bottlenecks
✓ Refactoring agents suggest improvements
✓ Tester agents add missing tests
✓ All changes tracked in memory for context
```

**Skills used:**
- `performance-analysis` (bottleneck detection)
- `agentdb-vector-search` (code pattern matching)
- `verification-quality` (quality checks)

---

## 🧠 Leveraging the Memory System

### What is Persistent Memory?

Claude-flow includes **ReasoningBank** - a SQLite-backed memory system that persists across sessions. Unlike regular Claude conversations that forget context, ReasoningBank remembers:

- Project decisions and rationale
- Code patterns and conventions
- Team preferences
- Previous solutions to similar problems

### How to Use Memory

**Storing Information:**
```bash
# Store a decision
npx claude-flow@alpha memory store \
  --key "project/auth/strategy" \
  --value "Using JWT with refresh tokens for auth" \
  --namespace "decisions"

# Store a pattern
npx claude-flow@alpha memory store \
  --key "code/patterns/error-handling" \
  --value "All async functions use try-catch with custom error classes" \
  --namespace "conventions"
```

**Or use natural language with Claude:**
```
You: "Remember that we decided to use JWT authentication with refresh tokens"
Claude: "✓ Stored in memory under decisions/auth/strategy"

You: "What did we decide about authentication?"
Claude: "According to memory, you're using JWT authentication with refresh tokens"
```

**Semantic Search (with AgentDB):**
```bash
# Find similar code patterns
npx claude-flow@alpha memory search "error handling" --semantic

# Results are ranked by similarity (cosine distance)
# Returns relevant patterns even if exact keywords don't match
```

**Memory Benefits:**
- **Context Preservation:** Resume work weeks later with full context
- **Team Knowledge:** Share decisions across team members
- **Pattern Learning:** AI learns from previous solutions
- **Fast Retrieval:** 2-3ms query time (150x faster with AgentDB)

### Memory in Practice

**Example 1: API Development**
```
Session 1 (Monday):
You: "Build user authentication API"
Claude: [Creates auth system, stores patterns in memory]

Session 2 (Friday):
You: "Now add admin authentication"
Claude: "I remember you used JWT with refresh tokens.
        I'll follow the same pattern for consistency."
        [Retrieves from memory, applies consistent approach]
```

**Example 2: Code Standards**
```
You: "Remember: we use functional components, hooks,
      and TypeScript strict mode for React"

[Stored in memory]

Later:
Claude: [Automatically follows these conventions in all React code]
```

---

## 🪝 Automation with Hooks

### What are Hooks?

Hooks are automatic actions triggered by events. They run **before** or **after** operations without manual intervention.

### Built-in Hooks

**Pre-Operation Hooks:**
- `pre-task` - Before starting a task
- `pre-edit` - Before modifying files
- `pre-command` - Before running commands
- `pre-search` - Before searching code

**Post-Operation Hooks:**
- `post-edit` - After modifying files (auto-format!)
- `post-task` - After completing tasks (run tests!)
- `post-command` - After running commands
- `post-commit` - After git commits

**Session Hooks:**
- `session-start` - When starting work
- `session-end` - When finishing work
- `session-restore` - When resuming work

### Example: Auto-Format on Save

```bash
# Enable automatic formatting after edits
npx claude-flow@alpha hooks enable --name format-on-save

# Configure for your language
cat > .claude/hooks/post-edit.sh << 'EOF'
#!/bin/bash
FILE=$1

# Format based on file type
case "$FILE" in
  *.js|*.jsx|*.ts|*.tsx)
    npx prettier --write "$FILE"
    ;;
  *.py)
    black "$FILE"
    ;;
  *.go)
    go fmt "$FILE"
    ;;
esac
EOF

chmod +x .claude/hooks/post-edit.sh
```

**Result:** Every file Claude edits is automatically formatted!

### Example: Run Tests After Changes

```bash
# Auto-run tests after code changes
cat > .claude/hooks/post-task.sh << 'EOF'
#!/bin/bash
TASK=$1

# Run tests after implementation tasks
if [[ "$TASK" == *"implement"* ]] || [[ "$TASK" == *"code"* ]]; then
  npm test
fi
EOF

chmod +x .claude/hooks/post-task.sh
```

**Result:** Tests run automatically after coding tasks!

### Example: Store Decisions in Memory

```bash
# Auto-save important decisions
cat > .claude/hooks/session-end.sh << 'EOF'
#!/bin/bash

# Generate session summary
SUMMARY=$(npx claude-flow@alpha session summary --format json)

# Store in memory
npx claude-flow@alpha memory store \
  --key "sessions/$(date +%Y%m%d)" \
  --value "$SUMMARY" \
  --namespace "history"

echo "✓ Session saved to memory"
EOF

chmod +x .claude/hooks/session-end.sh
```

**Result:** Every session is automatically documented in memory!

---

## 💡 Best Practices & Tips

### 1. Start Simple, Scale Up

```bash
# Week 1: Basic usage
npx claude-flow@alpha init
# Just use natural language, let skills activate automatically

# Week 2: Add memory
"Remember to use TypeScript strict mode in this project"

# Week 3: Enable hooks
npx claude-flow@alpha hooks enable --name auto-format

# Week 4: Advanced swarms
"Create a swarm with 5 specialized agents to build this feature"
```

### 2. Use Skills, Not Commands

❌ **Don't memorize commands:**
```bash
/sparc tdd "feature"
/swarm init --topology mesh
/memory store key value
```

✅ **Just talk naturally:**
```
"Build a user login feature with TDD"
"Create a team of agents to build an API"
"Remember that we use React hooks, not class components"
```

### 3. Leverage Memory for Context

**Good memory keys:**
```
decisions/architecture/database → "PostgreSQL with Prisma ORM"
conventions/code/naming → "camelCase for variables, PascalCase for components"
patterns/auth/jwt → "15min access token, 7day refresh token"
team/preferences/testing → "Jest with React Testing Library"
```

**Bad memory keys:**
```
stuff/1 → "some data"
temp → "temporary info"
x → "important thing"
```

### 4. Combine Skills for Power

Skills work together! Example:

```
You: "Build a complete e-commerce API with:
- Structured development approach
- Multiple specialized agents
- Comprehensive testing
- Performance optimization
- GitHub Actions CI/CD"

Skills activated automatically:
✓ sparc-methodology (structured approach)
✓ swarm-orchestration (agent coordination)
✓ verification-quality (testing)
✓ performance-analysis (optimization)
✓ github-workflow-automation (CI/CD)
```

### 5. Use Hive-Mind for Complex Projects

For projects with 10+ tasks or multiple subsystems:

```bash
# Initialize with hive-mind
npx claude-flow@alpha init --enterprise

# Then say:
"Create a hive-mind to build a social media platform with:
- User service (auth, profiles)
- Post service (CRUD, feed)
- Notification service (real-time)
- Media service (image uploads)
- Frontend web app
- Mobile app
All with full test coverage and CI/CD"

# What happens:
✓ Queen agent coordinates overall strategy
✓ 6 specialized teams (1 per service + 2 for UIs)
✓ Each team has workers (coder, tester, reviewer)
✓ Shared memory for cross-team knowledge
✓ Automated testing and deployment
```

### 6. Monitor Performance

```bash
# Check swarm status
npx claude-flow@alpha swarm status

# View memory usage
npx claude-flow@alpha memory stats

# Analyze performance
npx claude-flow@alpha benchmark run

# View agent metrics
npx claude-flow@alpha agent metrics
```

### 7. Version Control Integration

```bash
# Add to .gitignore
echo ".swarm/" >> .gitignore  # Memory DB (optional - can commit for team sharing)

# Commit claude-flow configuration
git add .claude/ CLAUDE.md
git commit -m "Add claude-flow configuration"

# Team members can now use the same setup
git clone repo
npx claude-flow@alpha init  # Uses committed config
```

---

## 🔧 Advanced Features

### Multi-Agent Swarms

For complex tasks, spawn multiple specialized agents:

```
You: "Create a swarm to build a payment processing system with:
- Backend API (Node.js)
- Database schema (PostgreSQL)
- Integration tests
- Security audit
- API documentation
- Deployment scripts"

Claude spawns:
✓ Backend-dev agent → Builds API
✓ Database agent → Designs schema
✓ Tester agent → Writes tests
✓ Security agent → Audits code
✓ API-docs agent → Generates docs
✓ DevOps agent → Creates deployment

All working in parallel, coordinated through memory!
```

### AgentDB (96-164x Faster Search)

Enable semantic vector search for large codebases:

```bash
# Install AgentDB (optional dependency)
npm install agentdb

# Initialize in project
npx claude-flow@alpha init --agentdb

# Now use semantic search
"Find all functions similar to this authentication logic"
"Show me code that handles file uploads"
"What patterns do we use for error handling?"

# Results are semantically ranked, not keyword-matched!
```

### GitHub Integration

Automate GitHub workflows:

```
"Review PR #42 for security vulnerabilities and performance issues"
→ github-code-review skill activates

"Create a release workflow that:
- Runs tests
- Builds artifacts
- Creates GitHub release
- Deploys to production"
→ github-workflow-automation skill activates

"Synchronize these 3 repositories:
- api-service
- web-client
- mobile-app
Keep dependencies aligned and run cross-repo tests"
→ github-multi-repo skill activates
```

### Cloud Execution (Flow-Nexus)

Run AI agents in cloud sandboxes:

```bash
# Optional: Install Flow-Nexus
claude mcp add flow-nexus npx flow-nexus@latest mcp start

# Register account
npx flow-nexus@latest register

# Use cloud features
"Deploy this swarm to Flow-Nexus cloud and run tests in E2B sandbox"
→ flow-nexus-platform skill activates
```

---

## 🎓 Learning Path

### Beginner (Week 1)

**Focus:** Basic setup and natural language skills

1. Install MCP server: `claude mcp add claude-flow npx claude-flow@alpha mcp start`
2. Initialize in a project: `npx claude-flow@alpha init`
3. Try simple tasks: "Build a todo list API with tests"
4. Let skills activate automatically

**Skills to explore:**
- `sparc-methodology`
- `pair-programming`

### Intermediate (Week 2-3)

**Focus:** Memory and automation

1. Start using memory: "Remember we use async/await, not promises"
2. Enable hooks: `npx claude-flow@alpha hooks enable --name auto-format`
3. Try swarms: "Create a team to build this feature"

**Skills to explore:**
- `swarm-orchestration`
- `hooks-automation`
- `agentdb-memory-patterns`

### Advanced (Week 4+)

**Focus:** Complex coordination and optimization

1. Use hive-mind for multi-service projects
2. Enable semantic search with AgentDB
3. Integrate GitHub automation
4. Create custom skills

**Skills to explore:**
- `hive-mind-advanced`
- `agentdb-vector-search`
- `github-workflow-automation`
- `performance-analysis`

---

## 🆘 Troubleshooting

### MCP Server Not Found

```bash
# Check if server is running
claude mcp list

# If not listed, add it
claude mcp add claude-flow npx claude-flow@alpha mcp start

# Restart Claude Code
```

### Skills Not Activating

```bash
# Verify skills are installed
ls .claude/skills/

# If missing, reinitialize
npx claude-flow@alpha init --force

# Check Claude can see skills
# Say: "List available skills"
```

### Memory Not Persisting

```bash
# Check memory database exists
ls .swarm/memory.db

# If missing, initialize
npx claude-flow@alpha memory init

# Verify it works
npx claude-flow@alpha memory store --key test --value "works"
npx claude-flow@alpha memory search test
```

### Hooks Not Running

```bash
# Verify hooks are executable
chmod +x .claude/hooks/*.sh

# Test a hook manually
.claude/hooks/post-edit.sh test.js

# Check hook configuration
cat .claude/hooks/config.yaml
```

### Performance Issues

```bash
# Clear memory cache
npx claude-flow@alpha memory clear --cache-only

# Optimize database
npx claude-flow@alpha memory optimize

# Consider AgentDB for large projects
npm install agentdb
npx claude-flow@alpha init --agentdb
```

---

## 📚 Additional Resources

**Documentation:**
- [Main README](../README.md) - Overview and features
- [Skills Tutorial](./guides/skills-tutorial.md) - Deep dive into skills
- [Memory System](./MEMORY-SYSTEM.md) - Memory architecture
- [Beginner's Guide](./REPO-ANALYSIS-BEGINNER-GUIDE.md) - Repository analysis

**Examples:**
- [REST API Examples](../examples/05-swarm-apps/) - Real-world APIs
- [Workflow Examples](../examples/02-workflows/) - Common patterns
- [SPARC Examples](../examples/06-tutorials/sparc/) - TDD workflows

**Community:**
- GitHub Issues: https://github.com/ruvnet/claude-flow/issues
- Documentation: https://github.com/ruvnet/claude-flow/tree/main/docs

---

## 🎉 Conclusion

**You now have everything you need to supercharge your Claude Code workflow!**

**Remember the key principles:**

1. **Skills over Commands** - Just talk naturally, let skills activate
2. **Memory is Power** - Store context, never lose decisions
3. **Automate with Hooks** - Set it and forget it
4. **Scale with Swarms** - Multiple agents = parallel work
5. **Start Simple** - You don't need all features on day 1

**Your First Steps:**

```bash
# 1. Add MCP server
claude mcp add claude-flow npx claude-flow@alpha mcp start

# 2. Initialize your project
cd your-project
npx claude-flow@alpha init

# 3. Start coding naturally
# Open Claude Code and say:
# "Build a REST API for a todo app with tests"
```

**That's it!** Claude-flow will orchestrate specialized agents, manage memory, and coordinate everything automatically.

Welcome to the future of AI-assisted development! 🚀

---

*Last Updated: 2025-10-30*
*Claude-Flow Version: 2.7.15*
