-Dimensional modeling: is a database design technique to support business users to query data in data warehouse. The dimensional modeling is developed to be oriented around query performance and easy of use .

-In dimensional modeling, there are two important concepts: facts and dimensions.

-Facts are also known as business measurements. Facts are normally (but not always) numeric values which could be aggregated. Example of fact could be number of units sold.

-Dimensions are called context. Dimensions are business descriptors which specify the facts, for example product name, brand, quarter, etc. are components of dimensions.

-The dimensional data model is built based on star schema with a fact table at the center surrounded by a number of dimension tables. The following four-step process is commonly used in dimensional modeling design:
Select the business process
Declare the Grain
Identify the dimensions
Identify the Fact

Let’s examine each step in the modeling process in a great detail.

1. Select the Business Process
   The first step is to identify and select the business process that is to be modeled. This could be a sales process, inventory tracking, order processing, etc. A business process is an operational activity that is important for decision making and performance analysis.
2. Declare the Grain
   Declaring the grain means defining exactly what a single row in the fact table represents. This step sets the level of detail (granularity) for the data. For example, the grain might be “one row per sales transaction” or “one row per product per day.”
   Declaring the grain ensures consistency and clarity in the data warehouse design, as all dimension and fact data will align to this defined level of detail.
3. Identify the dimensions :
   in the third step, we add number of dimensions that represents all possible descriptions which take on single values in the context of each fact in the fact table. Date, time, product, customer, store… are several good examples of common dimensions.
4. Identify the facts :
   in the last step, we select the numeric facts that will be loaded into each fact table row. To identify the fact we need to answer the question “What are KPIs of the business process?” or “What are we measuring?”

---------Benefits of Dimensional Modeling

1. Dimensional model have proved to be more understandable : in dimensional model, data is grouped into coherent dimensions that make it easy to read and interpret by business users.

2. Dimensional model allows boost query performance : the dimensional model is more de-normalized therefore it is optimized for querying. In addition, the predictable framework of a dimensional model allows database engine to make strong assumption about the data that will help to boost query performance.
