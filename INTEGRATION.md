# BMAD-METHOD™ Integration Guide for SuperClaude Environment

## Repository Overview

**BMAD-METHOD™** is a Universal AI Agent Framework that provides:
- **Agentic Planning**: Specialized AI agents for planning and architecture
- **Context-Engineered Development**: Comprehensive story files with full context
- **Domain Expansion**: Works beyond software development (creative writing, business, wellness)

## Key Components

### Core Structure (`~/motodev/ai-tools/BMAD-METHOD/`)
```
bmad-core/
├── agents/          # AI agent definitions (Analyst, PM, Architect, Dev, QA, etc.)
├── agent-teams/     # Pre-configured team compositions
├── checklists/      # Quality and process checklists
├── tasks/           # Task templates and workflows
├── templates/       # Document templates (PRD, Architecture, etc.)
└── workflows/       # Structured workflow definitions

tools/
├── cli.js           # Command-line interface
├── installer/       # Installation tools
├── builders/        # Build and bundle tools
└── flattener/       # Agent bundling tools

expansion-packs/     # Domain-specific extensions
dist/               # Pre-built bundles
docs/               # Comprehensive documentation
```

## Integration Points with SuperClaude

### 1. Enhanced Agent System
BMAD agents can complement SuperClaude personas:
- **BMAD Agents**: Analyst, PM, Architect, Dev, QA, Scrum Master
- **SuperClaude Personas**: 11 specialized personas (architect, frontend, backend, etc.)
- **Integration**: Use BMAD for structured planning, SuperClaude for execution

### 2. Workflow Enhancement
```yaml
Combined Workflow:
  Planning Phase (BMAD):
    - Use Analyst agent for requirements gathering
    - Use PM agent for PRD creation
    - Use Architect agent for technical design
  
  Execution Phase (SuperClaude):
    - Use appropriate personas for implementation
    - Leverage MCP servers for enhanced capabilities
    - Apply SuperClaude commands and flags
```

### 3. Command Integration
```bash
# Install BMAD in a project
npx bmad-method install

# Use with SuperClaude commands
/analyze --with-bmad     # Combine analysis approaches
/build --bmad-planning   # Use BMAD planning before build
/task --bmad-stories     # Generate BMAD story files
```

### 4. MCP Server Compatibility
BMAD can work alongside existing MCP servers:
- **Sequential**: For complex BMAD workflow analysis
- **Context7**: For documentation patterns in BMAD agents
- **Magic**: For UI components in BMAD-generated specs
- **Serena**: For symbol operations in BMAD architecture docs

## Installation & Setup

### Quick Installation
```bash
# Install globally
cd ~/motodev/ai-tools/BMAD-METHOD
npm install

# Or install in specific project
cd ~/motodev/projects/[project-name]
npx bmad-method install
```

### Creating Custom Agents
1. Navigate to `bmad-core/agents/`
2. Copy an existing agent as template
3. Modify for your domain/needs
4. Bundle with flattener tools

### Using Pre-built Teams
```bash
# Web UI approach (Gemini/ChatGPT)
cp dist/teams/team-fullstack.txt ~/your-project/
# Upload to AI and configure

# IDE approach
npx bmad-method install
# Agents available in .bmad/ directory
```

## Workflow Examples

### Example 1: Full Stack Development
```yaml
1. Planning (BMAD):
   - *analyst: Create project brief
   - *pm: Generate PRD from brief
   - *architect: Design technical architecture
   
2. Development (SuperClaude):
   - /build --frontend: Implement UI components
   - /build --backend: Create API endpoints
   - /test: Run comprehensive tests
```

### Example 2: Creative Writing Project
```yaml
1. Ideation (BMAD Expansion Pack):
   - Use creative writing agents
   - Generate story outlines
   
2. Execution (SuperClaude):
   - Use scribe persona for writing
   - Apply /document for formatting
```

## Best Practices

### When to Use BMAD
✅ **Use BMAD for:**
- Initial project planning and requirements gathering
- Creating comprehensive PRDs and architecture docs
- Structured agile workflow with story files
- Domain-specific tasks with expansion packs
- Team-based AI agent collaboration

### When to Use SuperClaude
✅ **Use SuperClaude for:**
- Code implementation and optimization
- Real-time analysis and debugging
- MCP server integration tasks
- Performance optimization
- Cross-tool orchestration

### Combined Approach
```yaml
Optimal Workflow:
  1. Start with BMAD planning agents
  2. Generate PRD and Architecture
  3. Create story files with BMAD
  4. Switch to SuperClaude for implementation
  5. Use appropriate personas and MCP servers
  6. Apply quality gates and validation
```

## Configuration

### Environment Variables
```bash
# Add to ~/.bashrc or ~/.zshrc
export BMAD_HOME="$HOME/motodev/ai-tools/BMAD-METHOD"
export PATH="$PATH:$BMAD_HOME/tools"

# Optional: Set default team
export BMAD_DEFAULT_TEAM="fullstack"
```

### Integration with Claude Config
Add to `~/.claude/CLAUDE.md`:
```markdown
## BMAD-METHOD Integration
- Location: ~/motodev/ai-tools/BMAD-METHOD
- Use for: Planning, PRD generation, story creation
- Commands: See INTEGRATION.md for combined workflows
```

## Advanced Integration

### Custom Expansion Packs
Create domain-specific agents that work with SuperClaude:
```javascript
// expansion-packs/my-domain/agent-custom.md
module.exports = {
  name: 'Custom Agent',
  integration: {
    superClaude: {
      personas: ['architect', 'analyzer'],
      mcpServers: ['sequential', 'context7'],
      commands: ['/analyze', '/build']
    }
  }
  // ... agent definition
}
```

### Hybrid Commands
Create aliases that combine both systems:
```bash
# Add to ~/.bashrc
alias plan-project='npx bmad-method plan && /analyze --comprehensive'
alias build-with-bmad='npx bmad-method generate-stories && /build --from-stories'
```

## Troubleshooting

### Common Issues
1. **Node Version**: Requires Node.js v20+
2. **Path Issues**: Ensure BMAD_HOME is set correctly
3. **Permission Issues**: Check file permissions in bmad-core/

### Debug Mode
```bash
# Enable verbose output
export BMAD_DEBUG=true
npx bmad-method install --verbose
```

## Resources

### Documentation
- [BMAD User Guide](docs/user-guide.md)
- [Core Architecture](docs/core-architecture.md)
- [Expansion Packs Guide](docs/expansion-packs.md)
- [SuperClaude Docs](~/.claude/)

### Support
- BMAD Discord: https://discord.gg/gk8jAdXWmj
- GitHub Issues: https://github.com/bmadcode/bmad-method/issues
- SuperClaude Context: Available in current environment

## Summary

BMAD-METHOD provides structured AI agent collaboration that complements SuperClaude's execution capabilities. Use BMAD for planning and documentation generation, then leverage SuperClaude's powerful personas and MCP servers for implementation. The combination creates a comprehensive AI-assisted development environment that covers the entire software lifecycle from ideation to deployment.

---
*Integration guide created for dtaylor's environment - September 2025*