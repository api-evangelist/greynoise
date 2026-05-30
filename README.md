# GreyNoise Intelligence (greynoise)

GreyNoise Intelligence collects and analyzes Internet-wide scan and attack traffic from a global network of sensors. Use GreyNoise to contextualize alerts, filter false positives, identify compromised devices, prioritize vulnerabilities by in-the-wild exploitation, and track emerging threats.

**APIs.yml:** [apis.yml](apis.yml)

## Type

- **x-type:** company
- **x-category:** Security
- **x-tier:** 3 (bulk-registered from public-apis, enriched 2026-05-30)
- **Source:** [public-apis/public-apis](https://github.com/public-apis/public-apis)

## Provider

- **Website:** https://www.greynoise.io
- **Developer Portal:** https://docs.greynoise.io
- **Console:** https://viz.greynoise.io
- **GitHub Organization:** https://github.com/GreyNoise-Intelligence
- **Pricing:** https://www.greynoise.io/pricing
- **Status:** https://status.greynoise.io
- **Trust Center:** https://trust.greynoise.io

## APIs

### GreyNoise API

Unified API surface spanning the free Community endpoint and the paid Enterprise endpoints. **27 operations** across 9 tag groups.

- **Base URL:** https://api.greynoise.io
- **Authentication:** API key in the `key` HTTP header (`APIKeyHeaderAuth`)
- **Documentation:** https://docs.greynoise.io
- **API Reference:** https://docs.greynoise.io/reference/getcommunityip
- **OpenAPI:** [openapi/greynoise-openapi.yml](openapi/greynoise-openapi.yml)

#### Operation groups

| Tag | Operations | Notes |
|---|---|---|
| Community | 1 | Free community IP lookup |
| IP Lookup | 2 | Single + multi-IP (up to 10,000 per request) full context |
| GNQL | 3 | Query / metadata-query / stats |
| Recall | 2 | Hourly/daily time-series over a GNQL query |
| IP Timeline | 1 | Per-IP per-field activity summary |
| Sessions | 10 | Sensor session telemetry, connection graphs, PCAP export |
| Tags | 1 | List behavior/affiliation tags |
| CVE | 2 | Per-CVE + bulk CVE (up to 10,000 per request) lookup |
| Callback | 4 | Post-exploit / C2 callback IP intelligence |
| Utility | 1 | Service-health ping |

## Tools

- **MCP Server:** [greynoise-mcp-server](https://github.com/GreyNoise-Intelligence/greynoise-mcp-server) — official Model Context Protocol server for the Enterprise API.
- **Terraform Provider:** [terraform-provider-greynoise](https://github.com/GreyNoise-Intelligence/terraform-provider-greynoise) — manage alerts and blocklists as code.
- **Splunk App:** [SA-GreyNoise](https://github.com/GreyNoise-Intelligence/SA-GreyNoise).

## SDKs & CLI

- **Python SDK + CLI:** [pygreynoise](https://github.com/GreyNoise-Intelligence/pygreynoise)
- **PowerShell Module:** [GreyNoisePS](https://github.com/GreyNoise-Intelligence/GreyNoisePS)
- **Labs GraphQL Client:** [greynoiselabs](https://github.com/GreyNoise-Intelligence/greynoiselabs)

## Generated Artifacts

This repo has been profiled by the API Evangelist pipeline. Counts below were produced on 2026-05-30.

| Artifact | Folder | Files |
|---|---|---|
| OpenAPI 3.0.0 spec (full, with Microcks examples) | `openapi/` | 1 |
| Naftiko capabilities (one per OpenAPI tag) | `capabilities/` | 10 |
| Spectral ruleset (GreyNoise conventions) | `rules/` | 1 |
| JSON Schema (one per component schema) | `json-schema/` | 65 |
| JSON Structure (one per component schema) | `json-structure/` | 65 |
| Example payloads (one per component schema) | `examples/` | 65 |
| JSON-LD context (provider-wide) | `json-ld/` | 1 |
| Controlled vocabulary | `vocabulary/` | 1 |
| Plans & pricing (API Commons Plans 0.1) | `plans/` | 1 |
| Rate limits (API Commons Rate Limits 0.1) | `rate-limits/` | 1 |
| FinOps profile (FOCUS-aligned) | `finops/` | 1 |

### Naftiko Capabilities

Each file is self-contained: inline `consumes` block plus paired `rest` and `mcp` exposers.

| File | Operations |
|---|---|
| `capabilities/greynoise-community.yaml` | 1 |
| `capabilities/greynoise-ip-lookup.yaml` | 2 |
| `capabilities/greynoise-gnql.yaml` | 3 |
| `capabilities/greynoise-recall.yaml` | 2 |
| `capabilities/greynoise-ip-timeline.yaml` | 1 |
| `capabilities/greynoise-sessions.yaml` | 10 |
| `capabilities/greynoise-tags.yaml` | 1 |
| `capabilities/greynoise-cve.yaml` | 2 |
| `capabilities/greynoise-callback.yaml` | 4 |
| `capabilities/greynoise-utility.yaml` | 1 |

## Plans

GreyNoise sells four tiers (Free, Standard, Advanced, Elite) plus three core intelligence modules (Triage, Investigate, Hunt) and three add-on modules (C2 Detection, Business Services / RIOT, Vulnerability Prioritization). See [plans/greynoise-plans-pricing.yml](plans/greynoise-plans-pricing.yml) for details.

## Rate Limits

The free Community API caps at ~50 searches per week per source IP. The Enterprise API enforces per-key contract-specific limits with usage telemetry in the GreyNoise web UI. Multi-IP lookup and Bulk CVE lookup cap at 10,000 items per request. See [rate-limits/greynoise-rate-limits.yml](rate-limits/greynoise-rate-limits.yml).

## FinOps

GreyNoise is sold as an annual flat-rate subscription per tier with optional priced modules; per-call usage is not metered. See [finops/greynoise-finops.yml](finops/greynoise-finops.yml) for FOCUS-aligned billing mapping and cost-allocation guidance.

## Integrations

SIEM (Splunk, Microsoft Sentinel, Google SecOps, CrowdStrike NG-SIEM, Cribl) · SOAR (Splunk SOAR, Cortex XSOAR, FortiSOAR, Swimlane, Tines, Google SecOps SOAR) · TIP (Anomali ThreatStream, MISP, Recorded Future, ThreatQ, OpenCTI) · Analyst tools (Maltego, Polarity) · Firewalls (Palo Alto Networks PAN-OS EDL, fail2ban) · AI (Microsoft Copilot for Security, MCP) · Infrastructure (Terraform).

## Tags

Security, Threat Intelligence, Cybersecurity, IP Reputation, Vulnerability Management, Network Telemetry, SOC Automation, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## Maintainers

- **Kin Lane** — kin@apievangelist.com
