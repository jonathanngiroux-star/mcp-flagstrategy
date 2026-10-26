# mcp-flagstrategy

MCP server for feature flag strategy - ongoing rollout-strategy reviews (switchyard extension).

## Tools

### list_flags
List feature flags for a project.

**Parameters:**
- `project_id` (string, optional): Project ID

### toggle_flag
Toggle a feature flag on/off.

**Parameters:**
- `flag_id` (string, required): Flag ID
- `enabled` (boolean, required): Enable or disable the flag

### get_rollout_status
Get rollout status for a flag.

**Parameters:**
- `flag_id` (string, required): Flag ID

### get_strategy_report
Get feature flag strategy report for a project.

**Parameters:**
- `project_id` (string, optional): Project ID

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

## Connecting to Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "flagstrategy": {
      "command": "python",
      "args": ["/path/to/mcp-flagstrategy/main.py"],
      "cwd": "/path/to/mcp-flagstrategy"
    }
  }
}
```

## License

MIT