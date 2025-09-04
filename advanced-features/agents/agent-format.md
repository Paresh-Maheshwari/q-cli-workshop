# Agent Format

## Overview

Agent configuration files are JSON files that define specialized AI assistants with specific tools, resources, and behaviors.

## Basic Structure

```json
{
  "name": "aws-expert",
  "description": "An agent specialized for AWS infrastructure tasks",
  "prompt": "You are an expert AWS infrastructure specialist",
  "tools": ["fs_read", "fs_write", "execute_bash"],
  "allowedTools": ["fs_read"],
  "resources": ["file://README.md"]
}
```

## Configuration Fields

### Core Fields
- `name` - Agent identifier (optional, uses filename if not specified)
- `description` - Human-readable description of agent purpose
- `prompt` - System prompt providing high-level context

### Tool Configuration
- `tools` - Available tools for the agent
- `allowedTools` - Tools that can be used without prompting
- `toolsSettings` - Configuration for specific tools
- `toolAliases` - Tool name remapping for naming collisions

### Integration
- `mcpServers` - MCP servers the agent has access to
- `resources` - Resources available to the agent
- `hooks` - Commands run at specific trigger points

## Example Configurations

### Development Agent
```json
{
  "name": "dev-assistant",
  "description": "General development helper",
  "tools": ["fs_read", "fs_write", "execute_bash"],
  "allowedTools": ["fs_read"],
  "toolsSettings": {
    "fs_write": {
      "allowedPaths": ["./src/**", "./docs/**"]
    }
  }
}
```

### AWS Specialist
```json
{
  "name": "aws-expert", 
  "description": "AWS infrastructure specialist",
  "prompt": "You are an expert in AWS services and best practices",
  "tools": ["use_aws", "fs_read"],
  "toolsSettings": {
    "use_aws": {
      "allowedServices": ["ec2", "s3", "lambda"]
    }
  }
}
```

## File Locations

### Local Agents
```
.amazonq/cli-agents/
├── dev-agent.json
└── aws-specialist.json
```

### Global Agents
```
~/.aws/amazonq/cli-agents/
├── general-assistant.json
└── code-reviewer.json
```

## Next Steps

- **[Back to Advanced Features](../09-productivity-features.md)**
- **[Agent File Locations](./agent-locations.md)**
- **[Default Agent Behavior](./default-behavior.md)**
