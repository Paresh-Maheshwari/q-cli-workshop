# Basic Commands

## Core Commands Overview

Amazon Q CLI provides several essential commands for different workflows. Master these basics to unlock the full potential of AI-assisted development.

## Primary Commands

### `q chat` - Interactive AI Assistant

Start an interactive conversation with Amazon Q:

```bash
# Start chat session
q chat
```

### `q login` - Authentication

```bash
# Login to Amazon Q
q login
```

### `q logout` - Sign Out

```bash
# Logout from Amazon Q
q logout
```

### `q doctor` - System Diagnostics

Check your Q CLI installation and configuration:

```bash
# System check and fix common issues
q doctor
```

### `q translate` - Natural Language to Shell

Convert natural language to shell commands:

```bash
# Translate natural language to shell commands
q translate
```

## Additional Commands

### `q settings` - Configuration

```bash
# Customize appearance and behavior
q settings
```

### `q whoami` - User Information

```bash
# Show current user details
q whoami
```

### `q update` - Update CLI

```bash
# Update Amazon Q CLI
q update
```

## Working with Amazon Q Chat

### Starting a Chat Session

```bash
# Start interactive chat
q chat
```

### Basic Chat Usage

```bash
# Ask questions about code
"Help me optimize this Python function"

# Get AWS guidance
"How do I create an S3 bucket with versioning?"

# Request code examples
"Show me a Terraform configuration for an EC2 instance"
```

## Command Options and Flags

### Global Options

```bash
# Show version
q --version

# Show help
q --help

# Show help for all subcommands
q --help-all

# Increase logging verbosity
q --verbose
```

### Chat-Specific Commands

Once in a chat session (`q chat`), you have access to these commands:

```bash
# Exit chat session
/quit

# Show available chat commands
/help

# Clear conversation history
/clear

# Manage conversation context
/context

# List available tools and permissions
/tools

# Manage agents
/agent

# Open editor to compose prompts
/editor

# Summarize conversation to free up context space
/compact

# Create GitHub issues or feature requests
/issue

# View and retrieve prompts
/prompts

# View context hooks
/hooks

# Show current session's context window usage
/usage

# See loaded MCP servers
/mcp

# Select a model for the conversation session
/model

# Toggle experimental features
/experiment

# Upgrade to Q Developer Pro subscription
/subscribe

# Save the current conversation
/save

# Load a previous conversation
/load

# View, manage, and resume to-do lists
/todos
```

### Keyboard Shortcuts

```bash
# Execute command in current session
!{command}

# Insert new-line for multi-line prompt
Ctrl + j  (or Alt + Enter)

# Fuzzy search commands and context files
Ctrl + s

# Toggle tangent mode for isolated conversations
Ctrl + t
```

## Best Practices

### Effective Communication

**Be Specific:**
```bash
# Good
"Help me optimize this Python function for better performance"

# Better  
"This Python function processes 10k records and takes 30 seconds. Help me optimize it for better performance"
```

### Workflow Integration

**Start with Diagnostics:**
```bash
q doctor  # Always check system health first
```

**Use Natural Language Translation:**
```bash
q translate  # Convert natural language to shell commands
```

## Common Use Cases

### Getting Help
```bash
# Check system status
q doctor

# Get user information
q whoami

# Update the CLI
q update
```

### Code Assistance
```bash
# Start chat for code help
q chat
"Review this code for security vulnerabilities"
```

### Learning AWS
```bash
# Ask about AWS services
q chat
"Explain how AWS Lambda works with examples"
"Show me best practices for Docker containers"
```

### Shell Commands
```bash
# Convert natural language to commands
q translate
"list all files modified in the last 24 hours"
```

## Next Steps

Now that you understand the basic commands, let's explore the [chat interface](./05-chat-interface.md) in more detail.

---

**Estimated Time:** 15 minutes  
**Prerequisites:** Completed authentication setup
