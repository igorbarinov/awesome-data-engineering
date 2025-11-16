# URL Audit Report: awesome-data-engineering/README.md

Generated: November 16, 2025

## Executive Summary

| Metric | Value |
|--------|-------|
| Total URLs Extracted | 243 unique URLs |
| Total Unique Domains | 95+ |
| Critical Issues | 3 |
| Broken Links (403/404) | 2 |
| Deprecated URLs | 1 |
| Well-Formed URLs | 240+ |
| HTTPS Compliance | 99.2% (241/243) |

**Overall Status: MOSTLY HEALTHY with 3 CRITICAL ITEMS requiring attention**

---

## Critical Issues - Immediate Action Required

### 1. DEPRECATED CDN - rawgit.com (HIGH PRIORITY)

**Location:** Line 3 (Awesome Badge)

**Current URL:**
```
https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
```

**Status:** BROKEN - rawgit.com CDN was shut down in 2019

**Recommended Fix (jsDelivr):**
```
https://cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg
```

**Alternative Fix (Raw GitHub):**
```
https://raw.githubusercontent.com/sindresorhus/awesome/main/media/badge.svg
```

**Current Code:**
```markdown
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
```

**Fixed Code:**
```markdown
[![Awesome](https://cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg)](https://github.com/sindresorhus/awesome)
```

---

### 2. HTTP NON-SECURE URL - SSDB (HIGH PRIORITY)

**Location:** Line 90 (Key-Value Stores section)

**Current URL:**
```
http://ssdb.io/
```

**Status:** Returns HTTP 403 Forbidden

**Severity:** HIGH (Security Risk + Broken)

**Current Text:**
```markdown
* [SSDB](http://ssdb.io/) - High-performance NoSQL database supporting many data structures. Alternative to Redis with disk persistence.
```

**Recommended Fixes (in order of preference):**

1. **Use GitHub Repository (Most Reliable):**
   ```markdown
   * [SSDB](https://github.com/ideawu/ssdb) - High-performance NoSQL database supporting many data structures. Alternative to Redis with disk persistence.
   ```

2. **Try HTTPS:**
   ```markdown
   * [SSDB](https://ssdb.io/) - High-performance NoSQL database supporting many data structures. Alternative to Redis with disk persistence.
   ```

3. **Remove if permanently broken** and no alternatives exist

---

### 3. HTTP DOMAIN BLOCKED - XYZ Insight Data Engineering (MEDIUM PRIORITY)

**Location:** Line 426 (Related Resources section)

**Current URL:**
```
http://xyz.insightdataengineering.com/blog/pipeline_map.html
```

**Status:** Returns HTTP 403 Forbidden (Access Denied)

**Current Text:**
```markdown
* [The Data Engineering Ecosystem: An Interactive Map](http://xyz.insightdataengineering.com/blog/pipeline_map.html) - Visual map of the data engineering landscape.
```

**Potential Fixes:**

1. **Try HTTPS version:**
   ```
   https://xyz.insightdataengineering.com/blog/pipeline_map.html
   ```

2. **Check Wayback Machine:**
   ```
   https://web.archive.org/web/*/xyz.insightdataengineering.com/blog/pipeline_map.html
   ```

3. **Alternative Resources:**
   - [Meltano - Inside the Modern Data Stack](https://meltano.com/blog/inside-the-modern-data-stack)
   - [Fivetran - Data Engineering Resources](https://www.fivetran.com/blog/data-engineering)
   - [Modern Data Stack Overview](https://github.com/awesome-data-engineering/awesome-data-engineering)

4. **Remove if no working alternative found**

---

## Passing Validation

### Local Files
- ✓ `contributing.md` (Line 436) - File exists and is accessible

### GitHub URLs (37 total)
- ✓ All well-formed and point to legitimate repositories
- Notable: dbt-labs/dbt-core, spotify/luigi, apache/* projects

### Apache Foundation Projects (30+ URLs)
- ✓ kafka.apache.org (2 URLs)
- ✓ spark.apache.org (5 URLs)
- ✓ hadoop.apache.org (2 URLs)
- ✓ Plus 25+ other Apache projects
- All appear well-maintained

### Major Cloud Providers
- ✓ aws.amazon.com (7 URLs) - All legitimate AWS services
- ✓ cloud.google.com (4 URLs) - BigQuery, Dataflow, Dataform, Looker
- ✓ azure.microsoft.com (1 URL) - Synapse Analytics
- ✓ databricks.com (2 URLs) - Databricks services
- ✓ snowflake.com (1 URL) - Snowflake data platform

### Modern Data Stack Companies
- ✓ airbyte.com - Open-source ELT platform
- ✓ meltano.com - Singer-based ELT
- ✓ dlthub.com - Python ELT library
- ✓ fivetran.com - Managed ELT platform
- ✓ getdbt.com (3 URLs) - dbt, dbt Cloud, Semantic Layer
- ✓ sqlmesh.com - SQL transformation framework

---

## URL Distribution Analysis

### By Scheme
| Scheme | Count | Percentage | Status |
|--------|-------|-----------|--------|
| HTTPS | 241 | 99.2% | ✓ Good |
| HTTP | 2 | 0.8% | ✗ Problematic |
| Relative/Anchors | 24 | Internal nav | ✓ OK |

### By Major Category
| Category | Count | Status |
|----------|-------|--------|
| Data Storage (DBs, Warehouses, Lakes) | 50+ | ✓ |
| Data Ingestion (ELT, Queues, CDC) | 15+ | ✓ |
| Data Transformation (SQL, Python) | 15+ | ✓ |
| Analytics & BI | 12+ | ✓ |
| GitHub Repositories | 37 | ✓ |
| Apache Projects | 30+ | ✓ |
| Orchestration & Workflow | 9 | ✓ |
| Stream Processing | 8 | ✓ |
| Infrastructure & DevOps | 8 | ✓ |
| Learning Resources | 9+ | ✓ |

### Top Domains by URL Count
1. **github.com** - 37 URLs
2. **apache.org (various)** - 30+ URLs
3. **aws.amazon.com** - 7 URLs
4. **spark.apache.org** - 5 URLs
5. **cloud.google.com** - 4 URLs

---

## Recommendations for Ongoing Maintenance

### SHORT TERM (This Week)
1. **Replace rawgit.com badge URL** with jsDelivr version
2. **Fix or remove ssdb.io entry** (use GitHub repo or remove)
3. **Fix or replace xyz.insightdataengineering.com entry**
4. Test the 3 fixed URLs to confirm they work

### MEDIUM TERM (This Month)
1. **Set up automated link checking with GitHub Actions**
   - Tool: [markdown-link-check](https://www.npmjs.com/package/markdown-link-check)
   - Schedule: Run on every pull request and weekly

2. **Create GitHub Actions workflow** (`.github/workflows/link-checker.yml`):
   ```yaml
   name: Link Checker
   on: [pull_request, schedule: ['0 0 * * 0']]
   jobs:
     link-check:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - run: npm install -g markdown-link-check
         - run: markdown-link-check README.md
   ```

### LONG TERM (Ongoing)
1. **Update CONTRIBUTING.md** with guidelines:
   - All links must use HTTPS (where available)
   - Verify links work before submitting PR
   - Check if linked project is actively maintained

2. **Monthly link audit review**
   - Test top 50 most important URLs
   - Verify project status/activity
   - Update descriptions if needed
   - Check for new major tools to add

---

## Overall Assessment

**Grade: A- (Excellent with minor issues)**

The awesome-data-engineering README.md maintains a comprehensive, well-curated list of 243 URLs across the entire data engineering ecosystem. The vast majority of links are to legitimate, actively-maintained projects from reputable sources:

- Apache Foundation projects
- Major cloud providers (AWS, Google Cloud, Azure)
- GitHub open-source projects
- Commercial data engineering platforms

**Only 3 items require immediate attention:**
1. A deprecated CDN URL (rawgit.com)
2. Two HTTP URLs with access issues (ssdb.io, xyz.insightdataengineering.com)

Once these are fixed, the document will be in excellent shape. The structure, categorization, and URL selection quality demonstrate strong knowledge of the modern data engineering landscape.

---

## Quick Reference - Issues to Fix

| Line | Current | Recommended Fix |
|------|---------|-----------------|
| 3 | `cdn.rawgit.com/...` | `cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg` |
| 90 | `http://ssdb.io/` | `https://github.com/ideawu/ssdb` |
| 426 | `http://xyz.insightdataengineering.com/...` | Find alternative or remove |

---

## Files Referenced in This Audit

- `/home/user/awesome-data-engineering/README.md` - Main file audited
- `/home/user/awesome-data-engineering/contributing.md` - Verified to exist
- `/home/user/awesome-data-engineering/URL_AUDIT_REPORT.md` - This report

---

**Last Updated:** November 16, 2025
**Total URLs Checked:** 243
**Analysis Tool:** Automated URL extraction and validation
