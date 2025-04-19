# Context7 MCP Configuration Examples

This document provides various configuration examples for Context7 MCP across different environments and scenarios. Use these examples as templates for your own setup.

## Basic Configurations

### Standard Windows Configuration (Cursor)

File location: `C:\Users\[username]\AppData\Roaming\Cursor\User\globalStorage\saoudrizwan.claude-dev\settings\cline_mcp_settings.json`

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

### VS Code Configuration

File location: `C:\Users\[username]\AppData\Roaming\Code\User\settings.json`

```json
{
  "mcp.servers": {
    "Context7": {
      "type": "stdio",
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"]
    }
  }
}
```

### Claude Desktop Configuration

File location: `C:\Users\[username]\AppData\Roaming\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "context7": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"]
    }
  }
}
```

## Advanced Configurations

### Multiple MCP Servers Configuration

This example shows how to configure multiple MCP servers alongside Context7:

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"],
      "disabled": false,
      "autoApprove": []
    },
    "github.com/modelcontextprotocol/servers/tree/main/src/memory": {
      "command": "node",
      "args": [
        "C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@modelcontextprotocol\\server-memory\\dist\\index.js"
      ],
      "env": {
        "MEMORY_FILE_PATH": "C:\\Users\\[username]\\Documents\\MCP\\memory\\memory.json"
      },
      "disabled": false,
      "autoApprove": [
        "create_entities",
        "create_relations",
        "read_graph",
        "search_nodes"
      ]
    }
  }
}
```

### Debug Mode Configuration

Enable debug mode for troubleshooting:

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": [
        "C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js",
        "--debug"
      ],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

### Local Development Configuration

If you're developing a local version of the Context7 MCP:

```json
{
  "mcpServers": {
    "context7-dev": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\path\\to\\your\\local\\context7-mcp\\dist\\index.js"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

## Linux and macOS Configurations

### Linux Configuration (VS Code)

File location: `~/.config/Code/User/settings.json`

```json
{
  "mcp.servers": {
    "Context7": {
      "type": "stdio",
      "command": "/usr/bin/node",
      "args": ["/usr/local/lib/node_modules/@upstash/context7-mcp/dist/index.js"]
    }
  }
}
```

### macOS Configuration (Cursor)

File location: `~/Library/Application Support/Cursor/User/globalStorage/saoudrizwan.claude-dev/settings/cline_mcp_settings.json`

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "/usr/local/bin/node",
      "args": ["/usr/local/lib/node_modules/@upstash/context7-mcp/dist/index.js"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

## Environment Variable Configuration

### Using Environment Variables for Configuration

You can add environment variables if needed:

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"],
      "env": {
        "NODE_ENV": "production",
        "LOG_LEVEL": "info"
      },
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

## Specific Tool Configurations

### Auto-Approving Specific Tools

Configure automatic approval for specific tools:

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"],
      "disabled": false,
      "autoApprove": [
        "resolve-library-id",
        "get-library-docs"
      ]
    }
  }
}
```

## Notes on Configuration

- Always use double backslashes (`\\`) in Windows file paths in JSON
- Replace `[username]` with your actual Windows username
- You may need to adjust paths depending on your specific Node.js installation
- Always restart your application after making configuration changes
- The `disabled` field can be set to `true` to temporarily disable a server without removing its configuration

For troubleshooting configuration issues, refer to the [Troubleshooting Guide](troubleshooting_guide.md).
