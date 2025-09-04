# Basic Commands

## Core Commands Overview

Amazon Q CLI provides essential commands for different workflows. Master these basics to unlock AI-assisted development.

## Primary Commands

### `q chat` - Interactive AI Assistant

Start an interactive conversation with Amazon Q:

```bash
# Start chat session
q chat

# Start with a question
q chat "Help me create a Python web application"

# Resume previous conversation
q chat --resume

# Use specific agent
q chat --agent my-agent

# Use specific model
q chat --model claude-3-sonnet
```

**Options:**
- `--resume` - Resume previous conversation from this directory
- `--agent <AGENT>` - Use specific context profile
- `--model <MODEL>` - Select AI model to use
- `--trust-all-tools` - Allow all tools without confirmation
- `--trust-tools <TOOLS>` - Trust specific tools only
- `--no-interactive` - Run without user input

**Chat Commands:**
- `/quit` - Exit chat session
- `/help` - Show available chat commands
- `/clear` - Clear conversation history
- `/context` - Manage conversation context

### Authentication Commands

**Note**: The Q CLI documentation shows `login` in development examples but does not document specific authentication commands with flags in the main help.

```bash
# Basic authentication
q login
```

### `q doctor` - System Diagnostics

Check your Q CLI installation and configuration:

```bash
q doctor
```

This command verifies:
- ✅ **Installation** - Q CLI is properly installed
- ✅ **Authentication** - Valid credentials are configured
- ✅ **Network** - Connection to AWS services
- ✅ **Permissions** - Required access levels

## All Available Commands

Based on `q --help-all`, here are all Q CLI commands:

### Core Commands
```bash
q chat           # AI assistant in terminal
q login          # Authenticate with AWS
q logout         # Sign out
q doctor         # Fix and diagnose issues
```

### System & Setup
```bash
q setup          # Setup CLI components
q update         # Update Amazon Q application
q diagnostic     # Run diagnostic tests
q init           # Generate shell dotfiles
q settings       # Customize appearance & behavior
```

### User & Profile
```bash
q whoami         # Show current user details
q profile        # Show profile information
```

### Desktop Integration
```bash
q launch         # Launch desktop app
q quit           # Quit desktop app
q restart        # Restart desktop app
q dashboard      # Open dashboard
```

### Advanced Features
```bash
q mcp            # Model Context Protocol
q agent          # Agent management
q integrations   # Manage system integrations
q translate      # Natural language to shell
q inline         # Inline shell completions
q theme          # Get or set theme
q issue          # Create GitHub issue
q debug          # Debug the app
```

## Chat Commands (In Session)

Based on actual Q CLI chat help, here are the verified commands:

### Essential Commands
```bash
/quit            # Quit the application
/help            # Print help message
/clear           # Clear conversation history
```

### Context & Session Management
```bash
/context         # Manage context files for chat session
  /context show    # Display context rules and matched files
  /context add     # Add context rules (filenames or glob patterns)
  /context remove  # Remove specified rules
  /context clear   # Remove all rules

/save            # Save the current conversation
/load            # Load a previous conversation
/compact         # Summarize conversation to free up context space
/usage           # Show current session's context window usage
```

### Productivity Features
```bash
/experiment      # Toggle experimental features
/todos           # View, manage, and resume to-do lists
/agent           # Manage agents
/model           # Select a model for current conversation session

# Knowledge Base (Beta - requires enabling)
/knowledge       # Manage knowledge base for persistent context
  /knowledge show    # Display knowledge base contents
  /knowledge add     # Add file or directory to knowledge base
  /knowledge remove  # Remove knowledge base entry by path
  /knowledge update  # Update file or directory in knowledge base
  /knowledge clear   # Remove all knowledge base entries
  /knowledge status  # Show background operation status
  /knowledge cancel  # Cancel background operation

# Tangent Mode (Experimental)
/tangent         # Create conversation checkpoint / restore from checkpoint
```

### Tools & Integration
```bash
/tools           # View tools and permissions
/mcp             # See MCP server loaded
/prompts         # View and retrieve prompts
/hooks           # View context hooks
```

### Utilities
```bash
/editor          # Open $EDITOR (defaults to vi) to compose a prompt
/issue           # Create a new Github issue or make a feature request
/subscribe       # Upgrade to Q Developer Pro subscription
```

**Note**: 
- `/execute_bash` is not a chat command. Use natural language: "run ls -la command"
- `/knowledge` requires enabling: `q settings chat.enableKnowledge true`
- `/tangent` is experimental and creates conversation checkpoints

## Command Verification

All commands listed here have been verified against the actual Q CLI help output. Commands that are not documented in the official Q CLI help are noted as such.

## Next Steps

Continue to [Chat Interface](../core-features/05-chat-interface.md) to learn about interactive conversations with Amazon Q CLI.
