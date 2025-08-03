Q5. What is meant by Metadata in the context of a Data warehouse? Explain the different types of
metadata stored in a data warehouse. Illustrate with a suitable example.

Metadata in a data warehouse is structured information that describes, explains, locates, or otherwise makes it easier to retrieve, use, or manage data within the warehouse system. It acts as a blueprint or reference that provides context and meaning to the data stored in the warehouse.
 First, it acts as the glue that connects all parts of the data warehouse.
 Next, it provides information about the contents and structures to the developers.
 Finally, it opens the door to the end-users and makes the contents recognizable in their own terms.

Metadata in a data warehouse fall into three major categories:
Operational Metadata
Extraction and Transformation Metadata  
End-User Metadata
Operational Metadata. As you know, data for the data warehouse comes from several operational systems of the enterprise. These source systems contain different data struc- tures. The data elements selected for the data warehouse have various field lengths and data types. In selecting data from the source systems for the data warehouse, you split records, combine parts of records from different source files, and deal with multiple cod- ing schemes and field lengths. When you deliver information to the end-users, you must be able to tie that back to the original source data sets. Operational metadata contain all of this information about the operational data sources.

Extraction and Transformation Metadata. Extraction and transformation metada- ta contain data about the extraction of data from the source systems, namely, the extrac- tion frequencies, extraction methods, and business rules for the data extraction. Also, this category of metadata contains information about all the data transformations that take place in the data staging area.

End-User Metadata. The end-user metadata is the navigational map of the data ware- house. It enables the end-users to find information from the data warehouse. The end-user metadata allows the end-users to use their own business terminology and look for infor- mation in those ways in which they normally think of the business.
.
