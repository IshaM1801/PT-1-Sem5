## Data Warehouse vs Data Mart

| **Data Warehouse**                   | **Data Mart**                                   |
| ------------------------------------ | ----------------------------------------------- |
| Corporate/Enterprise-wide            | Departmental                                    |
| Union of all data marts              | A single business process                       |
| Data received from staging area      | Star-join (facts & dimensions)                  |
| Queries on presentation resource     | Technology optimal for data access and analysis |
| Structure for corporate view of data | Structure to suit the departmental view of data |
| Organized on E-R model               |                                                 |

**Figure 2-5**: Data warehouse versus data mart.

## Data Architecture

Data Warehouse Architecture – 5 Mark Answer

The architecture of a data warehouse is composed of several key components that work together to support the collection, transformation, storage, and delivery of data for analysis and decision-making.

1. Production Data

This comes from various operational systems of the enterprise. These systems are often built on different platforms, databases, and formats. Data from them is usually disparate and inconsistent, requiring standardization and transformation before integration into the warehouse.

2. Internal Data

Internal data includes private files, spreadsheets, documents, and departmental databases maintained by users. Though informal, some of this data is useful and needs to be gathered and integrated carefully for customer profiling or detailed analysis.

3. Archived Data

Operational systems archive old data periodically. Archived data is essential for the warehouse to maintain historical snapshots and support trend analysis over time.

4. External Data

Organizations also rely on external data sources such as industry statistics, market share data, and economic indicators. This data is valuable for benchmarking and comparison but needs to be converted to internal formats and managed for consistency.

5. Data Staging Component

This is the ETL workbench—a separate environment where data is extracted, cleaned, transformed, standardized, deduplicated, and summarized before being loaded into the warehouse. It is crucial because warehouse data is subject-oriented and spans across multiple source systems.

6. Data Storage Component

A separate, read-only repository optimized for query performance and storing large volumes of historical data. Unlike operational databases, it stores data in structures suited for analysis, not transactions.

7. Information Delivery Component

Provides multiple methods to access data—ad hoc reports, complex queries, multidimensional (MD) analysis, statistical tools, and Executive Information Systems (EIS)—to serve users ranging from novices to power users.

8. Metadata Component

Stores data about data, such as definitions, mappings, and structures. It is more advanced than a regular data dictionary and is essential for managing and understanding warehouse data.

9. Management and Control Component

This component coordinates and monitors all activities in the warehouse—from ETL to storage and delivery—and interacts closely with metadata to ensure proper functioning and administration.
.
