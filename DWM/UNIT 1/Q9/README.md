Data Extraction/Transformation/Loading (ETL).
The activities that relate to ETL in a data warehouse are by far most time-consuming and human-intensive. Special recognition of the extent and complexity of these activities in the requirements will go a long way in easing the pain while setting up the architecture. Let us separate out the functions and state the special considerations needed in the requirements definition.

Data Extraction.
Clearly identify all the internal data sources. Specify all the computing platforms and source files from which the data is to be extracted. If you are going to include external data sources, determine the compatibility of your data structures with those of the outside sources. Also indicate the methods for data extraction.

Data Transformation.
Many types of transformation functions are needed before data can be mapped and prepared for loading into the data warehouse repository. These functions include input selection, separation of input structures, normalization and denormalization of source structures, aggregation, conversion, resolving of missing values, and conversions of names and addresses. In practice, this turns out to be a long and complex list of functions. Examine each data element planned to be stored in the data warehouse against the source data elements and ascertain the mappings and transformations.

Data Loading.
Define the initial load. Determine how often each major group of data must be kept up-to-date in the data warehouse. How much of the updates will be nightly updates? Does your environment warrant more than one update cycle in a day? How are the changes going to be captured in the source systems? Define how the daily, weekly, and monthly updates will be initiated and carried out.
