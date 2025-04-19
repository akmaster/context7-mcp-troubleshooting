# Context7 MCP Installation Guide

This guide provides detailed instructions for installing and configuring the Context7 MCP server on Windows environments. Follow these steps to integrate up-to-date library documentation into your AI coding assistant.

## Prerequisites

- Node.js (version 18.0.0 or higher)
- npm (usually comes with Node.js)
- Cursor, VS Code, or another MCP-compatible editor/IDE

## Step-by-Step Installation

### 1. Install Context7 MCP globally

Open a terminal (Command Prompt or PowerShell) and run:

```bash
npm install -g @upstash/context7-mcp@latest
```

This will install the Context7 MCP package globally on your system.

### 2. Verify installation

Confirm that the package was installed successfully:

```bash
npm list -g | findstr context7
```

You should see output similar to:
```
├── @upstash/context7-mcp@1.0.4 (or latest version)
```

### 3. Find installation paths

You will need these paths to configure your MCP settings:

```bash
# Get Node.js executable path
where node
# Example output: C:\Program Files\nodejs\node.exe

# Get global npm packages directory
npm root -g
# Example output: C:\Users\username\AppData\Roaming\npm\node_modules
```

### 4. Create MCP directory (optional but recommended)

Create a dedicated directory for MCP servers:

```bash
mkdir "C:\Users\%USERNAME%\Documents\Cline\MCP\context7-mcp"
```

### 5. Configure MCP in Cursor

The configuration file for Cursor is typically located at:
```
C:\Users\[username]\AppData\Roaming\Cursor\User\globalStorage\saoudrizwan.claude-dev\settings\cline_mcp_settings.json
```

Edit this file to add Context7 MCP:

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "C:\\Program Files\\nodejs\\node.exe",
      "args": ["C:\\Users\\[username]\\AppData\\Roaming\\npm\\node_modules\\@upstash\\context7-mcp\\dist\\index.js"],
      "disabled": false,
      "autoApprove": []
    }
    // Other MCP servers may be here
  }
}
```

> **Note:** Replace `[username]` with your actual Windows username.

### 6. Configure MCP in VS Code (Alternative)

If you're using VS Code, the configuration file can be found at:
```
C:\Users\[username]\AppData\Roaming\Code\User\settings.json
```

Add the following configuration:

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

### 7. Restart your application

After making changes to the configuration files, restart Cursor, VS Code, or your MCP-compatible application to apply the changes.

## Testing the Installation

Once installed and configured, you can test Context7 MCP by:

1. Opening your AI assistant (Cursor, VS Code with appropriate extensions, etc.)
2. Asking a question about a library with the prefix "use context7"

Example:
```
How do I use React hooks? use context7
```

## Next Steps

If you encounter any issues during installation or testing, refer to our [Troubleshooting Guide](troubleshooting_guide.md).

For various configuration examples for different environments, see [Configuration Examples](configuration_examples.md).

## Additional Resources

- [Official Context7 Documentation](https://github.com/upstash/context7-mcp)
- [MCP Protocol Specification](https://github.com/modelcontextprotocol/mcp)
- [Cursor MCP Documentation](https://docs.cursor.com/context/model-context-protocol)
