# mcp-server

# Issue: MCP: List Servers Command Not Appearing in VS Code on macOS

## Problem Description
I am trying to configure and run a Python-based Model Context Protocol (MCP) server using Visual Studio Code on my MacBook Air. However, the `MCP: List Servers` command is not appearing in the VS Code Command Palette.

## Environment
- **Operating System:** macOS (MacBook Air)
- **Editor:** Visual Studio Code
- **Python Version:** Python 3.14
- **MCP Package Version:** 2.3.0
- **Virtual Environment:** `.venv`

## Steps Taken
1. Created a Python virtual environment using `.venv`.
2. Activated the environment using:
   ```bash
   source .venv/bin/activate
   ```
3. Upgraded pip.
4. Installed the MCP package using:
   ```bash
   python -m pip install "mcp[cli]"
   ```
5. Verified installation using:
   ```bash
   python -m pip show mcp
   ```
6. Created an MCP configuration file at `.vscode/mcp.json`.
7. Configured the MCP server to use the macOS Python executable:

   ```json
   {
     "servers": {
       "helloMcp": {
         "type": "stdio",
         "command": "${workspaceFolder}/.venv/bin/python",
         "args": ["server.py"]
       }
     }
   }
   ```

## Expected Result
The `MCP: List Servers` command should appear in the VS Code Command Palette when pressing `Cmd + Shift + P`, allowing me to select and start my MCP server.

## Actual Result
The `MCP: List Servers` command does not appear in the Command Palette. I am unable to start or manage my MCP server through VS Code.

## Help Needed
I need assistance identifying the required VS Code version, extensions, or configuration changes to enable MCP support on macOS and successfully run my Python MCP server.
