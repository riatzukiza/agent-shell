# Agent Shell

> Emacs-based agent shell for Agent Client Protocol (ACP) integration

## Overview

Agent Shell provides a native Emacs interface for interacting with LLM agents through the Agent Client Protocol (ACP). It enables seamless integration with multiple AI agents (Claude Code, Codex, Gemini CLI, Goose, Qwen Code) directly within Emacs.

## Key Features

- **Native Emacs Integration**: Built on comint-shell for authenticating Emacs experience
- **Multi-Agent Support**: Configurable support for Claude Code, OpenAI Codex, Google Gemini, Goose, and Qwen Code
- **Authentication Management**: Environment variable and API key management for each agent
- **Container Support**: Devcontainer integration for containerized development environments
- **ACP Protocol**: Full Agent Client Protocol implementation for standardized communication

## Build & Development Commands

```bash
# Run tests
make test

# Lint code
make lint

# Byte compile for performance
make compile

# Check documentation
make checkdoc
```

## Code Style

- **Elisp Patterns**: Use alists for data structures, seq.el for list operations
- **CL Integration**: Limit to `cl-defun` for named parameters and self-documenting functions
- **Map.el**: Use map.el for alist operations when possible
- **Consistency**: Follow existing patterns for new features
- **Testing**: Add tests for new functionality in `tests/` directory

## Agent Configuration

### Claude Code Integration
```elisp
(setq agent-shell-anthropic-authentication
      (agent-shell-anthropic-make-authentication :login t))
```

### OpenAI Codex Integration
```elisp
(setq agent-shell-openai-authentication
      (agent-shell-openai-make-authentication :login t))
```

### Environment Variables
```elisp
(setq agent-shell-anthropic-claude-environment
      (agent-shell-make-environment-variables
       "ANTHROPIC_API_KEY" (auth-source-pass-get "secret" "anthropic-api-key")
       "HTTPS_PROXY" "http://proxy.example.com:8080"))
```

## Cross-Repository Integration

### Related Tools
- **[clojure-mcp](../clojure-mcp/)**: MCP server implementation for protocol reference
- **[opencode-openai-codex-auth](../opencode-openai-codex-auth/)**: OAuth patterns for authentication
- **[promethean](../promethean/)**: Agent orchestration patterns

### 🔗 Comprehensive Cross-References
- **[CROSS_REFERENCES.md](./CROSS_REFERENCES.md)** - Complete cross-references to all related repositories
- **[Workspace AGENTS.md](../AGENTS.md)** - Main workspace documentation
- **[Repository Index](../REPOSITORY_INDEX.md)** - Complete repository overview

### Integration Patterns
1. **Protocol Development**: Use ACP implementation as reference for new agent protocols
2. **Authentication Flows**: OAuth and API key management patterns for other tools
3. **Multi-Agent Support**: Patterns for supporting multiple AI providers
4. **Container Integration**: Devcontainer patterns for development environments

## Development Workflow

1. **Feature Development**: Implement in agent-shell-*.el files
2. **Testing**: Add corresponding tests in tests/agent-shell-*-tests.el
3. **Documentation**: Update README.org and docstrings
4. **Integration**: Test with various agent providers

## File Structure

```
agent-shell.el                 # Main entry point
agent-shell-*.el              # Provider-specific implementations
tests/agent-shell-*-tests.el   # Test files
README.org                    # Main documentation
```

## Resources

- [Agent Client Protocol Specification](https://agentclientprotocol.com/)
- [Main Repository](https://github.com/riatzukiza/agent-shell)
- [ACP.el Implementation](https://github.com/xenodium/acp.el)

## Dependencies

- **shell-maker**: Comint-based shell framework (MELPA)
- **acp.el**: Agent Client Protocol implementation
- **Emacs 29+**: Required for latest features

## License

Same as main repository (check LICENSE file)