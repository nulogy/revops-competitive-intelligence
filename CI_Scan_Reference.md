# Competitive Intelligence Scan Reference

Generated from: Nulogy_Battle_Card_Inventory_v4.xlsx
Last updated: 2026-03-23

---

## Competitors by Product Line

### Shop Floor
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| Plex | "Plex", "Rockwell Plex", "Plex MES" | High |
| Acumatica | "Acumatica" | High |
| Odoo | "Odoo", "Odoo MRP" | High |
| Manhattan WMS | "Manhattan", "Manhattan WMS", "Manhattan Associates" | High |
| Aptean Ross ERP | "Aptean", "Aptean Ross", "Ross ERP" | High |
| Microsoft Dynamics 365 | "Dynamics 365", "D365", "Microsoft Dynamics" | High |
| Blue Yonder WMS | "Blue Yonder", "BY WMS", "JDA" | High |
| Epicor Kinetic | "Epicor", "Epicor Kinetic" | Medium |
| SAP Business One | "SAP B1", "SAP Business One", "Business One" | Low |
| Oracle NetSuite | "NetSuite", "Oracle NetSuite" | Low |

### Smart Factory
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| QAD Redzone | "Redzone", "QAD Redzone", "Red Zone" | Maintenance |
| Vorne XL | "Vorne", "Vorne XL" | Maintenance |
| Factbird | "Factbird" | Medium |
| Pulsar | "Pulsar" | Medium |
| PlantRun | "PlantRun", "Plant Run" | Medium |
| FourJaw | "FourJaw", "Four Jaw" | Medium |
| Evocon | "Evocon", "Lineview" | Low |
| MachineMetrics | "MachineMetrics", "Machine Metrics" | Medium |
| Guidewheel | "Guidewheel", "Guide Wheel" | Medium |
| Tulip | "Tulip", "Tulip Interfaces" | Low |

### Quality & Compliance
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| SafetyChain | "SafetyChain", "Safety Chain" | Maintenance |
| CMX1 | "CMX1", "CMX" | Maintenance |
| SafetyCulture | "SafetyCulture", "Safety Culture", "iAuditor" | Maintenance |
| ComplianceMate | "ComplianceMate", "Compliance Mate", "Ladle" | Maintenance |
| Trustwell | "Trustwell", "FoodLogiQ", "Food LogiQ" | Maintenance |
| Intelex | "Intelex" | Maintenance |
| Ideagen | "Ideagen" | Maintenance |
| FoodsConnected | "FoodsConnected", "Foods Connected" | Maintenance |
| Safefood360 | "Safefood360", "Safefood 360" | Maintenance |
| TraceGains | "TraceGains", "Trace Gains" | Maintenance |
| RizePoint | "RizePoint", "Rize Point" | Maintenance |
| ETQ Reliance | "ETQ", "ETQ Reliance" | Low |
| ComplianceQuest | "ComplianceQuest", "Compliance Quest" | Low |

### Maintenance / CMMS
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| UpKeep | "UpKeep", "Up Keep" | Maintenance |
| eMaint | "eMaint", "Fluke eMaint" | Maintenance |
| Fiix | "Fiix", "Rockwell Fiix" | Maintenance |
| Limble | "Limble", "Limble CMMS" | Maintenance |
| MaintainX | "MaintainX", "Maintain X" | Maintenance |
| ShireSystem | "ShireSystem", "Shire System", "Elecosoft" | Maintenance |
| Brightly | "Brightly", "Siemens Brightly" | Maintenance |
| Llumin | "Llumin" | Maintenance |

### Supplier Collaboration
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| E2Open | "E2Open", "E2 Open" | High |
| Blue Yonder / OneNetwork | "OneNetwork", "One Network", "BY Network" | High |
| GTNexus / Infor Nexus | "GTNexus", "GT Nexus", "Infor Nexus" | High |
| TraceLink | "TraceLink", "Trace Link" | High |
| SAP Business Network | "SAP Business Network", "Ariba Network" | Medium |

### General / Cross-Product
| Competitor | Search Variants | Priority |
|------------|-----------------|----------|
| Custom Dev / AI-Generated Code | "build vs buy", "custom development", "in-house" | Medium |

---

## General Signal Terms

Search these terms across all public channels to catch competitive mentions not tied to known competitors:

### Win/Loss Signals
- "lost to"
- "beat us"
- "went with"
- "chose"
- "selected"
- "decided on"

### Active Competition Signals
- "competing against"
- "up against"
- "vs"
- "alternative"
- "compared to"
- "RFP"
- "bake-off"
- "evaluation"

### Churn / Switch Signals
- "switched to"
- "moving to"
- "replacing us"
- "churned"

### General Intel
- "competitor"
- "competitive"
- "differentiate"
- "objection"

---

## HubSpot Closed-Lost Deals

Scan closed-lost deals from the last 7 days for competitor intelligence.

### Fields to Extract
| Field | API Name | Type | CI Value |
|-------|----------|------|----------|
| Main Reason | `main_reason_for_won_deal__c` | Enumeration | Flag deals where = "Competition" |
| Summary Details | `summary_won_details__c` | Free text | Scan for competitor names |
| Won-Lost Report | `won_lost_report__c` | Free text | Scan for competitor names |
| Product Line | `product_categorization` | Text | Group by product |
| ARR | `arr` | Number | Quantify losses |
| Close Date | `closedate` | Date | Filter last 7 days |
| Owner | `hubspot_owner_id` | ID | Who to follow up with |

### Filter Criteria
```
hs_is_closed_lost = true
closedate >= [7 days ago]
```

### Main Reason Values to Flag
- **"Competition"** — Explicit competitive loss, high priority for follow-up
- **"Price - on-going costs"** / **"Price - one time costs"** — May contain competitor pricing intel in summary
- **"Product Fit"** — May indicate feature gaps vs. competitors

### Text Scanning
Scan `summary_won_details__c` and `won_lost_report__c` for:
1. Known competitor names from the inventory above
2. Keywords: "competitor", "alternative", "went with", "chose", "evaluating", "compared to", "incumbent"
3. New company names not in tracker (potential new competitors)

---

## Channels to Scan

### Direct Read (full scan, last 7 days)
- #chat-competitors

### Pattern Match (search within)
- Channels containing "prospect"
- Channels containing customer names (high-signal for churn intel)

### General Search Scope
- All public channels

---

## New Competitor Threshold

| Signal Level | Criteria | Action |
|--------------|----------|--------|
| Casual | Single mention, no deal context | Note in weekly summary |
| Warm | 2+ mentions across 2 weeks, OR mentioned in #chat-competitors with context | Add to Research Gaps in tracker |
| Hot | Mentioned in prospect/customer channel, OR "lost to" / win-loss language | Flag for immediate card consideration |
| Create Card | Multiple deal-context mentions, OR explicit win/loss attribution | Add to Planned Builds, assign owner |

---

## Output Destinations

- **Slack summary:** #chat-competitors
- **Detailed file:** /Weekly Scans/CI_Scan_YYYY-MM-DD.md
