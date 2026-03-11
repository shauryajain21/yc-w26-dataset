# YC W26 Companies Dataset

Two independently compiled datasets of Y Combinator Winter 2026 batch companies.

## Files

| File | Description |
|---|---|
| `data/yc_w26_companies_v1.csv` | Broad dataset — 85 companies, 7 columns |
| `data/yc_w26_companies_v2.csv` | Curated dataset — 49 companies, 3 columns |

---

## Benchmarks

### Coverage

| Metric | v1 | v2 |
|---|---|---|
| Total companies | 85 | 49 |
| Unique to this file | 68 | 32 |
| Overlapping companies | 17 | 17 |
| **Combined unique companies** | **117** | — |

### Schema

| Column | v1 | v2 |
|---|---|---|
| Company name | ✅ | ✅ |
| Website | ✅ | ❌ |
| Category | ✅ | ✅ |
| Subcategory | ✅ | ❌ |
| Description | ✅ | ✅ |
| AI Depth classification | ✅ | ❌ |
| Notable Info (funding, traction) | ✅ | ❌ |

### Description Quality

| Metric | v1 | v2 |
|---|---|---|
| Total entries | 85 | 49 |
| Generic descriptions (<30 chars) | 37 (43.5%) | 1 (2.0%) |
| Detailed descriptions (30+ chars) | 48 (56.5%) | 48 (98.0%) |

v1 has broader coverage but nearly half its entries have placeholder descriptions like "Robotics company" or "Enterprise software". v2 is smaller but almost every entry has a specific, informative description with founder backgrounds, traction metrics, or technical details.

### Verdict

- **v1** is the better foundation — more companies, richer schema (websites, subcategories, AI depth, funding data)
- **v2** has superior description quality and 32 companies not found in v1
- **Ideal approach:** merge v1 as the base, backfill missing companies and richer descriptions from v2

---

## Structure

```
yc-w26-dataset/
├── README.md
└── data/
    ├── yc_w26_companies_v1.csv
    └── yc_w26_companies_v2.csv
```
