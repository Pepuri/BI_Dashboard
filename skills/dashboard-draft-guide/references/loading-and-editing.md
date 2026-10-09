# Loading and editing

Inspect actual sources, schema, jobs, model binding, and last successful execution when accessible. Ask only about missing choices that affect the result.

| Choice | Establish |
|---|---|
| Freshness | Required latency, completion, refresh, acceptable staleness |
| History | Source, serving, model, and default view windows separately |
| Performance | Collection/ETL, model refresh, initial load, filter response, memory, or cost |
| Reuse | Prepared SQL/Delta, directory mappings, transforms, schedules, ownership |
| Constraints | License/capacity, volume, access, cost, operational responsibilities |
| Failure | Error state, last-good source, actual model data, recovery |

A date filter is not a physical retention or model-loading boundary. Source history does not imply model history. Choose modes from constraints and current official capabilities. Do not universalize Import, Direct Lake, DirectQuery, or any processing stack.

Propose `current structure → changes → reason → added operational burden → verification`. Recommend a primary option and a relevant alternative when a real choice remains. Reuse sufficient prepared data before new processing layers. Do not rebuild architecture for formatting.

Distinguish event, observation, completion, source snapshot, actual model data, refresh, and display time zone. Verify and display the fallback actually used, not a candidate date.

## Optional implementation capabilities

No authoring binary, connector, Microsoft permission, or third-party skill is bundled. Inspect capabilities available in the host.

For missing Microsoft implementation skills, follow [Microsoft skill setup](microsoft-setup.md). Install the relevant package through the host's authorized flow, then check its actual capabilities and access. Installation alone does not establish working connectivity.

| Layer | Example installed capability | Ownership |
|---|---|---|
| Report/PBIR | `powerbi-report-cli` | Report layout, bindings, filters, navigation |
| Semantic model | `semantic-model-authoring` | Tables, relationships, DAX, mode |
| SQL source inspection | `sqldw-cli` or authorized SQL tool | Schema, dates, representative data |
| Needed transformation | `spark-cli` or authorized engineering tool | Designated code and runs |
| Operational review | `powerbi-operational-report-quality` plus report tool | Meaning, density, interactions |
| Browser account work | `power-bi` or host browser tool | Authorized browser operations |
| Technical verification | Official documentation tools or browsing | Current features, limits, API signatures |

Missing capabilities do not prevent independent design. State unperformed actions and do not invent commands or bypass permissions/failure contracts. Upstream skills are separate dependencies; do not copy their source into this package without distribution rights.

Before editing, state target, capability, method, layer, scope, and checks. Use one writer per artifact/live UI with parallel read-only reviews where useful.

Relevant sequence: recover state → resolve fields/keys/loading → necessary model/data changes → representative overview/investigation → extend → affected checks → authorized operations/handoff.

Batch related edits, validate, apply, and check affected pages. Formatting does not imply data refresh. Report reload, model processing, refresh, and service execution are distinct. Follow host reload rules and protect unsaved human edits; disk hashes alone do not establish their ownership.

Recheck for new changes, failures, or unresolved concerns; broaden for global changes. Preserve passed unchanged evidence. Handoff: version, binding, staged/applied/cloud state, last successful check, remaining issue, next operation.

## Official entry points

- [Power BI report skill](https://learn.microsoft.com/power-bi/developer/agentic/power-bi-report-skill-overview)
- [Direct Lake overview](https://learn.microsoft.com/fabric/fundamentals/direct-lake-overview)

Verify applicable current behavior at use time. Documentation does not grant access or decide business priorities.
