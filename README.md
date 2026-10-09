# M365 BI Dashboard Skill

A community-authored skill for designing Microsoft 365 operational dashboards with Power BI and Microsoft Fabric. It connects the operator's task to required fields, data contracts, loading choices, editing methods, and evidence-based review. Use it for M365 workloads such as Intune devices and Entra ID accounts when the supplied data supports the investigation.

**Workflow:** business task and required information → data contract → loading choice → representative pages → editing and verification → acceptance checks → quality review.

## What is included

- `dashboard-draft-guide`: dashboard drafts, design reviews, and resuming existing work.
- Required identity and context in investigation tables, with masking and access requirements.
- Metric selection based on an operational decision and inspectable evidence.
- Separate source retention, serving tables, model loading, and view filters.
- A plan for editing reports, semantic models, and necessary data transformations.
- Required acceptance checks before quality scores, with draft and implementation evidence kept distinct.
- [Request templates](skills/dashboard-draft-guide/references/request-template.md), a [configurable profile](examples/user-profile.example.md), and a [synthetic example](examples/device-operations.synthetic.json).
- [Official Microsoft companion skill installation](skills/dashboard-draft-guide/references/microsoft-setup.md).

This package supplies instructions. Report authoring tools, connectors, licenses, and account permissions are separate requirements for implementation. It is independently maintained and is not a Microsoft product or endorsement.

## Install this skill

Ask Codex:

```text
$skill-installer
Install the skill from:
https://github.com/Pepuri/BI_Dashboard/tree/main/skills/dashboard-draft-guide
```

If the same skill name already exists, preserve its private settings and choose the destination before installation. The installer does not automatically overwrite an existing folder.

For a project-local installation, download the repository ZIP and copy the **entire** `skills/dashboard-draft-guide` folder to your project's `.agents/skills/dashboard-draft-guide`. Include `references/` and `agents/`. Start a new chat and restart the app if the skill is not discovered. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills).

The repository also includes a portable `plugin.json` and a Codex compatibility manifest. They support plugin packaging; this repository has not been submitted to or reviewed for the public Plugins Directory. See [plugin packaging](https://developers.openai.com/plugins/build/plugins).

## Install Microsoft's implementation skills

Design-only work can use the supplied brief and schema. For actual Power BI editing, Microsoft's **Power BI authoring** package is the recommended companion. For Fabric engineering, add **Fabric skills** as needed.

| Official Microsoft package | Relevant skills | When to use |
|---|---|---|
| `powerbi-authoring` | `powerbi-report-cli`, `semantic-model-authoring` | Report/PBIR editing, relationships, DAX, and semantic models |
| `fabric-skills` | `sqldw-cli`, `spark-cli`, `dataflows-cli`, and other Fabric workflows | Fabric sources, necessary transformations, and service operations |

Both packages are distributed from [Microsoft's Skills for Fabric repository](https://github.com/microsoft/skills-for-fabric). See the [setup guide](skills/dashboard-draft-guide/references/microsoft-setup.md) for Codex installation commands, runtime requirements, authentication, and verification.

These packages are separate dependencies. This custom skill does not automatically install them or grant Microsoft access.

## Use

```text
$dashboard-draft-guide
Draft an M365 operations dashboard for finding stale Intune devices by organization.
Inspect the attached schema and existing daily Import model first.
Show display name, account, device, state, and actual data date in the investigation table.
Explain the selected metrics, loading structure, representative pages,
editing skills and methods, acceptance evidence, and review criteria.
Scope: design only. Write the dashboard brief in my requested language.
```

For implementation, identify the target artifacts and execution scope. Publication, scheduling, and actual data changes follow the current user's authorized scope.

In ordinary ChatGPT or Claude conversations, attach `SKILL.md` and the relevant `references/` files and ask the assistant to follow them. This does not install a skill in those products or grant local file access.

## Preserve your design direction

Copy the [example profile](examples/user-profile.example.md) into your own private workspace. Set the language, time zone, viewport, required fields, navigation, and acceptance conditions. Refer to that profile in later requests.

Record corrections as `problem → reason → design principle → applicable scope → verification`. Keep reusable preferences, project decisions, and actual applied state distinct. Keep private profiles and customer data outside this public repository.

A technical version field does not automatically justify a version-change KPI. Explain the decision it supports. For person-linked investigations, missing required names or accounts prevents acceptance even if the layout scores well.

## Privacy and distribution

The package excludes real customers, users, accounts, tenant identifiers, private conversation links, personal local paths, original work history, reports, telemetry, and screenshots. Example names, addresses, identifiers, and data are synthetic. Keep actual sources and configuration in your private workspace, and use synthetic examples when contributing.

## License

MIT. See [LICENSE](LICENSE). Microsoft companion packages retain their own licenses and setup requirements.
