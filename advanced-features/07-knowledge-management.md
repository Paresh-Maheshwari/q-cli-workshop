# Knowledge Management

## Personal Knowledge Base

Build and maintain your personal knowledge repository for quick access to information, code snippets, and documentation across chat sessions.

![Knowledge Management Overview](../images/knowledge-overview.svg)

## 🚀 Enable Knowledge Base

First, enable the knowledge feature:

```bash
# Enable knowledge feature (required)
q settings chat.enableKnowledge true

# Or enable via experiment
/experiment
# Select "Knowledge" to toggle on
```

## 📚 Knowledge Commands

Once enabled, use these commands in chat sessions:

```bash
# Display knowledge base contents
/knowledge show

# Add files or directories to knowledge base
/knowledge add <path>

# Remove knowledge base entry by path
/knowledge remove <path>

# Update existing file or directory in knowledge base
/knowledge update <path>

# Remove all knowledge base entries
/knowledge clear

# Show background operation status
/knowledge status

# Cancel background operations
/knowledge cancel

# Get help with knowledge commands
/knowledge help
```

## 📁 Adding Knowledge

### Add Files and Directories

```bash
# Add individual files
/knowledge add package.json
/knowledge add src/app.py
/knowledge add README.md

# Add entire directories
/knowledge add ./docs/
/knowledge add ./src/
/knowledge add ./config/

# Add files with relative paths
/knowledge add ../shared/utils.js
```

### What Gets Indexed

The knowledge base automatically indexes:
- **File contents** - Text, code, documentation
- **Directory structures** - File organization and relationships
- **Metadata** - File types, sizes, modification dates

## 🔍 Using Knowledge in Conversations

### Natural Language Queries

Once files are added, reference them naturally in conversations:

```bash
# Reference specific files
"Based on my package.json, what dependencies should I update?"

# Ask about project structure
"Looking at my src directory, how should I organize these components?"

# Get contextual help
"Using my existing config files, help me set up a new environment"

# Code analysis
"Review my app.py file and suggest improvements"
```

### Semantic Search

The knowledge base provides intelligent search across your indexed content:

```bash
# Ask about concepts
"What authentication methods do I use in my projects?"

# Find similar patterns
"Show me examples of error handling from my codebase"

# Get project insights
"What databases am I using across my projects?"
```

## 🔧 Managing Your Knowledge Base

### View Current Contents

```bash
# See what's in your knowledge base
/knowledge show

# Check indexing status
/knowledge status
```

### Update and Maintain

```bash
# Update files after changes
/knowledge update src/app.py

# Update entire directories
/knowledge update ./docs/

# Remove outdated entries
/knowledge remove old-project/

# Start fresh if needed
/knowledge clear
```

### Background Operations

```bash
# Check if indexing is in progress
/knowledge status

# Cancel long-running operations
/knowledge cancel
```

## 💡 Best Practices

### ✅ Effective Knowledge Management

- **Add project roots** - Include main directories for full context
- **Update regularly** - Keep knowledge base current with `/knowledge update`
- **Use descriptive queries** - Be specific about what you're looking for
- **Clean up periodically** - Remove outdated projects with `/knowledge remove`

### 🎯 Strategic Usage

- **Project onboarding** - Add new project files to understand structure
- **Code reviews** - Reference existing patterns and standards
- **Documentation** - Include README files and documentation
- **Configuration** - Add config files for environment setup help

## 🔒 Privacy and Storage

### Local Storage
- Knowledge base is stored locally on your machine
- Files are indexed but not uploaded to external services
- Semantic search happens locally for privacy

### Data Management
- Use `/knowledge clear` to remove all data
- Individual entries removed with `/knowledge remove`
- No automatic cleanup - you control what's stored

## 🚀 Try It Yourself

**Interactive Exercise**: Set up your first knowledge base:

```bash
# 1. Enable knowledge
q settings chat.enableKnowledge true

# 2. Start a chat session
q chat

# 3. Add some files
/knowledge add README.md
/knowledge add package.json

# 4. View your knowledge base
/knowledge show

# 5. Ask a question about your files
"What does my README say about installation?"
```

## 📚 Next Steps

**Advanced Features**: Explore more Q CLI capabilities:
- **MCP Integration** → [Module 8](./08-mcp-integration.md)
- **Productivity Features** → [Module 9](./09-productivity-features.md)
- **Project Workflows** → [Module 10](../projects/10-project-website.md)

Continue to [MCP Integration](./08-mcp-integration.md) to learn about extending Q CLI with external tools and services.
