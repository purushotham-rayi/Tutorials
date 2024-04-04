# Slowly Changing Dimensions

* Slowly Changing Dimensions (SCD) is a concept in data warehousing that refers to the methods and techniques used to manage changes to data over time in a dimensional data model, typically in a data warehouse or data mart environment.
* In a dimensional model, data is organized into dimensions (descriptive attributes) and facts (numerical measures).
* As the source data changes over time, it becomes necessary to track these changes in the data warehouse to maintain historical accuracy and enable meaningful analysis.

There are three main types of Slowly Changing Dimensions:

    * Type 1: Overwrite
*   Type 2: Add New Row
*   Type 3: Add New Attribute