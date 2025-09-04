# Thinking Mode

## Overview

Thinking Mode enables complex reasoning with step-by-step thought processes, showing Q CLI's internal reasoning for better transparency and learning.

## Enable Thinking Mode

```bash
# In chat session
/experiment
# Select "Thinking [ON]" from the interactive menu
```

## How It Works

When enabled, Q CLI shows its reasoning process for complex problems:
- **Transparent reasoning** - See how conclusions are reached
- **Step-by-step analysis** - Break down complex problems
- **Learning tool** - Understand AI decision-making
- **Debugging aid** - Identify reasoning errors

## When Thinking Mode Activates

Thinking mode automatically engages for:
- **Complex problem-solving** - Multi-step technical challenges
- **Code analysis** - Understanding complex codebases
- **Architecture decisions** - System design choices
- **Debugging sessions** - Root cause analysis
- **Multi-step reasoning** - Tasks requiring sequential logic

## Benefits

### For Learning
- **Understand AI reasoning** - See how problems are approached
- **Learn problem-solving patterns** - Adopt effective strategies
- **Identify knowledge gaps** - Spot areas for improvement
- **Debug your own thinking** - Compare approaches

### for Development
- **Better code reviews** - Understand analysis depth
- **Architecture insights** - See design considerations
- **Debugging assistance** - Follow logical troubleshooting
- **Decision validation** - Verify reasoning paths

## Settings

Configure thinking mode:
```bash
q settings
# Look for: chat.enableThinking - Enable thinking tool for complex reasoning (boolean)
```

## Usage Examples

### Complex Code Analysis
```
User: "Help me optimize this database query performance"

🤔 Thinking: Let me analyze this query step by step:
1. First, I'll examine the query structure and identify potential bottlenecks
2. Check for missing indexes on frequently queried columns
3. Look for N+1 query patterns or unnecessary joins
4. Consider query execution plan optimization
5. Evaluate caching opportunities

Based on my analysis, here are the optimization opportunities...
```

### Architecture Decisions
```
User: "Should I use microservices or monolith for this project?"

🤔 Thinking: This requires evaluating multiple factors:
1. Team size and experience with distributed systems
2. Expected scale and traffic patterns
3. Deployment and operational complexity
4. Development velocity requirements
5. Data consistency needs

Considering these factors for your specific context...
```

## Best Practices

### When to Use
- **Enable for complex tasks** - Architecture, debugging, analysis
- **Disable for simple queries** - Basic information requests
- **Learning sessions** - When you want to understand reasoning
- **Code reviews** - To see detailed analysis

### Maximizing Value
- **Ask follow-up questions** about the reasoning process
- **Challenge assumptions** shown in the thinking
- **Learn patterns** from repeated reasoning approaches
- **Apply insights** to your own problem-solving

## Troubleshooting

### Not Seeing Thinking Output
```bash
# Check if thinking mode is enabled
/experiment
# Ensure "Thinking [ON]" is selected

# Verify settings
q settings
# Check: chat.enableThinking = true
```

### Thinking Mode Not Activating
- **Try more complex questions** - Simple queries may not trigger thinking
- **Ask multi-step problems** - Requires sequential reasoning
- **Request analysis** - "Analyze this code and explain your reasoning"

## Next Steps

- **[Back to Productivity Features](./09-productivity-features.md)**
- **[Todo Lists](./09a-todo-lists.md)** - Task management
- **[Knowledge Base](./09c-knowledge-base.md)** - Information storage
