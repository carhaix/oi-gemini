# <img src="https://www.oioioi.ai/brand/oi-icon.svg" alt="Oi Logo" style="width: 1em; height: 1em; vertical-align: -0.12em;" /> Oi - Gemini CLI

[Website](https://www.oioioi.ai) | [App](https://app.oioioi.ai)

Install Oi into Gemini CLI so you can work with your team's shared Contexts and Workflows.

You will need an Oi account and an Oi organization API key before connecting Oi to Gemini CLI.

## Quick Start

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

Oi is provided as a hosted streamable HTTP MCP server at `https://api.oioioi.ai/mcp`.

## Usage

After connecting Oi in Gemini CLI, ask Gemini to use Oi for Context and Workflow discovery, retrieval, and usage flows:

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

Gemini CLI exposes MCP tools with an `mcp_oi_` prefix internally. In normal use, you can simply ask Gemini to use Oi.

## Update

```bash
gemini extensions update oi
```

## Uninstall

```bash
gemini extensions uninstall oi
```

## Links

- [Oi MCP guide](https://www.oioioi.ai/guides/what-is-oi-mcp)
- [Gemini CLI extension docs](https://geminicli.com/docs/extensions/)
- [Gemini CLI releasing guide](https://geminicli.com/docs/extensions/releasing/)
