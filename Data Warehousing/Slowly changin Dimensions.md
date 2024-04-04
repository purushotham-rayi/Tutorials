# Slowly Changing Dimensions

* Slowly Changing Dimensions (SCD) is a concept in data warehousing that refers to the methods and techniques used to manage changes to data over time in a dimensional data model, typically in a data warehouse or data mart environment.
* In a dimensional model, data is organized into dimensions (descriptive attributes) and facts (numerical measures).
* As the source data changes over time, it becomes necessary to track these changes in the data warehouse to maintain historical accuracy and enable meaningful analysis.

There are different types of Slowly Changing Dimensions from **SCD 0** to **SCD 6**:


# SCD 0: No Changes:

The dimension is considered static and never changes.

In SCD 0, if there is a change in the source system, the change is not implemented in the warehouse system.
Usually, SCD 0 is implemented when the source data never changes or when changes in source system is not relevant anymore. 


