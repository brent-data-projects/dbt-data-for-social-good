# Nonprofit Analytics Engineering Tech Stack

Purpose of this doc is to lay out the shortlist of tools to pick from, so it's easier to help nonprofits make analytics/data/AI tooling decisions.  Obviously if they're already entrenched in a stack, work around that - but this page is designed more for greenfield

## Source Systems & Version Control

### Version Control: GitHub

**Description**: Industry-standard Git-based version control platform that enables collaborative development, automated workflows via Actions, and comprehensive project management. For nonprofits, GitHub provides the foundation for managing code, documentation, and automating data pipelines while maintaining transparency and audit trails.

**Why This Choice**: GitHub's nonprofit program, robust CI/CD capabilities, and extensive integration ecosystem make it the clear winner for version control and DevOps workflows in analytics engineering.

**Reference**:
- GitHub for Nonprofits ([link](https://github.com/solutions/industry/nonprofits)):
  - Free GitHub Team plan
  - 25% off GitHub Enterprise Cloud plan

### CRM Option 1 (scrappy): Airtable

**Description**: Hybrid spreadsheet-database platform that combines the familiarity of spreadsheets with relational database capabilities. Ideal for smaller nonprofits or those getting started with structured data management. Offers native integrations, automation workflows, and collaborative features without requiring technical expertise.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Low learning curve for non-technical users
- Built-in forms, automation, and basic reporting
- API access for data extraction
- Strong nonprofit discount program

**Cons**:

- Limited scalability for complex data models
- Basic reporting capabilities compared to dedicated BI tools
- Can become expensive as data volume grows
- Less robust security and compliance features
</details><br>

**Best For**: Nonprofits with < 500 donors, simple program tracking needs, or those transitioning from spreadsheets.

**Reference**:
- Airtable for Nonprofits: ([link](https://support.airtable.com/docs/nonprofit-and-educational-plans-faqs))
  - For 501(c)(3)'s, and doesn't apply to religious organizations or healthcare

### CRM Option 2: Salesforce

**Description**: Enterprise-grade CRM platform with specialized Nonprofit Cloud designed for complex fundraising, program management, and donor stewardship. Offers advanced automation, comprehensive reporting, and extensive third-party integrations. The platform provides purpose-built objects for nonprofits like donations, grants, and volunteer management.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Industry-leading CRM with nonprofit-specific features
- Extensive customization and automation capabilities
- Strong security and compliance features
- Robust API and integration ecosystem
- Comprehensive reporting and analytics

**Cons**:

- Steep learning curve requiring dedicated admin resources
- Can be complex to implement and maintain
- Limited customization on free Power of Us licenses
- May be overkill for smaller organizations
</details><br>

**Best For**: Nonprofits with >$1M annual revenue, complex fundraising needs, or multiple programs requiring sophisticated tracking.

**Reference**:
- Main page ([link](https://www.salesforce.com/nonprofit/))
- [Power of Us Program](https://www.salesforce.com/company/power-of-us/) Program provides qualified nonprofits 10 free licenses of Nonprofit Cloud Enterprise Edition
  - Eligibility guidelines: https://www.salesforce.com/content/dam/web/en_us/www/documents/company/p10-eligibility-guidelines-English-2023.pdf

## Data Ingestion & Transformation

### Airbyte

**Description**: Open-source data integration platform that provides 300+ pre-built connectors for extracting data from various sources into your data warehouse. Offers both self-hosted and cloud options, with a focus on ELT (Extract, Load, Transform) patterns that work well with modern data stacks.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Large library of pre-built connectors including nonprofit-specific sources
- Open-source with commercial support options
- Strong community and rapid connector development
- Handles schema evolution and data typing automatically
- Cost-effective for high-volume data movement

**Cons**:

- Requires technical expertise to set up and maintain
- Self-hosted option requires infrastructure management
- Some connectors may have limitations or bugs
- Cloud version can become expensive with high data volumes
</details><br>

**Best For**: Organizations with diverse data sources, technical teams, or those requiring custom connector development.

**Reference**:
- [Airbyte Documentation](https://docs.airbyte.com/)
- [Airbyte Connector Catalog](https://docs.airbyte.com/integrations/)

### dbt

**Description**: Data transformation tool that enables analytics engineers to transform raw data using SQL and software engineering best practices. Provides version control, testing, documentation, and lineage tracking for data transformations. The de facto standard for transformation in modern data stacks.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- SQL-based transformations accessible to analysts
- Built-in testing, documentation, and lineage
- Strong version control and collaboration features
- Extensive package ecosystem
- Excellent integration with modern data warehouses

**Cons**:

- Requires SQL expertise and analytics engineering knowledge
- Learning curve for traditional BI developers
- Limited support for non-SQL transformations
- Can become complex with large transformation projects
</details><br>

**Best For**: Any organization implementing a modern data stack with dedicated analytics engineering resources.

**Reference**:
- [dbt Documentation](https://docs.getdbt.com/)
- [dbt Community](https://www.getdbt.com/community/)

## Cloud Data Platform

### Option 1: Snowflake

**Description**: Cloud-native data warehouse designed for scalability, performance, and ease of use. Offers separate compute and storage scaling, multi-cluster architecture, and strong security features. Supports both structured and semi-structured data with built-in JSON and XML handling.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Excellent performance and scalability
- Pay-per-use pricing model
- Strong security and compliance features
- Easy to manage with minimal DBA requirements
- Excellent SQL support and analytics functions
- Strong ecosystem of integrations and tools

**Cons**:

- Can be expensive for high-volume, constant workloads
- Requires understanding of compute scaling for cost optimization
- Limited built-in visualization capabilities
- Newer platform with evolving feature set
</details><br>

**Best For**: Organizations with variable workloads, need for rapid scaling, or complex analytical requirements.

**Reference**:
- [Snowflake website](https://www.snowflake.com)
- [Snowflake Pricing](https://www.snowflake.com/en/pricing/)

### Option 2: BigQuery

**Description**: Google's serverless, highly scalable data warehouse with built-in machine learning capabilities. Offers seamless integration with Google Cloud ecosystem, automatic scaling, and pay-per-query pricing. Includes built-in geospatial and time-series analytics functions.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Serverless architecture with automatic scaling
- Pay-per-query pricing can be cost-effective
- Built-in ML capabilities (BigQuery ML)
- Excellent integration with Google Workspace and other Google services
- Strong geospatial and time-series analytics
- Generous free tier

**Cons**:

- Can be expensive for frequent, large queries
- Query costs can be unpredictable
- Limited control over performance optimization
- Proprietary SQL dialect with some limitations
- Data egress costs for moving data out
</details><br>

**Best For**: Organizations already using Google Workspace, need for built-in ML, or those with sporadic analytical workloads.

**Reference**:
- [BigQuery Pricing](https://cloud.google.com/bigquery/pricing)

## Analytics, BI, Reporting

### Tableau

**Description**: Industry-leading data visualization and business intelligence platform that enables self-service analytics through drag-and-drop interface. Offers powerful visualization capabilities, advanced analytics features, and strong data connectivity. Provides both desktop and cloud-based solutions.

<details><summary>Expand to see Pros & Cons</summary>

**Pros**:

- Intuitive drag-and-drop interface for non-technical users
- Extensive visualization options and customization
- Strong data connectivity and live connection capabilities
- Active community and extensive learning resources
- Robust security and governance features
- Excellent nonprofit pricing through TechSoup

**Cons**:

- Can be expensive for large deployments
- Requires training for advanced features
- Performance can degrade with large datasets
- Limited data preparation capabilities compared to specialized tools
- Complex licensing model
</details><br>

**Best For**: Organizations with diverse visualization needs, non-technical end users, or those requiring advanced analytics capabilities.

**Reference**:
- 2 year Desktop license via techsoup.org for Nonprofits for $74: https://www.techsoup.org/products/tableau-desktop-and-tableau-prep-builder-g-49474-
- Tableau Accelerators for Nonprofits: https://exchange.tableau.com/accelerators?version=2021.2&category=Non-for-Profit

---

## Recommended Architecture Patterns

Starter Stack (Budget <$10K/year)

- **CRM**: Airtable
- **Data Warehouse**: BigQuery (free tier)
- **Transformation**: dbt Core (free)
- **Visualization**: Tableau Desktop via TechSoup
- **Version Control**: GitHub (free nonprofit plan)

Growth Stack (Budget $10K-50K/year)

- **CRM**: Salesforce Nonprofit Cloud
- **Data Integration**: Airbyte Cloud
- **Data Warehouse**: Snowflake or BigQuery
- **Transformation**: dbt Cloud
- **Visualization**: Tableau Cloud or Power BI
- **Version Control**: GitHub Team

Enterprise Stack (Budget >$50K/year)

- **CRM**: Salesforce Nonprofit Cloud with advanced features
- **Data Integration**: Airbyte Cloud + custom connectors
- **Data Warehouse**: Snowflake with multiple environments
- **Transformation**: dbt Cloud with advanced features
- **Visualization**: Tableau Cloud + embedded analytics
- **Version Control**: GitHub Enterprise
- **Data Governance**: Additional tools for cataloging and lineage

## Implementation Considerations

Technical Expertise Required

- **Low**: Airtable + Tableau Desktop (basic)
- **Medium**: Full modern data stack with dbt
- **High**: Custom integrations and advanced analytics

Data Volume Considerations

- **<1GB**: Airtable + BigQuery free tier
- **1GB-1TB**: Snowflake or BigQuery with proper optimization
- **\>1TB**: Enterprise-grade solutions with dedicated optimization

Compliance Requirements

- **Basic**: Standard cloud security features
- **HIPAA/SOX**: Enterprise platforms with additional security controls
- **International**: Consider data residency requirements
