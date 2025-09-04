# Agent File Locations

## Overview

Agent configuration files can be placed in two locations for workspace-specific or user-wide availability.

## Local Agents (Workspace-Specific)

**Location:** `.amazonq/cli-agents/`

```
my-project/
├── .amazonq/
│   └── cli-agents/
│       ├── dev-agent.json
│       └── aws-specialist.json
└── src/
    └── main.py
```

**Characteristics:**
- Project-specific configurations
- Only available in current directory and subdirectories
- Perfect for team sharing via version control

## Global Agents (User-Wide)

**Location:** `~/.aws/amazonq/cli-agents/`

```
~/.aws/amazonq/cli-agents/
├── general-assistant.json
├── code-reviewer.json
└── documentation-writer.json
```

**Characteristics:**
- Available from any directory
- Personal productivity agents
- Cross-project functionality

## Agent Precedence

1. **Local first** - Checks `.amazonq/cli-agents/` in current directory
2. **Global fallback** - Checks `~/.aws/amazonq/cli-agents/` in home directory

### Naming Conflicts
If both locations have agents with the same name:
```
WARNING: Agent conflict for my-agent. Using workspace version.
```

## Best Practices

### Use Local Agents For:
- Project-specific configurations
- Team collaboration
- Development environment requirements
- Specialized project tools

### Use Global Agents For:
- General-purpose assistants
- Personal productivity tools
- Cross-project workflows
- Common development patterns

## Example Usage

### Create Local Agent
```bash
mkdir -p .amazonq/cli-agents
cat > .amazonq/cli-agents/project-helper.json << 'EOF'
{
  "description": "Helper for this specific project",
  "tools": ["fs_read", "fs_write", "execute_bash"],
  "resources": ["file://README.md"]
}
EOF
```

### Create Global Agent
```bash
mkdir -p ~/.aws/amazonq/cli-agents
cat > ~/.aws/amazonq/cli-agents/general-helper.json << 'EOF'
{
  "description": "General purpose assistant",
  "tools": ["*"],
  "allowedTools": ["fs_read"]
}
EOF
```

## Directory Creation

- **Global directory** - Automatically created by Q CLI
- **Local directory** - Must be manually created in workspace

## Next Steps

- **[Back to Advanced Features](../09-productivity-features.md)**
- **[Agent Format](./agent-format.md)**
- **[Default Agent Behavior](./default-behavior.md)**
