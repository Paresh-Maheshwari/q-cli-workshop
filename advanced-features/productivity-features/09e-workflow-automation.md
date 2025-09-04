# Workflow Automation

## Overview

Advanced productivity features including Tangent Mode, keyboard shortcuts, and workflow optimization tools.

## Tangent Mode

### Enable Tangent Mode
```bash
# In chat session
/experiment
# Select "Tangent Mode [ON]" from the menu
```

### Usage
```bash
# Toggle tangent mode on/off
/tangent

# Or use keyboard shortcut (default: Ctrl+T)
```

### How It Works
- **Conversation checkpoints** - Save current discussion state
- **Explore side topics** - Branch into related discussions
- **Return to main thread** - Resume original conversation
- **Context preservation** - Maintain both main and tangent contexts

### Benefits
- **Non-disruptive exploration** - Investigate related topics without losing main thread
- **Better focus** - Keep main conversation on track
- **Learning enhancement** - Explore concepts without derailing progress
- **Problem-solving** - Investigate multiple solution paths

## Keyboard Shortcuts

### Available Shortcuts
```bash
# Fuzzy search (default: Ctrl+S)
# Quick command access

# Tangent mode toggle (default: Ctrl+T)
# When tangent mode is enabled
```

### Configuration
```bash
q settings
```

Shortcut settings:
- `chat.skimCommandKey` - Fuzzy search key binding (single character)
- `chat.tangentModeKey` - Tangent mode key binding (single character, default: 't')

## Advanced Chat Features

### Fuzzy Search
- **Quick command access** - Use Ctrl+S for command search
- **Experiment commands** - Search `/experiment`, `/knowledge`
- **Fast navigation** - Find commands without typing full names

### Edit Mode
```bash
q settings
# chat.editMode - Enable edit mode for chat interface (boolean)
```

### Notifications
```bash
q settings
# chat.enableNotifications - Enable desktop notifications (boolean)
```

## Workflow Optimization

### Conversation Management
```bash
# Compact conversations to free up context space
/compact

# Check context window usage
/usage

# Clear conversation history
/clear
```

### Context Hooks
```bash
# View context hooks
/hooks

# Hooks can automate context management
# Based on file changes or directory navigation
```

### Auto-Compaction
```bash
q settings
# chat.disableAutoCompaction - Disable automatic conversation summarization (boolean)
```

## Integration Features

### Agent Management
```bash
# Manage agents from terminal
q agent

# Agents can automate workflows and provide specialized assistance
```

### Model Selection
```bash
# Select model for current conversation
/model

# Configure default model
q settings
# chat.defaultModel - Default AI model for conversations (string)
```

### Prompt Management
```bash
# View and retrieve prompts
/prompts

# Standardize common requests and workflows
```

## Settings Overview

### Productivity Settings
```bash
q settings
```

Key workflow settings:
- `chat.enableHistoryHints` - Show conversation history hints
- `chat.greeting.enabled` - Show greeting message on chat start
- `api.timeout` - API request timeout in seconds
- `chat.disableMarkdownRendering` - Disable markdown formatting

### Tangent Mode Settings
- `chat.enableTangentMode` - Enable/disable tangent mode feature
- `chat.tangentModeKey` - Keyboard shortcut key
- `introspect.tangentMode` - Auto-enter tangent mode for introspect questions

## Best Practices

### Effective Tangent Mode Usage
- **Use for exploration** - Investigate related concepts
- **Return to main thread** - Don't lose original discussion
- **Document insights** - Note important discoveries from tangents
- **Limit tangent depth** - Avoid too many nested tangents

### Workflow Optimization
- **Customize shortcuts** - Set comfortable key bindings
- **Use auto-compaction** - Keep conversations manageable
- **Regular cleanup** - Clear old conversations
- **Context management** - Add/remove files as needed

### Agent Integration
- **Project-specific agents** - Configure agents for different workflows
- **Tool permissions** - Set appropriate access levels
- **Workflow automation** - Use agents for repetitive tasks

## Troubleshooting

### Tangent Mode Issues
```bash
# Check if tangent mode is enabled
/experiment
# Ensure "Tangent Mode [ON]"

# Verify keyboard shortcut
q settings
# Check chat.tangentModeKey setting
```

### Keyboard Shortcuts Not Working
```bash
# Check key bindings
q settings
# Verify chat.skimCommandKey and chat.tangentModeKey

# Test in different terminal environments
# Some terminals may intercept certain key combinations
```

### Performance Issues
```bash
# Check conversation size
/usage

# Compact if needed
/compact

# Clear history if necessary
/clear
```

## Next Steps

- **[Back to Productivity Features](./09-productivity-features.md)**
- **[Session Management](./09d-session-management.md)** - Conversation persistence
- **[Project 1: Website](./10-project-website.md)** - Apply productivity features in practice
