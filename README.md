# <img src="https://www.oioioi.ai/brand/oi-icon.svg" alt="Oi Logo" style="width: 1em; height: 1em; vertical-align: -0.12em;" /> Oi - Gemini CLI and Antigravity

[Website](https://www.oioioi.ai) | [App](https://app.oioioi.ai)

Install Oi into Gemini CLI or Antigravity so you can work with your team's shared Contexts and Workflows.

You will need an Oi account and an Oi organization API key before connecting Oi.

Oi is provided as a hosted streamable HTTP MCP server at `https://api.oioioi.ai/mcp`.

## Gemini CLI

1. Install the extension:

```bash
gemini extensions install https://github.com/carhaix/oi-gemini
```

2. When prompted for `Oi API token`, paste an exported Oi organization API key.

3. Restart Gemini CLI so the extension MCP server is loaded.

4. Confirm the extension is installed:

```bash
gemini extensions list
```

5. Start Gemini CLI and ask it to use Oi:

```text
List the Oi contexts available to my team.
```

Gemini CLI exposes MCP tools with an `mcp_oi_` prefix internally. In normal use, you can simply ask Gemini to use Oi.

## Antigravity

1. Install the plugin:

```bash
agy plugin install https://github.com/carhaix/oi-gemini
```

2. Add your Oi organization API key to the installed plugin environment file:

```bash
OI_API_TOKEN=your_oi_api_key_here
```

The file is located at:

```text
~/.gemini/antigravity-cli/plugins/oi/.env
```

3. Restart Antigravity CLI.

4. Confirm the MCP server is connected:

```text
/mcp
```

Expected status:

```text
oi  connected
```

5. Ask Antigravity to use Oi:

```text
Use Oi to list my contexts.
```

If `/mcp` shows `Unauthorized [Auth Needed]`, Antigravity loaded the plugin but did not send a valid `Authorization` header to Oi. Confirm the `.env` file contains `OI_API_TOKEN` and restart Antigravity.

## Usage

After connecting Oi, ask Gemini CLI or Antigravity to use Oi for Context and Workflow discovery, retrieval, and usage flows:

```text
# list the Contexts available to your team
List the Oi contexts available to my team.

# list the Workflows available to your team
List the Oi workflows available to my team.

# recommend the best Context or Workflow for a task
Use Oi to recommend the best setup for reviewing this launch plan.

# use one Context for a focused task
Use the Oi designer context to review this onboarding flow.

# stack contexts to tackle complex problems
Use Oi with product-manager, designer, growth-lead, and software-engineer contexts to improve this onboarding flow.

# use one Workflow for a multi-step task
Use the Oi launch-readiness workflow to audit this release checklist before we ship.
```

## Update

Gemini CLI:

```bash
gemini extensions update oi
```

Antigravity:

```bash
agy plugin install https://github.com/carhaix/oi-gemini
```

## Uninstall

Gemini CLI:

```bash
gemini extensions uninstall oi
```

Antigravity:

```bash
agy plugin uninstall oi
```

## Files

- `gemini-extension.json` configures the Gemini CLI extension.
- `plugin.json` and `mcp_config.json` configure the Antigravity plugin.

## Links

- [Oi MCP guide](https://www.oioioi.ai/guides/what-is-oi-mcp)
- [Gemini CLI extension docs](https://geminicli.com/docs/extensions/)
- [Gemini CLI releasing guide](https://geminicli.com/docs/extensions/releasing/)
