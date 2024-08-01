## Goals of Data Warehousing and Business Intelligence
1. What are the primary concerns of business management that drive the requirements for a DW/BI system?
2. How does the DW/BI system ensure that information is easily accessible and understandable to business users?
3. Why is it important for the DW/BI system to present information consistently, and what does this imply about data labels and definitions?
4. In what ways must the DW/BI system adapt to change without disrupting existing data or applications?
5. What are the expectations for the timeliness of data conversion into actionable information in a DW/BI system?
6. How does the DW/BI system protect an organization's confidential information, and why is this important?
7. Why is it crucial for the DW/BI system to be seen as an authoritative and trustworthy foundation for decision-making?
8. What determines the success of a DW/BI system in terms of business community acceptance?
9. How does the role of a DW/BI manager compare to that of a publishing editor-in-chief, and what are the key responsibilities?
10. Why is it important for a DW/BI manager to focus on serving business users rather than solely on technology and processes?
11. What are the potential consequences of omitting any single responsibility from the DW/BI manager's role?

## Dimensional Modeling Introduction
1. What are the two simultaneous requirements that dimensional modeling aims to address?
2. Why is simplicity critical in dimensional modeling, and how does it benefit both users and software?
3. How does dimensional modeling differ from third normal form (3NF) models, and why are 3NF models less suitable for BI queries?
4. What is the difference between star schemas and OLAP cubes in the context of dimensional modeling?
5. Why is a star schema often recommended as the physical foundation for building an OLAP cube?
6. What are the key considerations to keep in mind when deploying data into OLAP cubes?
7. What is the primary role of a fact table in a dimensional model, and what is the importance of maintaining a consistent grain?
8. Why are additive facts crucial in a dimensional model, and how are semi-additive and non-additive facts handled?
9. How should textual data be treated in a dimensional model, and why is it typically not stored in fact tables?
10. What is the purpose of dimension tables in a dimensional model, and what type of information do they contain?
11. How do dimension attributes contribute to the usability and understandability of the DW/BI system?
12. What is the significance of hierarchical relationships within dimension tables, and why is denormalization preferred over snowflaking?
13. How do facts and dimensions come together in a star schema, and what are the benefits of this structure?
14. In what ways are dimensional models extensible to accommodate change, and how does this impact existing BI applications?
15. How can you translate the complementary nature of fact and dimension tables into a report, and what would the SQL query look like for such a report?

## Kimball's DW/BI Architecture
1. What are the four distinct components of the Kimball DW/BI architecture?
2. What is the role of operational source systems in the DW/BI environment?
3. Describe the process and significance of the Extract, Transformation, and Load (ETL) system in a DW/BI environment.
4. Why is it important to cleanse and conform data during the ETL process, and how does it add value to the data?
5. What are the potential drawbacks of creating both normalized structures for ETL processing and dimensional structures for the presentation area?
6. What is the purpose of the presentation area in a DW/BI system, and what should it contain?
7. Why is it essential for the presentation area to include detailed, atomic data alongside aggregated data?
8. How does the concept of conformed dimensions contribute to the success of a DW/BI system?
9. What is the enterprise data warehouse bus architecture, and why is it important?
10. Explain the role of business intelligence (BI) applications in the DW/BI architecture.
11. How does the restaurant metaphor illustrate the separation of components in the DW/BI environment?
12. In the restaurant metaphor, what does the ETL system represent, and why is it kept off-limits to business users?
13. What qualities are important in the "dining room" of the DW/BI system, and how do they relate to the presentation area and BI applications?
14. How can DW/BI managers ensure that the system meets the needs of its users and avoids becoming obsolete?
15. What are the consequences of not proactively managing user satisfaction in a DW/BI environment?

## Alternative DW/BI Architectures
1. What are the two dominant architectural alternatives to the Kimball DW/BI architecture?
2. How does the independent data mart approach differ from the Kimball architecture, and what are its potential drawbacks?
3. Why is the independent data mart approach prevalent despite not being advocated by industry leaders?
4. Describe the hub-and-spoke Corporate Information Factory (CIF) architecture and its core elements.
5. How does the CIF architecture's approach to data integration differ from the Kimball architecture's approach?
6. In the CIF architecture, what is the role of the Enterprise Data Warehouse (EDW), and how is it typically used by business users?
7. What are the potential issues with business users accessing the EDW directly in the CIF architecture?
8. How do the downstream reporting and analytic environments in the CIF architecture typically differ from the Kimball architecture's presentation area?
9. Explain the concept of a hybrid hub-and-spoke and Kimball architecture and how it combines elements from both approaches.
10. What are the claimed benefits of the hybrid architecture, and under what circumstances might it be appropriate?
11. If an organization has already invested in a 3NF EDW that is not meeting user expectations, what might be a suitable architectural approach?
12. What are the considerations and potential costs associated with starting a DW/BI project with a hybrid architectural approach?
13. How does the hybrid approach address the performance and usability issues associated with a 3NF EDW?
14. Why might an organization choose to fully normalize and instantiate data before loading it into dimensional structures?
15. What are the implications of adopting a hybrid approach in terms of development time, operational costs, and organizational patience?

## Dimensional Modeling Myths
1. Why is the belief that dimensional models are only for summary data incorrect, and what role should detailed data play in dimensional models?
2. How does the corollary to Myth 1 about historical data storage in dimensional structures relate to business requirements?
3. What is the misconception behind Myth 2 regarding dimensional models being departmental rather than enterprise-wide?
4. How should dimensional models be organized to support enterprise analytics effectively?
5. What evidence counters Myth 3 that dimensional models are not scalable?
6. How do dimensional models maintain the ability to answer the same questions as normalized models?
7. Why is Myth 4, which states that dimensional models are only for predictable usage, a misunderstanding?
8. How should dimensional models be designed to accommodate evolving business analyses and reporting needs?
9. What is the impact of designing dimensional models based on a predefined list of reports?
10. How does building fact tables at the most granular level contribute to the flexibility and adaptability of dimensional models?
11. What does the quote "God is in the details" imply about the level of detail necessary in dimensional models?
12. Why is Myth 5, which claims that dimensional models can't be integrated, false?
13. What is the role of conformed dimensions in the integration of dimensional models?
14. How does the enterprise data warehouse bus architecture facilitate the integration of dimensional models?
15. What are the consequences of not adhering to the bus architecture with shared conformed dimensions in dimensional modeling?

## More Reasons to Think Dimensionally
1. Why is it important to focus on business processes rather than specific reports or dashboard gauges when gathering requirements for a DW/BI initiative?
2. How should the scope of a DW/BI project be defined in relation to business processes?
3. What mindset shift is necessary for both IT and business management when rolling out a DW/BI system?
4. How should business processes be prioritized when developing a DW/BI roadmap, and what role does the DW/BI team play in this process?
5. What is the significance of the enterprise data warehouse bus matrix in the context of DW/BI system data architecture?
6. How can the bus matrix be used to advocate for a master data management platform?
7. In the context of data stewardship or governance programs, why should the focus be on major dimensions first?
8. How does identifying the central nouns used to describe the business help in establishing data governance efforts?
9. What is the relationship between robust dimensions and the effectiveness of a DW/BI system?
10. How do dimensional modeling concepts influence the design of star schemas or OLAP cubes?
11. Why is it crucial for the dimensional model to remain a focus during the design of the ETL system and BI applications?
12. How do dimensional modeling concepts facilitate the linkage between business and technical communities in DW/BI projects?
13. What are the benefits of having a dimensional mindset throughout the entire lifecycle of a DW/BI project?
14. How can thinking dimensionally early in the project lifecycle benefit the overall outcome of a DW/BI initiative?
15. What are the key tasks and considerations for a DW/BI team when implementing dimensional modeling principles in their projects?

## Agile Considerations
1. How do agile practices align with delivering business value in DW/BI projects?
2. What role does the enterprise data warehouse bus matrix play in agile DW/BI planning?
3. How do conformed dimensions support agile development cycles in DW/BI?
4. What strategies can DW/BI teams use to avoid creating isolated data silos with agile methods?
5. How can DW/BI teams balance agility with the need for consistent and integrated data?

