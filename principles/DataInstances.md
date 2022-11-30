# Principle: One instance of data is preferred over multiple ad-hoc copies of data

## Abstract

Data or a collection of datum is just 1's and 0's. Computing has made the action of copying data inexpensive and and the storage overly easy. However, from a management standpoint this ease and low creates a multitude of problems such as security, consistency, and maintenance. As data grows these problems  grow in complexity because they are interelated and multiply exponentially with a linear increase in the amount of data.

To address, this principle sets forth the idea of a data instance which attempts to allow for conceptually positive benefits of data copies which will lessen need for ad-hoc data copies.  Therefore the complexity will be contained in a finite set of attributes that can be patterned, and referenced repeatidly for scaled consistency.

**Data Instance** is a conceptual map between system, entity, usage(consumption), and life-cycle. The mission of a data instance is to provide an atomic definition for all enterprise level data entities that are required to run the business mapped to a single system(-of-record) with defined consumption and specified life-cycle.  


### Terms

- **Data Instance:** An atomic map between system-entity-usage-life-cycle which limits the need for ad-hoc copies of data.
- **Data Entity:** A high-level system agnostic definition of data
- **System of Record(SOR):** The primary system that initiates the data entity.
- **Data Life-Cycle:** The management and maintenance of data, creation, clean-up, archival, backup, availability, etc.
- 
## Authorities

- [Snowflake Data Architecture](https://github.com/gautada/celsus/blob/main/authorities/SnowflakeDataArchitecture.md)
