# Authority - Snowflake Data Architecture

**Type:** Vendor / Industry Expertise
**Source:** [Snowflake](https://www.snowflake.com)
**Owner:** Adam Gautier <adam@gautier.org>

## Links

- [Snowflake Data Architecture Principles](https://www.snowflake.com/trending/data-architecture-principles)
- O'Reilly Report - Architecting Data Intensive SaaS Applications -- [Snowflake](https://www.snowflake.com) & [O'Reilly](https://oreilly.com)


## Decomposition

### Consider Data a Shared Resource

Eliminating regional, business unit, and departmental data silos is the surest way to ensure organizational stakeholders can access the d
ata they need to drive insights and also receive a 360 degree view of the business.

### Ensure Security and Control Access

Data platforms such as Snowflake allow data governance and access controls at the raw data level, eliminating ad-hoc 
security further down the data pipeline. With today's demands for widely available real-time data, highly secure self-service 
access is increasingly become a necessity.

### Reduce or Eliminate Data Movement and Replication

Any time data is moved or copied, precious time and resources are consumed and data fidelity is potentially compromised. Modern 
data platforms require MPP (massively parallel processing) to support a multi-workload, multi-structure environments, They also need to 
support high user concurrency across disparate units and/or geographies. The only way to achieve this is through a cloud data platform 
that can leverage economies of scale (up, down, or out) to meet fluctuating business workload requirements.

#### Principles

- [Data Instances](https://github.com/gautada/celsus/blob/main/principles/DataInstances.md)


