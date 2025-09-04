# Session Management

## Overview

Session Management allows you to save and restore conversations, maintaining context across Q CLI sessions.

## Commands

### Terminal Commands
```bash
q save           # Save current conversation
q load           # Load previous conversation
```

### Chat Integration
Sessions are automatically managed within chat, allowing you to:
- **Resume conversations** - Continue where you left off
- **Maintain context** - Keep conversation history
- **Switch between topics** - Save and load different discussions

## How It Works

### Saving Conversations
- **Automatic context preservation** - Chat history and context maintained
- **Named sessions** - Organize conversations by topic or project
- **Cross-session continuity** - Resume complex discussions

### Loading Conversations
- **Restore full context** - Complete conversation history
- **Continue seamlessly** - Pick up where you stopped
- **Access previous insights** - Reference earlier solutions

## Usage Examples

### Basic Session Management
```bash
# Save current conversation
q save

# Load a previous conversation
q load

# In chat - conversations are automatically managed
# Context and history persist across sessions
```

### Project-Based Sessions
```bash
# Save work on specific project
q save  # When working on authentication feature

# Later, resume the same discussion
q load  # Continue authentication work with full context
```

### Context Preservation
- **File context** - Previously added files remain in context
- **Conversation history** - Full chat log preserved
- **Problem-solving state** - Continue complex debugging sessions

## Best Practices

### Effective Session Management
- **Save at logical breakpoints** - End of features, before switching topics
- **Use descriptive names** - If naming is supported, be specific
- **Regular saves** - Don't lose important conversations
- **Clean up old sessions** - Remove outdated conversations

### Workflow Integration
- **Project sessions** - One session per major project or feature
- **Learning sessions** - Save educational conversations for reference
- **Problem-solving** - Preserve debugging and troubleshooting context
- **Code reviews** - Maintain context during review discussions

### Context Management
- **Add relevant files** before saving - Use `/context add`
- **Document session purpose** - Note what the session covers
- **Link related sessions** - Reference connections between conversations

## Session Storage

- **Local storage** - Sessions saved on your machine
- **Privacy preserved** - No cloud synchronization
- **File-based** - Can be backed up with your data
- **Persistent** - Survives Q CLI updates and restarts

## Troubleshooting

### Save/Load Issues
```bash
# Check if commands are available
q help

# Verify Q CLI version supports session management
q --version

# Check file permissions in Q CLI directory
ls -la ~/.amazonq/
```

### Context Not Preserved
- **Re-add files** to context if needed: `/context add file.py`
- **Check conversation history** - Ensure full context loaded
- **Verify session integrity** - Some sessions may be corrupted

### Performance with Large Sessions
- **Monitor session size** - Large conversations may load slowly
- **Clean up context** - Remove unnecessary files from context
- **Start fresh sessions** - For new topics or projects

## Integration with Other Features

### With Knowledge Base
- **Save knowledge-enhanced sessions** - Conversations using knowledge base
- **Reference saved knowledge** - Use knowledge in loaded sessions
- **Maintain knowledge context** - Knowledge persists across sessions

### With Todo Lists
- **Session-specific todos** - Todos created in saved sessions
- **Resume todo work** - Continue task-focused conversations
- **Track progress** - See todo evolution across sessions

### With Thinking Mode
- **Preserve reasoning** - Complex thinking processes saved
- **Reference previous analysis** - Build on earlier reasoning
- **Learning continuity** - Maintain learning conversations

## Next Steps

- **[Back to Productivity Features](./09-productivity-features.md)**
- **[Knowledge Base](./09c-knowledge-base.md)** - Information storage
- **[Workflow Automation](./09e-workflow-automation.md)** - Advanced features
