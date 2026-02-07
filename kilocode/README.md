# KiloCode Configuration

This directory contains KiloCode custom mode configurations for the ai-agents project.

## Modes

### Developer Assistant (`developer-assistant.yaml`)
A development assistant focused on helping developers code faster and smarter through code suggestions, explanations, reviews, and debugging help. Operates in a developer-controlled manner with incremental implementation support.

### Architect Assistant (`architect-assistant.yaml`)
An architect-focused assistant for planning, requirements gathering, design decisions, and documentation. Helps break down complex architectural challenges into manageable components.

## Importing and Using These Modes

### Option 1: Import via Settings (Recommended)
1. Open KiloCode settings
2. Navigate to **Agent Behaviour**
3. Select **Import mode**
4. Upload both YAML files (`developer-assistant.yaml` and `architect-assistant.yaml`)
5. Restart VS Code or your KiloCode-enabled editor

### Option 2: Manual Update
Edit the custom modes file directly:
- **Path**: `C:\Users\<your-username>\AppData\Roaming\Code\User\globalStorage\kilocode.kilo-code\settings\custom_modes.yaml`
- Copy the contents from both YAML files into the `customModes` section
- Save the file and restart VS Code

### Step 2: Select a Mode
1. Open the KiloCode mode selector (usually in the status bar or command palette)
2. Choose either:
   - **Developer Assistant** - For coding tasks, debugging, and implementation
   - **Architect Assistant** - For planning, requirements, and architecture documentation

## File Structure

```
kilocode/
├── README.md                    # This file
├── developer-assistant.yaml    # Developer mode configuration
└── architect-assistant.yaml     # Architect mode configuration
```

## Mode Permissions

### Developer Assistant
- **Read**: Read project files
- **Edit**: Modify project files
- **Browser**: Web browsing capabilities
- **Command**: Execute shell commands
- **MCP**: Model Context Protocol access

### Architect Assistant
- **Read**: Read project files
- **Edit**: Modify only Markdown (.md) files
- **Browser**: Web browsing capabilities
- **MCP**: Model Context Protocol access
