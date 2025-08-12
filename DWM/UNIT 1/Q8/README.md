📘 1.14.2 Factless Fact Table

    •	Factless table means only the key available in the Fact there is no measures available.
    •	Used only to put relation between the elements of various dimensions.
    •	Are useful to describe events and coverage, i.e. the tables contain information that something has/has not happened.
    •	Often used to represent many-to-many relationships.
    •	The only thing they contain is a concatenated key, they do still however represent a focal event which is identified by the combination of conditions referenced in the dimension tables.

⸻

📊 An Example of Factless Fact Table

An Example of Factless fact table can be seen in the Fig. 1.14.1.
⸻

🔍 There are two main types of factless fact tables:

⸻

1. Event tracking tables
   • Use a factless fact table to track events of interest to the organization.
   For example, attendance at a cultural event can be tracked by creating a fact table containing the following foreign keys (i.e. links to dimension tables):
   event identifier, speaker/entertainer identifier, participant identifier, event type, date.
   This table can then be queried to find out information, such as which cultural events or event types are the most popular.
   • Following example shows factless fact table which records every time a student attends a course or
   • Which class has the maximum attendance? or
   • What is the average number of attendance of a given course?
   • All the queries are based on the COUNT() with the GROUP BY queries.
   So we can first count and then apply other aggregate functions such as AVERAGE, MAX, MIN.
   ⸻

2. Coverage Tables
   • The other type of factless fact table is called Coverage table by Ralph.
   • It is used to support negative analysis report.
   For example, a Store that did not sell a product for a given period.
   To produce such report, you need to have a fact table to capture all the possible combinations.
   You can then figure out what is missing.

📝 Common examples of factless fact table:
• Ex-Visitors to the office.
• List of people for the web click.

Fact Constellation
• As its name implies, it is shaped like a constellation of stars (i.e., star schemas).
• This schema is more complex than star or snowflake varieties, which is due to the fact that it contains multiple fact tables.
• This allows dimension tables to be shared amongst the fact tables.
• A schema of this type should only be used for applications that need a high level of sophistication.
• For each star schema or snowflake schema it is possible to construct a fact constellation schema.
• That solution is very flexible, however it may be hard to manage and support.
• The main disadvantage of the fact constellation schema is a more complicated design because many variants of aggregation must be considered.
• In a fact constellation schema, different fact tables are explicitly assigned to the dimensions, which are for given facts relevant.
• This may be useful in cases when some facts are associated with a given dimension level and other facts with a deeper dimension level.
• Use of that model should be reasonable when for example, there is a sales fact table (with details down to the exact date and invoice header id) and a fact table with sales forecast which is calculated based on month, client id and product id.
• In that case using two different fact tables on a different level of grouping is realized through a fact constellation model.
