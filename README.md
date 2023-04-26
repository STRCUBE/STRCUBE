CS605-2023-01 STRCUBE Stream/Cube Streaming Data Warehouse.

Our Project is entitled as ‘STRCUBE’ - Stream / Cube : Streaming Data Warehouse designed and developed for real time data analysis by which organizations dealing with high frequency, infinite volume, transient nature data arriving typically from many data sources are able to make better and more informed decisions based on insights gained from real time analysis of this system.

A data stream is a real-time, continuous, ordered (implicitly by arrival time or explicitly by timestamp) sequence of items. It is impossible to control the order in which items arrive, nor is it feasible to locally store a stream in its entirety. Likewise, queries over streams run continuously over a period of time and incrementally return new results as new data arrive. These are known as long-running, continuous, standing, and persistent queries.

<strong>Stream Dimensional Modeling</strong>: The main goal of stream dimensional modeling is to create a data model that accurately represents the business processes and entities involved in a stream processing system.

This involves designing a schema that can efficiently handle large volumes of real-time data, while providing users with the ability to easily access and analyze that data.

The dimensional modeling approach is particularly useful for stream processing systems because it allows for efficient data retrieval and analysis by organizing data into fact tables and dimension tables, which can be easily queried and aggregated. 

Data Model Aspects:

A real-time data stream is a sequence of data items that arrive in some order and may be seen only once. Since items may arrive in bursts, a data stream may instead be modeled as a sequence of lists of elements or data items. Individual stream items may take the form of relational tuples or instantiations of objects.

In relation-based models, data items are transient tuples stored in virtual relations, possibly horizontally partitioned across remote nodes. In object-based models (e.g. COUGAR and Tribeca), sources and item types are modeled as hierarchical data types with associated methods.

In many cases, only an excerpt of a stream is of interest at any given time, giving rise to window models, which may be classified according the the following three criteria:

1. Direction of movement of the endpoints: Two fixed endpoints define a fixed window, two sliding endpoints (either forward or backward, replacing old items as new items arrive) define a sliding window, while one fixed endpoint and one moving endpoint (forward or backward) define a landmark window.
2. Physical vs. logical: Physical, or time-based windows are defined in terms of a time interval, while logical, (also known as count-based) windows are defined in terms of the number of tuples.
3. Update interval: Eager re-evaluation updates the window upon arrival of each new tuple, while batch processing (lazy re-evaluation) induces a “jumping window”. If the update interval is larger than the window size, the result is a series of non-overlapping tumbling windows.

For Stream/ Cube - Dimensional Modeling, we came up with an approach of Hybrid Modeling based on Dimensions as Entities for Dimensional Modeling and also Time/Count-Based Modeling for Sliding Window Implementation.

We have defined Stream Database Properties in xml instance contains:

Stream Properties and
Data warehouse Properties.

We are using mainly two data models in this project:<br/>
Xml Data Model and
Relational (Sql Tables) Data Model.

Architecture:<br/>
<img src="https://iiitbac-my.sharepoint.com/:i:/g/personal/boppana_venkatesh_iiitb_ac_in/EeIgm-tkXCdAjXc1LWORd2oBmNcPwqPYB4G84dYzOCvcUg?e=3ExMvm">
