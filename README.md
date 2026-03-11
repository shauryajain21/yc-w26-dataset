# YC W26 Companies Dataset

Two independently compiled datasets of Y Combinator Winter 2026 batch companies.

## Files

| File | Description |
|---|---|
| `yc_w26_companies_linkup_claude_code.csv` | Broad dataset — 85 companies, 7 columns |
| `yc_w26_companies_claude_code_native_web_search.csv` | Curated dataset — 49 companies, 3 columns |

---

## Benchmarks

### Coverage

| Metric | Linkup + Claude Code | Claude Code (Native Web Search) |
|---|---|---|
| Total companies | 85 | 49 |
| Unique to this file | 68 | 32 |
| Overlapping companies | 17 | 17 |
| **Combined unique companies** | **117** | — |

### Schema

| Column | Linkup + Claude Code | Claude Code (Native Web Search) |
|---|---|---|
| Company name | ✅ | ✅ |
| Website | ✅ | ❌ |
| Category | ✅ | ✅ |
| Subcategory | ✅ | ❌ |
| Description | ✅ | ✅ |
| AI Depth classification | ✅ | ❌ |
| Notable Info (funding, traction) | ✅ | ❌ |

### Description Quality

| Metric | Linkup + Claude Code | Claude Code (Native Web Search) |
|---|---|---|
| Total entries | 85 | 49 |
| Generic descriptions (<30 chars) | 37 (43.5%) | 1 (2.0%) |
| Detailed descriptions (30+ chars) | 48 (56.5%) | 48 (98.0%) |

Linkup + Claude Code has broader coverage but nearly half its entries have placeholder descriptions like "Robotics company" or "Enterprise software". Claude Code (Native Web Search) is smaller but almost every entry has a specific, informative description with founder backgrounds, traction metrics, or technical details.

### Verdict

- **Linkup + Claude Code** is the better foundation — more companies, richer schema (websites, subcategories, AI depth, funding data)
- **Claude Code (Native Web Search)** has superior description quality and 32 companies not found in the other dataset
- **Ideal approach:** merge Linkup + Claude Code as the base, backfill missing companies and richer descriptions from the native web search dataset

---

## Structure

```
yc-w26-dataset/
├── README.md
└── data/
    ├── yc_w26_companies_linkup_claude_code.csv
    └── yc_w26_companies_claude_code_native_web_search.csv
```
