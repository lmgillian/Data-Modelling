## Fundamental Concepts
1. Why is it important to gather business requirements and understand data realities before starting a dimensional modeling effort?
2. How do business objectives, key performance indicators, and decision-making processes influence the dimensional modeling process?
3. What role do business representatives and source system experts play in the dimensional modeling process?
4. Why are collaborative dimensional modeling workshops essential, and who should be involved in these sessions?
5. What are the four key decisions made during the design of a dimensional model?
6. How does selecting the business process impact the design of a dimensional model?
7. Why is declaring the grain considered the pivotal step in dimensional design?
8. What consistency must be maintained between the grain, dimensions, and facts in a dimensional model?
9. How do dimensions provide context for business process events in a data warehouse?
10. Why are dimensions sometimes referred to as the "soul" of the data warehouse?
11. What are facts in the context of a dimensional model, and what characteristics do they typically have?
12. How does a fact table relate to a physical observable event?
13. What is a star schema, and how is it typically implemented in a relational database management system?
14. How does an OLAP cube differ from a relational star schema, and what languages are used to access it?
15. Why might an OLAP cube be the final step in deploying a dimensional DW/BI system?
16. How can dimensional models be extended gracefully when data relationships change?
17. What changes can be implemented in a dimensional model without altering existing BI queries or applications?
18. How can facts be added to an existing fact table without changing the grain?
19. What considerations must be taken into account when adding dimensions or attributes to an existing dimensional model?
20. How can the grain of a fact table be made more atomic, and what precautions should be taken to preserve existing queries?

## Basic Fact Table Techniques
1. What is the fundamental design of a fact table based on, and why is it not influenced by eventual reports?
2. What types of keys and stamps do fact tables always contain besides numeric measures?
3. How are additive, semi-additive, and non-additive facts categorized in a fact table?
4. What is a recommended approach for handling non-additive facts in a fact table?
5. Why must nulls be avoided in the fact table's foreign keys, and how is the unknown or not applicable condition represented?
6. What are conformed facts, and why is it important to ensure their technical definitions are identical?
7. What does a row in a transaction fact table correspond to, and what must the measured numeric facts be consistent with?
8. How does a periodic snapshot fact table summarize measurement events, and what is its typical grain?
9. What type of fact table summarizes the measurement events occurring at predictable steps in a process, and how is it unique?
10. What are factless fact tables, and how can they be used to analyze events that did not happen?
11. What is the purpose of aggregate fact tables or OLAP cubes, and how do they relate to query performance?
12. When is it convenient to use consolidated fact tables, and what are the trade-offs involved in their use?

## Basic Dimension Table Techniques
1. What is the structure of a dimension table and what types of attributes does it typically contain?
2. Why are surrogate keys used in dimension tables instead of operational system's natural keys?
3. What are natural, durable, and supernatural keys, and why are durable keys important in a data warehouse?
4. What does "drilling down" mean in the context of analyzing data, and how is it performed?
5. What are degenerate dimensions and in what scenarios are they commonly used?
6. Why do dimensional designers denormalize dimension tables, and what are the benefits of this approach?
7. How can multiple hierarchies coexist in the same dimension table?
8. Why should flags and indicators in dimension tables be supplemented with full text descriptions?
9. How should null-valued dimension attributes be handled, and why?
10. What is the role of a calendar date dimension in a data warehouse, and how is it typically structured?
11. What are role-playing dimensions, and how are they used in a fact table?
12. What is a junk dimension, and when should it be used?
13. Why should snowflaked dimensions be avoided, and what is the preferred alternative?
14. What are outrigger dimensions, and when is it appropriate to use them?

## Integration via Conformed Dimensions
1. What are conformed dimensions and how do they enable integration of data from different business processes?
2. How can information from separate fact tables be combined in a single report using conformed dimensions?
3. What is the role of conformed attributes in aligning results from separate fact tables in a drill-across report?
4. Why are shrunken dimensions necessary when constructing aggregate fact tables or capturing data at a higher level of granularity?
5. What does "drilling across" involve, and how is it performed using conformed attributes?
6. How does a value chain identify the flow of an organization's primary business processes, and how does it relate to fact tables?
7. What is the enterprise data warehouse bus architecture, and how does it provide an incremental approach to building the DW/BI system?
8. How is the enterprise data warehouse bus matrix used to design and communicate the bus architecture?
9. What additional details are provided in the detailed implementation bus matrix compared to the enterprise data warehouse bus matrix?
10. How does the opportunity/stakeholder matrix assist in identifying which business groups should be involved in the design sessions for each business process?

## Dealing with Slowly Changing Dimension Attributes
1. What is Type 0 SCD and when is it appropriate to use this technique?
2. How does Type 1 SCD handle changes in dimension attributes, and what is the impact on historical data?
3. What additional columns should be added to a dimension row when implementing Type 2 SCD?
4. How does Type 3 SCD preserve old attribute values, and what is an alternate reality in this context?
5. When is the Type 4 SCD technique used, and what is a rapidly changing monster dimension?
6. What is the purpose of the Type 5 SCD technique, and how does it build on Type 4?
7. How does Type 6 SCD deliver both historical and current dimension attribute values?
8. What is Type 7 SCD, and how does it support both as-was and as-is reporting?
9. In Type 7 SCD, how are the two perspectives (as-was and as-is) deployed to BI applications?
10. For each SCD type, what are the implications for ETL processing and fact table design?

## Dealing with Dimension Hierarchies
1. What is a fixed depth positional hierarchy and when should it be used in a dimension table?
2. How do you handle a fixed depth hierarchy when the hierarchy levels have agreed upon names?
3. What is a slightly ragged or variable depth hierarchy, and how can it be modeled in a dimension table?
4. What are the limitations of using SQL extensions and OLAP access languages for ragged hierarchies of indeterminate depth?
5. How can a hierarchy bridge table overcome the limitations of SQL extensions for ragged hierarchies?
6. What is a pathstring attribute, and how does it facilitate the handling of ragged variable depth hierarchies without SQL language extensions?
7. What are the limitations of the pathstring approach for modeling ragged hierarchies?
8. How does the pathstring approach affect the ability to handle alternative hierarchies or shared ownership hierarchies?
9. What are the potential vulnerabilities of the pathstring approach when there are structure changes in the ragged hierarchy?

## Advanced Fact Table Techniques
1. What are fact table surrogate keys and when might they be useful?
2. Why should centipede fact tables be avoided, and what is the preferred alternative?
3. How should numeric values be handled when they don't clearly fall into either the fact or dimension attribute categories?
4. What are lag/duration facts, and how can they be effectively stored in accumulating snapshot fact tables?
5. How should header/line schemas be modeled in fact tables?
6. What is the recommended approach for dealing with allocated facts of differing granularity in header/line transaction data?
7. Why are profit and loss fact tables challenging to build, and when in the DW/BI program implementation should they be tackled?
8. How should fact tables that record financial transactions in multiple currencies be structured?
9. What is the recommended technique for handling multiple units of measure facts?
10. Why is it preferable to calculate year-to-date metrics in BI applications or OLAP cubes rather than storing YTD facts in the fact table?
11. Why must BI applications avoid issuing SQL that joins two fact tables together, and what is the correct technique to use instead?
12. In what scenarios might timespan tracking be added to fact tables, and what additional columns are required?
13. How should late arriving facts be handled to ensure they are associated with the correct dimensional context?

## Advanced Dimension Techniques
1. When might surrogate keys be used in fact tables, and what are their benefits?
2. What is a centipede fact table, and why is it not recommended?
3. How should numeric values that don't clearly fall into fact or dimension attribute categories be handled?
4. What are lag/duration facts, and how are they used in accumulating snapshot fact tables?
5. How should header/line schemas be modeled in operational transaction systems?
6. What is the recommended approach for handling allocated facts in header/line transaction data?
7. How should profit and loss fact tables be structured to expose the full equation of profit?
8. How should fact tables that record financial transactions in multiple currencies be structured?
9. What technique is recommended for handling multiple units of measure facts?
10. Why is it preferable to calculate year-to-date metrics in BI applications rather than storing them in the fact table?
11. Why should BI applications avoid joining two fact tables together, and what technique should be used instead?
12. How can timespan tracking be implemented in fact tables, and what additional columns are required?
13. How should late arriving facts be handled to ensure they are associated with the correct dimensional context?

## Special Purpose Schemas
1. What are supertype and subtype schemas, and when are they needed in data warehousing?
2. How do financial services and other businesses use supertype and subtype schemas for heterogeneous products?
3. What is the solution for building a fact table that can accommodate a wide variety of products with divergent attributes?
4. What are real-time fact tables, and what techniques support frequent updates beyond traditional nightly batch processes?
5. How can a "hot partition" be used in a real-time fact table, and what are its characteristics?
6. What is an error event schema, and how does it contribute to managing data quality in a data warehouse?
7. What is the grain of an error event fact table, and how is it associated with an error event detail fact table?