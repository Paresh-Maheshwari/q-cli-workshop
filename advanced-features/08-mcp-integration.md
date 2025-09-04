# MCP Integration

## Model Context Protocol (MCP)

MCP enables Amazon Q CLI to connect with external tools and services, extending its capabilities beyond built-in features.

## AWS MCP Servers

AWS provides specialized MCP servers for enhanced cloud development. Visit [AWS MCP Documentation](https://awslabs.github.io/mcp/) for complete setup guides.

### Key AWS MCP Servers

**📚 Documentation & Knowledge**
- `aws-documentation-mcp-server` - Latest AWS docs and APIs
- `aws-knowledge-mcp-server` - Official AWS content and code samples

**🏗️ Infrastructure & Deployment**
- `aws-api-mcp-server` - AWS CLI commands integration
- `cdk-mcp-server` - AWS CDK development with security
- `terraform-mcp-server` - Terraform workflows with scanning
- `cfn-mcp-server` - CloudFormation resource management

**🤖 AI & Machine Learning**
- `bedrock-mcp-server` - Amazon Bedrock integration
- `lambda-tool-mcp-server` - Execute Lambda functions as tools

## Q CLI MCP Commands

### Terminal Commands

```bash
# List configured MCP servers
q mcp list

# Add a new MCP server
q mcp add --name <NAME> --command <COMMAND>

# Remove an MCP server
q mcp remove --name <NAME>

# Check server status
q mcp status --name <NAME>

# Import server configuration from file
q mcp import --file <FILE> [SCOPE]

# Get help with MCP commands
q mcp help
```

### Chat Commands

```bash
# View loaded MCP servers (in chat)
/mcp
```

## MCP Server Configuration

### Adding Servers

```bash
# Add a server with basic command
q mcp add --name "my-server" --command "python server.py"

# Add with arguments
q mcp add --name "git-server" --command "npx" --args "@modelcontextprotocol/server-git"

# Add with environment variables
q mcp add --name "aws-server" --command "uvx" --args "aws-mcp-server" --env "AWS_REGION=us-east-1"

# Add with custom timeout
q mcp add --name "slow-server" --command "python server.py" --timeout 10000

# Add to specific agent
q mcp add --name "project-server" --command "node server.js" --agent "my-agent"

# Add with different scopes
q mcp add --name "global-server" --command "server" --scope global
q mcp add --name "workspace-server" --command "server" --scope workspace
```

### Importing Configurations

```bash
# Import server configuration from file
q mcp import --file servers.json

# Import with specific scope
q mcp import --file servers.json default
q mcp import --file servers.json workspace  
q mcp import --file servers.json global

# Force overwrite existing servers
q mcp import --file servers.json --force

# Import with scope and force
q mcp import --file servers.json global --force
```

### Managing Servers

```bash
# List all configured servers
q mcp list

# Check if a server is running
q mcp status --name "my-server"

# Remove a server
q mcp remove --name "my-server"

# Remove from specific agent
q mcp remove --name "project-server" --agent "my-agent"

# Force overwrite existing server
q mcp add --name "existing-server" --command "new-command" --force
```

## Configuration Examples

### AWS Knowledge MCP Server

Configuration format:

```json
{
  "mcpServers": {
    "aws-knowledge-mcp-server": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://knowledge-mcp.global.api.aws"
      ]
    }
  }
}
```

Add using command line:
```bash
# Add AWS Knowledge MCP server
q mcp add --name "aws-knowledge-mcp-server" \
  --command "npx" \
  --args "mcp-remote" \
  --args "https://knowledge-mcp.global.api.aws"

# Expected output:
# ✓ Added MCP server 'aws-knowledge-mcp-server' to global config in /home/kali/.aws/amazonq/mcp.json
```

**Configuration Location:**
- Global: `~/.aws/amazonq/mcp.json`
- Workspace: `.amazonq/mcp.json`
- Agent-specific: `.amazonq/cli-agents/<agent-name>.json`

**Features:**
- Real-time AWS documentation access
- API references and best practices
- Latest AWS announcements
- Architectural guidance

**Tools:**
- `search_documentation` - Search AWS docs
- `read_documentation` - Get AWS docs as markdown
- `recommend` - Get content recommendations

## Setup Example: AWS Knowledge MCP Server

### Installation
```bash
# Install AWS Knowledge MCP Server (remote server)
# Follow setup guide: https://awslabs.github.io/mcp/servers/aws-knowledge-mcp-server
```

**Features:**
- Real-time AWS documentation access
- API references and best practices
- Latest AWS announcements
- Architectural guidance

**Tools:**
- `search_documentation` - Search AWS docs
- `read_documentation` - Get AWS docs as markdown
- `recommend` - Get content recommendations

### Agent Configuration
```json
{
  "allowedTools": [
    "@aws-knowledge/search_documentation",
    "@aws-knowledge/read_documentation"
  ]
}
```

## Setup Example: Frontend MCP Server

### Installation
```bash
# Install Frontend MCP Server
uvx awslabs.frontend-mcp-server@latest
```

**Features:**
- Modern React application guidance
- AWS Amplify authentication
- Tailwind CSS and shadcn/ui setup
- React Router implementation
- Component development with AWS integrations

**Tools:**
- `GetReactDocsByTopic` - React development guidance

### Agent Configuration
```json
{
  "allowedTools": [
    "@frontend/GetReactDocsByTopic"
  ]
}
```

## Setup Resources

- **AWS MCP Documentation**: https://awslabs.github.io/mcp/
- **MCP Protocol**: https://modelcontextprotocol.io/
- **Server Installation**: Follow AWS MCP setup guides for specific servers

## Next Steps

Continue to [Productivity Features](./09-productivity-features.md) for todo lists and workflows.
