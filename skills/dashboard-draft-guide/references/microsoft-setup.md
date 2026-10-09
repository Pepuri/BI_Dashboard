# Official Microsoft companion skills

Read this when preparing an implementation environment or resolving missing Microsoft authoring skills. Inspect what is already installed before adding anything. Design from supplied material can proceed without these packages.

## Choose the package

Microsoft distributes the packages through [Skills for Fabric](https://github.com/microsoft/skills-for-fabric). Its marketplace is `fabric-collection`.

| Package | Contents relevant to this skill | Need |
|---|---|---|
| `powerbi-authoring` | `powerbi-report-cli`, `semantic-model-authoring`, and a Power BI modeling MCP configuration | Recommended for Power BI implementation |
| `fabric-skills` | Fabric SQL, Spark, Dataflow, discovery, and other workflows | Add for actual Fabric work that needs these capabilities |

This community package does not bundle Microsoft's code or automatically install dependencies. Installing a package does not supply data collection, credentials, licenses, or tenant permissions. Do not add a Spark layer merely because its skill is available.

## Codex installation

Use a current Codex CLI with `plugin` commands. Add Microsoft's marketplace, inspect the available entries, and install the Power BI package:

```sh
codex plugin marketplace add microsoft/skills-for-fabric
codex plugin list --available --json
codex plugin add powerbi-authoring@fabric-collection
```

For Fabric engineering, add the Fabric package only when needed:

```sh
codex plugin add fabric-skills@fabric-collection
```

Then inspect the installed packages:

```sh
codex plugin list --json
```

These use [Codex's documented plugin commands](https://learn.chatgpt.com/docs/cli/reference) with Microsoft's published marketplace and package identifiers. OpenAI also documents [legacy marketplace and Claude-compatible package support](https://developers.openai.com/plugins/build/plugins). Start a new chat after installation; restart the desktop app if its plugin list has not refreshed.

If your Codex client lacks these commands, use its supported plugin installation interface or follow the current upstream setup instructions. Resolve the current entries before installation instead of guessing commands for an older client. Microsoft's repository has separate setup instructions for other agent hosts; do not use Claude Code slash commands as Codex shell commands.

## Verify implementation readiness

1. Confirm that the required skills appear in the current host. Read their installed instructions before acting.
2. Check the runtime required by the selected workflow. Microsoft's local Power BI modeling MCP currently requires Node.js 18 or later. Report authoring binaries and other tools follow their own setup.
3. Confirm the actual report/model target, source binding, and available access. Service operations need applicable Microsoft authentication and permissions; plugin installation does not establish them.
4. Check the preview host for report work. Power BI Desktop is useful for local opening and visual verification; use a supported alternative when available.
5. Begin with a read-only inspection or validation. Report installed, authenticated, connected, rendered, and successfully executed as separate states.

Consult [Power BI agentic setup](https://learn.microsoft.com/en-us/power-bi/developer/agentic/power-bi-agentic-overview), [semantic-model requirements](https://learn.microsoft.com/en-us/power-bi/developer/agentic/semantic-model-authoring-skill-overview), and [Fabric installation](https://learn.microsoft.com/en-us/fabric/fundamentals/skills-for-fabric-install). Recheck current upstream requirements when installing or using the tools.

## Look up technical details

Use Microsoft Learn tools for current product features, limits, and signatures. Keep business priorities in the user's design contract.

If the Learn MCP tools are unavailable, the official Learn CLI can perform the same lookup:

| Learn MCP tool | CLI alternative |
|---|---|
| `microsoft_docs_search` | `npx @microsoft/learn-cli search "Power BI report skill prerequisites"` |
| `microsoft_docs_fetch` | `npx @microsoft/learn-cli fetch <official-documentation-url>` |
| `microsoft_code_sample_search` | `npx @microsoft/learn-cli code-search "Microsoft Graph managed devices" --language powershell` |

Use the host's normal installation and execution rules. This lookup alternative is not a mandatory dashboard dependency.
