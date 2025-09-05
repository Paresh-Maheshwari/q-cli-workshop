# Todo Lists

## Overview

Amazon Q CLI provides built-in todo list functionality for task management and tracking multi-step workflows.

## Commands

### Terminal Command
```bash
# View, manage, and resume to-do lists
q todos
```

### Chat Command
```bash
# Access todo functionality in chat
/todos
# Interactive menu for managing todo lists
```

## Enable Todo Lists

```bash
# Enable via experiments
/experiment
# Select "Todo Lists [ON]" from the menu
```

## How It Works

- **Storage**: Lists stored locally in `.amazonq/cli-todo-lists/`
- **Built-in Tool**: Uses `todo_list` tool for creating and managing tasks
- **Integration**: Works within chat sessions for task tracking

## Usage Examples

### In Chat Session
```bash
# Access todo management
/todos

# Ask Q CLI to create todos from conversations
"Add a todo to optimize the database queries"
"Create a task to review the authentication code"
```

### Task Tracking
- Create todos from natural language requests
- Track multi-step development tasks
- Resume work on specific todos
- Manage task priorities and status

## Settings

Configure todo functionality:
```bash
q settings
# Look for: chat.enableTodoList - Enable the todo list feature (boolean)
```

## Best Practices

### Effective Todo Management
- **Be specific** with task descriptions
- **Break down** complex tasks into smaller steps
- **Use natural language** when asking Q CLI to create todos
- **Regular review** of pending tasks

### Integration Tips
- Reference todos in conversations: "Help me work on todo #3"
- Create todos during problem-solving sessions
- Use todos to track learning objectives
- Link todos to specific code files or projects

## Troubleshooting

### Common Issues
```bash
# Todo lists not working
/experiment
# Ensure "Todo Lists" is enabled

# Check settings
q settings
# Verify chat.enableTodoList is true
```

### Storage Location
- **Local storage**: `.amazonq/cli-todo-lists/`
- **Backup**: Consider backing up todo files
- **Sync**: Todo lists are local to each machine

## Next Steps

- **[Back to Productivity Features](../09-productivity-features.md)**
- **[Thinking Mode](./09b-thinking-mode.md)** - Advanced reasoning
- **[Knowledge Base](./09c-knowledge-base.md)** - Information storage
