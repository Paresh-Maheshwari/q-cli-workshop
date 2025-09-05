# Productivity Features

Amazon Q CLI includes built-in productivity features to enhance your development workflow and task management.

## 📋 Available Features

| Feature | Commands | Description | Details |
|---------|----------|-------------|---------|
| **Todo Lists** | `/todos` | Persistent task management and tracking | [Learn More →](./productivity-features/09a-todo-lists.md) |
| **Thinking Mode** | `/experiment` | Complex reasoning with step-by-step processes | [Learn More →](./productivity-features/09b-thinking-mode.md) |
| **Conversation Management** | `/save`, `/load` | Save and restore chat sessions | [Learn More →](./productivity-features/09d-session-management.md) |
| **Context Management** | `/context` | Manage files and directories in conversation context | [Learn More →](./productivity-features/09c-knowledge-base.md) |
| **Agents** | `/agent` | Specialized AI assistants with custom configurations | [Learn More →](./agents/agent-format.md) |

## 🚀 Quick Start

### Enable Features

```bash
# Enable productivity features
q settings chat.enableTodoList true
q settings chat.enableThinking true
q settings chat.enableTangentMode true

# Or enable via experiment menu
/experiment
# Select features to toggle on/off
```

### Basic Usage

```bash
# Todo management
/todos view          # View existing todo lists
/todos resume        # Resume work on a todo list

# Conversation features
/save               # Save current conversation
/load               # Load previous conversation

# Context management
/context            # Manage conversation context
/usage              # Show context window usage
```

## 📚 Feature Details

### [📋 Todo Lists](./productivity-features/09a-todo-lists.md)
Persistent task management with automatic creation, interactive selection, and progress tracking. Perfect for complex multi-step projects.

**Key Commands**: `/todos view`, `/todos resume`, `/todos clear-finished`

### [🧠 Thinking Mode](./productivity-features/09b-thinking-mode.md)
Shows Q's step-by-step reasoning process for complex problems. Helps understand how conclusions are reached and improves learning.

**Activation**: Enable via `/experiment` or `q settings chat.enableThinking true`

### [💬 Conversation Management](./productivity-features/09d-session-management.md)
Save and restore chat sessions to maintain continuity across work sessions. Includes conversation compaction for memory management.

**Key Commands**: `/save`, `/load`, `/compact`

### [📁 Context Management](./productivity-features/09c-knowledge-base.md)
Add files and directories to conversation context for better project understanding and more relevant assistance.

**Key Commands**: `/context`, `/hooks`, `/usage`

### [🤖 Agents](./agents/agent-format.md)
Create specialized AI assistants with custom configurations, tools, and behaviors for specific workflows.

**Key Commands**: `/agent`, custom agent configurations

## ⚙️ Configuration

### Key Settings

```bash
# Todo lists
q settings chat.enableTodoList true

# Thinking mode
q settings chat.enableThinking true

# Conversation management
q settings chat.disableAutoCompaction false
q settings chat.enableHistoryHints true
```

## 🎯 Best Practices

### Workflow Integration
- **Start with todo lists** for complex projects
- **Enable thinking mode** for problem-solving sessions
- **Save conversations** before major context changes
- **Manage context** to keep discussions relevant

### Productivity Tips
- Combine features for maximum efficiency
- Regular cleanup of completed todos
- Strategic use of conversation saves
- Context management for project awareness

## 🚀 Try It Yourself

**Quick Setup**: Enable and test productivity features:

```bash
# 1. Enable all features
q settings chat.enableTodoList true
q settings chat.enableThinking true
q settings chat.enableTangentMode true

# 2. Start a chat session
q chat

# 3. Test features
"Create a todo list for setting up a new project"
/todos view
/save
```

## 📚 Next Steps

**Explore Each Feature**:
- **[Todo Lists](./productivity-features/09a-todo-lists.md)** - Master task management
- **[Thinking Mode](./productivity-features/09b-thinking-mode.md)** - Understand complex reasoning
- **[Conversation Management](./productivity-features/09d-session-management.md)** - Maintain session continuity
- **[Context Management](./productivity-features/09c-knowledge-base.md)** - Optimize project assistance
- **[Agents](./agents/agent-format.md)** - Create specialized AI assistants

**Hands-on Projects**: Apply productivity features in real projects:
- **[Website Project](../projects/10-project-website.md)** - Build a responsive website
- **[Game Project](../projects/11-project-game.md)** - Create an interactive game

Continue to [Website Project](../projects/10-project-website.md) to apply these productivity features in a real project.
