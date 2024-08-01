## Dimension Triage to Avoid Too Few Dimensions
1. What is the risk of designing a dimensional model with too few dimensions, particularly with only month and account dimensions?
2. Why is it important to include additional analytic dimensions such as product and branch in a dimensional model?
3. How do you determine the appropriate number of dimensions for a dimensional model?
4. What types of dimensions might be missing if a dimensional model has too few dimensions?
5. How can causal, date, degenerate, role-playing, status, audit, and junk dimensions enhance a dimensional model?
6. Why is it usually possible to add new dimensions to a dimensional model without changing the grain of the fact table?
7. What factors influenced the choice of dimensions for the bank's initial schema in the case study?
8. How do you handle multivalued dimensions, such as customers associated with a bank account?
9. Why might a financial services company need to use mini-dimensions for attributes like credit bureau data?
10. How can mini-dimensions be used effectively without overcomplicating the fact table?
11. What is the impact of using mini-dimensions on the ETL process and BI presentation?
12. How do you manage a rapidly changing monster dimension, such as customer demographics, in a bridge table scenario?
13. What is dynamic value banding, and how can it be implemented in a dimensional model for flexible reporting?
14. What challenges might arise when querying for dynamic value bands, and how can performance be optimized?
15. How do agile development practices apply to the process of designing and implementing dimensional models in DW/BI systems?

## Supertype and Subtype Schemas for Heterogeneous Products
1. What challenges arise in financial services due to the heterogeneous nature of products offered?
2. Why is it necessary to have two different perspectives for analyzing accounts in a retail bank?
3. What limitations does a supertype fact table have in terms of the facts it can present?
4. How does the subtype schema address the need for in-depth analysis of a specific line of business?
5. Why is it impractical to include line-of-business-specific facts and attributes in a supertype fact table or dimension?
6. How do business users interact with supertype and subtype schemas during their analysis?
7. What is the relationship between the keys of subtype account dimensions and the supertype account dimension?
8. How does the supertype/subtype design technique apply to businesses with varied products across multiple lines of business?
9. When is a family of supertype and subtype fact tables needed, and what customer demands do they address?
10. How is data managed between supertype and subtype tables when lines of business are physically separated?
11. What approach is taken when business processes capture metrics that do not vary by line of business?
12. How do subtype account dimension tables complement a supertype fact table in analyses?
13. In what scenarios would you use the supertype account dimension table versus the subtype account dimension table?
14. How do you ensure consistency and integration when using both supertype and subtype schemas for analysis?
15. What considerations must be made when designing and implementing supertype and subtype schemas in a DW/BI environment?

