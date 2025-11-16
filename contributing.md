# Contribution Guidelines

Thank you for your interest in contributing to Awesome Data Engineering! This list exists to help data engineers discover the **right tools** for their needs - not every tool, but the most impactful ones.

## Philosophy

This is a **curated** list, not a comprehensive directory. Every addition should:
- Be actively maintained (recent commits, active community)
- Have real-world production usage at scale
- Solve a specific, well-defined problem
- Add value that isn't already covered by existing entries

## Before Contributing

1. **Search existing entries** - Ensure your suggestion isn't already listed
2. **Verify production readiness** - The tool should be stable enough for production use
3. **Check activity** - Repository or project should have recent activity (within 6-12 months)
4. **Review quality** - Good documentation, clear use cases, active community

## Submission Guidelines

### Format Requirements

All entries must follow this exact format:

```markdown
* [Tool Name](https://example.com/) - One clear sentence describing what it does and why you'd use it.
```

**Requirements:**
- **No spaces** between link text and URL: `[Tool](url)` not `[Tool] (url)`
- **Description must be actionable** - Explain what users can accomplish, not just what it is
- **One sentence** - Keep descriptions concise (ideally under 100 characters)
- **Proper capitalization** - Tool names should match official branding
- **HTTPS links** - Use secure URLs when available
- **Link to official source** - Main website or repository, not third-party pages

### Good Examples
✅ `* [dbt](https://www.getdbt.com/) - Transform data in your warehouse using SQL and software engineering best practices.`
✅ `* [Apache Kafka](https://kafka.apache.org/) - Distributed event streaming platform used by 100,000+ organizations.`

### Bad Examples
❌ `* [Tool] (https://example.com) - This is a tool`
*Issues: Space in link syntax, vague description*

❌ `* [SomeTool](https://example.com) - A data engineering tool that does things with data`
*Issue: Vague, doesn't explain what problem it solves*

❌ `* [NewTool](https://github.com/user/newtool) - Brand new tool I just created`
*Issue: Not production-proven, no real-world usage*

## What to Include

### Ideal Candidates
- **Industry standards** - Tools widely adopted in production environments
- **Active open-source projects** - Strong community, regular updates, good documentation
- **Production-proven** - Used at scale by known companies
- **Fills a gap** - Solves a problem not well-addressed by existing entries
- **Modern alternatives** - Significantly better approaches to existing problems

### What NOT to Include
- **Abandoned projects** - No updates in over a year without clear maintenance status
- **Personal/experimental projects** - Not battle-tested in production
- **Redundant entries** - Tools that don't differentiate from existing entries
- **Proprietary tools without trials** - If commercial, should have public documentation or trials
- **Vendor-specific tools** - Unless they're industry standards (e.g., AWS, GCP, Azure services)

## Categories

Entries should be placed in the most appropriate category following the **data lifecycle**:

1. **Data Ingestion** - Moving data from sources to destinations
2. **Data Storage** - Databases, warehouses, lakes, file systems
3. **Data Transformation** - SQL/Python tools for transforming data
4. **Orchestration & Workflow** - Scheduling and coordinating pipelines
5. **Stream Processing** - Real-time data processing
6. **Batch Processing** - Large-scale batch processing
7. **Data Quality & Observability** - Testing and monitoring data
8. **Data Discovery & Governance** - Catalogs, lineage, and governance
9. **Reverse ETL** - Syncing data to operational systems
10. **Analytics & Visualization** - BI tools and charting libraries
11. **Infrastructure & Deployment** - Container orchestration, IaC, monitoring
12. **Learning Resources** - Datasets for learning

If you're unsure which category fits, open an issue to discuss.

## Subcategories

Within categories, tools are organized by subcategory. Add your entry to the **bottom** of the appropriate subcategory, or propose a new subcategory if needed.

## Pull Request Process

1. **One tool per PR** - Makes review easier and discussion focused
2. **Descriptive PR title** - Format: `Add [Tool Name] to [Category]`
3. **Explain in PR description**:
   - What the tool does
   - Why it should be included
   - Production usage examples (if available)
   - How it's different from existing entries
4. **Ensure CI passes** - Check that markdown linting passes
5. **Respond to feedback** - Maintainers may ask for clarification or changes

## Quality Standards

All contributions are reviewed for:
- **Relevance** - Does it belong on a data engineering list?
- **Quality** - Is it production-ready and well-maintained?
- **Uniqueness** - Does it add value beyond existing entries?
- **Format** - Does it follow the style guidelines?
- **Accuracy** - Is the description factually correct?

## Updating Existing Entries

Found outdated information or broken links? PRs to update existing entries are welcome!

- Fix broken links
- Update descriptions to reflect current capabilities
- Add important sub-tools or related projects
- Remove deprecated or abandoned tools

## Questions?

Open an issue if you're unsure whether your contribution fits, or need help with formatting.

---

Thank you for helping make this the definitive resource for data engineers! 🚀
