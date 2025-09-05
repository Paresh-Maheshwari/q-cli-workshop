# Knowledge Base

## Overview

The Knowledge Base enables persistent context storage and retrieval across chat sessions with semantic search capabilities.

## Enable Knowledge Base

```bash
# In chat session
/experiment
# Select "Knowledge [ON]" from the interactive menu
```

## Commands

### Basic Operations
```bash
/knowledge add <path>        # Add files or directories
/knowledge show             # Display knowledge base contents
/knowledge remove <path>    # Remove entry by path
/knowledge update <path>    # Update existing entry
/knowledge clear            # Remove all entries
```

### Management
```bash
/knowledge status           # Show background operation status
/knowledge cancel           # Cancel background operation
```

## Features

### Semantic Search
- **Intelligent retrieval** - Find relevant information contextually
- **Cross-session persistence** - Knowledge survives chat restarts
- **File and directory support** - Index entire codebases
- **Text content storage** - Save important information

### Content Types
- **Source code files** - Index programming files
- **Documentation** - Store and search docs
- **Configuration files** - Keep settings accessible
- **Text snippets** - Save important notes

## Usage Examples

### Adding Content
```bash
# Add individual files
/knowledge add README.md
/knowledge add src/main.py

# Add entire directories
/knowledge add ./docs/
/knowledge add ./src/

# Add text content directly
"Save this API endpoint information to knowledge base"
```

### Searching Knowledge
```bash
# Search for specific topics
/knowledge search "authentication"
/knowledge search "database configuration"

# Browse all knowledge
/knowledge show

# Update existing knowledge
/knowledge update ./src/auth.py
```

### Integration with Chat
```bash
# Reference knowledge in conversations
"Based on my saved documentation, help me implement user authentication"

# Use knowledge for context
"Using the API patterns in my knowledge base, create a new endpoint"
```

## Settings

Configure knowledge base behavior:
```bash
q settings
```

Available settings:
- `chat.enableKnowledge` - Enable knowledge base functionality
- `knowledge.defaultIncludePatterns` - Default file patterns to include
- `knowledge.defaultExcludePatterns` - Default file patterns to exclude
- `knowledge.maxFiles` - Maximum number of files for indexing
- `knowledge.chunkSize` - Text chunk size for processing
- `knowledge.chunkOverlap` - Overlap between text chunks
- `knowledge.indexType` - Type of knowledge index to use

## Best Practices

### Effective Knowledge Management
- **Organize by project** - Keep related files together
- **Regular updates** - Refresh knowledge when files change
- **Descriptive searches** - Use specific terms for better results
- **Clean up regularly** - Remove outdated information

### Content Strategy
- **Include documentation** - README files, API docs, guides
- **Add configuration files** - Settings, environment configs
- **Store code patterns** - Reusable functions and classes
- **Save learning notes** - Important discoveries and solutions

### Performance Tips
- **Monitor file limits** - Check `knowledge.maxFiles` setting
- **Use include/exclude patterns** - Filter relevant content
- **Regular maintenance** - Clean up unused entries
- **Optimize chunk size** - Adjust for your content type

## Troubleshooting

### Knowledge Base Not Working
```bash
# Check if knowledge is enabled
/experiment
# Ensure "Knowledge [ON]" is selected

# Verify settings
q settings
# Check: chat.enableKnowledge = true
```

### Search Not Finding Content
```bash
# Check what's in knowledge base
/knowledge show

# Try different search terms
/knowledge search "exact phrase"
/knowledge search keyword

# Update stale content
/knowledge update <path>
```

### Performance Issues
```bash
# Check background operations
/knowledge status

# Cancel long-running operations
/knowledge cancel

# Clear and rebuild if needed
/knowledge clear
```

## Storage and Privacy

- **Local storage** - Knowledge base stored on your machine
- **No cloud sync** - Data remains private and local
- **File-based** - Can be backed up with your files
- **Session persistence** - Survives Q CLI restarts

## Next Steps

- **[Back to Productivity Features](../09-productivity-features.md)**
- **[Todo Lists](./09a-todo-lists.md)** - Task management
- **[Session Management](./09d-session-management.md)** - Conversation persistence
