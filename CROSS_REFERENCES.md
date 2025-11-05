# Agent Shell Cross-Reference Documentation

> Emacs-based agent shell for Agent Client Protocol (ACP) integration with comprehensive repository cross-references

## 🔗 Repository Cross-References

This document provides comprehensive cross-references to all related repositories in the agent development ecosystem, enabling agents to navigate between related tools, protocols, and integration patterns seamlessly.

### 🏗️ Development Infrastructure Dependencies

#### **Agent Development & Orchestration**
- **[promethean](https://github.com/riatzukiza/promethean)** - Local LLM enhancement system and autonomous agent framework
  - [AGENTS.md](https://github.com/riatzukiza/promethean/blob/main/AGENTS.md)
  - [CROSS_REFERENCES.md](https://github.com/riatzukiza/promethean/blob/main/CROSS_REFERENCES.md)
  - [README.md](https://github.com/riatzukiza/promethean/blob/main/README.md)
  - **Integration**: Use Promethean agents as targets for Agent Shell ACP protocol testing

#### **MCP Protocol Integration**
- **[clojure-mcp](https://github.com/bhauman/clojure-mcp)** - MCP server for Clojure REPL-driven development
  - [AGENTS.md](https://github.com/bhauman/clojure-mcp/blob/main/AGENTS.md)
  - [README.md](https://github.com/bhauman/clojure-mcp/blob/main/README.md)
  - **Integration**: Protocol reference for Agent Client Protocol implementation

### 🔧 Authentication & Security Dependencies

#### **OAuth Authentication Patterns**
- **[opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth)** - OpenAI Codex OAuth authentication plugin
  - [AGENTS.md](https://github.com/numman-ali/opencode-openai-codex-auth/blob/main/AGENTS.md)
  - [README.md](https://github.com/numman-ali/opencode-openai-codex-auth/blob/main/README.md)
  - **Integration**: OAuth flow patterns for OpenAI Codex integration in Agent Shell

#### **TypeScript SDK Integration**
- **[moofone/codex-ts-sdk](https://github.com/moofone/codex-ts-sdk)** - TypeScript SDK for OpenAI Codex with cloud tasks
  - [AGENTS.md](https://github.com/moofone/codex-ts-sdk/blob/main/AGENTS.md)
  - [README.md](https://github.com/moofone/codex-ts-sdk/blob/main/README.md)
  - **Integration**: TypeScript authentication patterns for cross-language compatibility

### 🌐 Web & Frontend Integration

#### **OpenCode Development**
- **[stt](https://github.com/riatzukiza/devel/tree/main/stt)** - Multiple opencode development branches and experiments
  - [AGENTS.md](https://github.com/riatzukiza/devel/blob/main/stt/AGENTS.md)
  - [CROSS_REFERENCES.md](https://github.com/riatzukiza/devel/blob/main/stt/CROSS_REFERENCES.md)
  - **Integration**: Web-based agent interfaces for Agent Shell testing

- **[opencode-hub](https://github.com/riatzukiza/devel/tree/main/opencode-hub)** - Centralized opencode coordination and distribution
  - [AGENTS.md](https://github.com/riatzukiza/devel/blob/main/opencode-hub/AGENTS.md)
  - [README.md](https://github.com/riatzukiza/devel/blob/main/opencode-hub/README.md)
  - **Integration**: Package management for Agent Shell plugins

#### **Full-Stack Applications**
- **[riatzukiza/openhax](https://github.com/riatzukiza/openhax)** - Full-stack application with Reactant + Fastify
  - [AGENTS.md](https://github.com/riatzukiza/openhax/blob/main/AGENTS.md)
  - **Integration**: Full-stack patterns for agent-based applications

### ⚙️ Configuration & Environment

#### **System Configuration**
- **[dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles)** - System configuration and environment setup
  - [AGENTS.md](https://github.com/riatzukiza/devel/blob/main/dotfiles/.config/opencode/AGENTS.md)
  - **Integration**: Emacs configuration and environment setup for Agent Shell

### 🔌 Runtime & Performance

#### **Rust-Based Runtime**
- **[openai/codex](https://github.com/openai/codex)** - Rust-based Codex CLI and runtime
  - [AGENTS.md](https://github.com/openai/codex/blob/main/AGENTS.md)
  - [README.md](https://github.com/openai/codex/blob/main/README.md)
  - **Integration**: High-performance runtime for Agent Shell agent connections

## 🔄 Agent Shell Integration Patterns

### **ACP Protocol Implementation**
#### **Protocol Reference Integration**
- **MCP Server**: Use [clojure-mcp](https://github.com/bhauman/clojure-mcp) as protocol reference
- **Agent Targets**: Connect to [promethean](https://github.com/riatzukiza/promethean) agents via ACP
- **Testing**: Validate protocol compliance across different agent implementations

#### **Protocol Development Workflow**
```bash
# Protocol reference implementation
cd ../clojure-mcp && pnpm install && pnpm test

# Agent Shell ACP testing
emacs agent-shell.el
M-x agent-shell-start-with-agent promethean-agent

# Cross-protocol testing
cd ../promethean && pnpm --filter @promethean-os/agent test
```

### **Authentication Integration**
#### **OAuth Pattern Integration**
- **OpenAI Codex**: Use [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) OAuth patterns
- **TypeScript SDK**: Integrate with [moofone/codex-ts-sdk](https://github.com/moofone/codex-ts-sdk) authentication
- **Cross-Language**: Ensure authentication compatibility between Elisp and TypeScript

#### **Authentication Development**
```bash
# OAuth pattern development
cd ../opencode-openai-codex-auth
pnpm build && pnpm test

# TypeScript SDK integration
cd ../moofone/codex-ts-sdk
pnpm build && cp dist/* ../agent-shell/auth/

# Agent Shell authentication testing
emacs agent-shell-openai.el
M-x agent-shell-openai-test-authentication
```

### **Multi-Agent Support Integration**
#### **Agent Provider Integration**
- **Promethean Agents**: Connect to [promethean](https://github.com/riatzukiza/promethean) autonomous agents
- **OpenCode Agents**: Test with [stt](https://github.com/riatzukiza/devel/tree/main/stt) development agents
- **Clojure Agents**: Integrate with [clojure-mcp](https://github.com/bhauman/clojure-mcp) REPL agents

#### **Multi-Agent Testing**
```bash
# Start multiple agent environments
cd ../promethean && pnpm --filter @promethean-os/agent start
cd ../clojure-mcp && pnpm start
cd ../stt/opencode && bun dev

# Agent Shell multi-agent testing
emacs agent-shell.el
M-x agent-shell-start-session promethean
M-x agent-shell-start-session clojure-mcp
M-x agent-shell-start-session opencode
```

### **Container Integration**
#### **Devcontainer Patterns**
- **Environment Setup**: Use [dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles) for container configuration
- **Multi-Repo**: Containerized development with all dependencies
- **Testing**: Isolated testing environments for each agent provider

#### **Container Development**
```bash
# Container environment setup
cd ../dotfiles && ./.setup/devcontainer.sh

# Multi-repo container development
docker-compose up -d  # Includes agent-shell, promethean, clojure-mcp

# Container testing
emacs agent-shell.el
M-x agent-shell-test-in-container
```

## 🔄 Cross-Repository Development Workflows

### **Protocol Development Workflow**
1. **Reference Implementation**: Study [clojure-mcp](https://github.com/bhauman/clojure-mcp) MCP implementation
2. **Agent Shell Implementation**: Implement ACP protocol in Elisp
3. **Agent Integration**: Connect to [promethean](https://github.com/riatzukiza/promethean) agents
4. **Testing**: Cross-protocol compliance testing

### **Authentication Development Workflow**
1. **Pattern Study**: Analyze [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) OAuth patterns
2. **Cross-Language Integration**: Ensure compatibility with [moofone/codex-ts-sdk](https://github.com/moofone/codex-ts-sdk)
3. **Agent Shell Implementation**: Implement authentication in Elisp
4. **Testing**: Multi-provider authentication testing

### **Multi-Agent Workflow**
1. **Agent Development**: Develop agents in [promethean](https://github.com/riatzukiza/promethean)
2. **Protocol Integration**: Connect via Agent Shell ACP protocol
3. **Testing**: Multi-agent session testing
4. **Documentation**: Update cross-references

## 📋 Quick Reference Commands

### **Cross-Repository Development**
```bash
# Full agent development environment
cd ../promethean && pnpm build
cd ../clojure-mcp && pnpm install
cd ../opencode-openai-codex-auth && pnpm build
cd ../moofone/codex-ts-sdk && pnpm build

# Agent Shell development
emacs agent-shell.el
M-x agent-shell-test-all-providers
```

### **Integration Testing**
```bash
# Protocol compliance testing
cd ../clojure-mcp && pnpm test --protocol
cd ../promethean && pnpm --filter @promethean-os/agent test --acp

# Authentication testing
cd ../opencode-openai-codex-auth && pnpm test --oauth
cd ../moofone/codex-ts-sdk && pnpm test --auth

# Agent Shell integration
make test  # Agent Shell tests
```

### **Container Development**
```bash
# Containerized development
cd ../dotfiles && ./setup-container.sh
docker-compose up -d

# Container testing
emacs agent-shell.el
M-x agent-shell-container-test
```

## 🎯 Decision Trees for Agents

### **Choosing Integration Target**
- **Protocol development?** → [clojure-mcp](https://github.com/bhauman/clojure-mcp) for reference + [promethean](https://github.com/riatzukiza/promethean) for agents
- **Authentication development?** → [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) + [moofone/codex-ts-sdk](https://github.com/moofone/codex-ts-sdk)
- **Multi-agent testing?** → All agent repositories for comprehensive testing
- **Container development?** → [dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles) + all repositories

### **Integration Complexity**
- **Simple**: Agent Shell + single agent provider
- **Medium**: Agent Shell + multiple providers + authentication
- **Complex**: Full ecosystem integration with containers and cross-protocol testing

## 📚 Additional Documentation

- **[Workspace Documentation](https://github.com/riatzukiza/devel/blob/main/AGENTS.md)** - Main workspace coordination
- **[Repository Index](https://github.com/riatzukiza/devel/blob/main/REPOSITORY_INDEX.md)** - Complete repository overview
- **[Git Submodules Documentation](https://github.com/riatzukiza/devel/blob/main/docs/reports/research/git-submodules-documentation.md)** - Technical submodule details
- **[Promethean Cross-References](https://github.com/riatzukiza/promethean/blob/main/CROSS_REFERENCES.md)** - Agent framework integration
- **[STT Cross-References](https://github.com/riatzukiza/devel/blob/main/stt/CROSS_REFERENCES.md)** - OpenCode development integration

## 🌐 External Resources

- **[Agent Client Protocol Specification](https://agentclientprotocol.com/)** - Official ACP protocol documentation
- **[ACP.el Implementation](https://github.com/xenodium/acp.el)** - Reference ACP implementation
- **[Main Repository](https://github.com/riatzukiza/agent-shell)** - Agent Shell source code

---

## License

Same as main repository (check LICENSE file)