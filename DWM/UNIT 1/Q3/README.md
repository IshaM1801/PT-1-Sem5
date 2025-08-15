---
# **Data Warehouse Architecture**

Architecture is the proper arrangement of the components in a data warehouse.
It defines the **flow of data** from operational systems to the delivery of information to business users.
A complete data warehouse consists of several main building blocks, each performing specific functions to ensure data is **consistent, integrated, historical, and easily retrievable**.
---

## **1. Source Data**

The architecture begins with the **source data** — the origin of all information in the warehouse.

- **Production Data:**

  - Extracted from various operational systems that run day-to-day business operations.
  - Includes sales, inventory, payroll, accounting, order entry, and customer service systems.
  - May reside on multiple platforms, using different DBMS, file systems, and operating systems.
  - The same data item may have different meanings across systems
    _(e.g., “account” in billing may differ from “account” in finance)_.
  - Requires **careful standardization and data conversion**.

- **Internal Data:**

  - Generated within departments — spreadsheets, word processing files, small desktop databases.
  - May contain valuable business insights despite being informal.
  - Only selected parts are included after proper evaluation and conversion.

- **Archived Data:**

  - Historical snapshots stored in offline storage (tapes, optical disks, historical relational databases).
  - Includes closed transactions or data from obsolete systems.
  - Essential for **trend analysis** and **long-term forecasting**.

- **External Data:**

  - Acquired from outside sources — industry benchmarks, market research, demographics, stock market feeds.
  - Often in incompatible formats → requires **reformatting, standardization, and staging**.

---

## **2. Data Staging Component**

Intermediate storage and processing area where **raw source data** is transformed into the integrated form required for the warehouse.

**Key Functions:**

- **Data Extraction:**

  - Pulling data from operational databases, flat files, spreadsheets, and external feeds.
  - Scheduled to minimize disruption to production systems.

- **Data Transformation:**

  - **Data cleansing:** remove errors, resolve duplicates.
  - **Standardization:** consistent naming conventions, units of measure.
  - Resolve **synonyms** (same meaning, different names) and **homonyms** (same name, different meaning).
  - Derive new fields, create surrogate keys, summarize details for faster retrieval.

- **Data Loading:**

  - **Initial Load:** large, one-time historical transfer.
  - **Incremental Load:** regular updates — daily, weekly, or monthly.

---

## **3. Data Storage Component**

- Separate from operational databases.
- Contains **integrated, subject-oriented, time-variant, and non-volatile** data.
- Typically in **relational DBMS** for detailed data, and **multidimensional DBMS** for summaries.
- Optimized for **query performance**, not transaction processing.
- Stores both **detailed** and **summary** data.

---

## **4. Information Delivery Component**

Front-end interface for warehouse users.

- **Supports:**

  - **Novice users:** standard reports.
  - **Business analysts:** ad hoc queries, OLAP analysis.
  - **Executives:** dashboards, scorecards, KPIs.

- **Delivery Modes:**

  - Preformatted reports, parameterized queries.
  - EIS systems, web interfaces.
  - Data mining tools for discovering hidden patterns.
  - Distribution via email, intranet, web portals.

---

## **5. Metadata Component**

“Data about data” — directory and guide to warehouse contents.

- **Includes:**

  - Definitions, structures, source descriptions.
  - Transformation rules, data lineage.

- **Types:**

  - **Technical Metadata:** mapping rules, data models, ETL job details.
  - **Business Metadata:** business definitions, valid values, usage guidelines.

---

## **6. Management and Control Component**

- Coordinates and controls all warehouse operations.
- Monitors extraction, transformation, loading, and query performance.
- Uses metadata for scheduling, error handling, optimization.
- Ensures **security, backup, and recovery**.

---
