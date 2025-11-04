# Readme
This repository is about the TP2 of the data graphs class. 
- To find the screenshot deliverables, please refer to the uploaded files section. 
- For the short note deliverable, please refer to the text below. 

## Short note
### Recommendation strategy
I would start with a simple “people who viewed this also viewed that” approach. The idea is to look at products that multiple users interact with, and if two products are often viewed or bought by the same customers, we recommend one when the user looks at the other. In Neo4j, this can be done by finding 2-hop paths between users and products and ranking results by frequency or a similarity score like Jaccard. To go further, we could use Personalized PageRank to give more weight to products connected to items the user recently viewed, and fall back to the most popular items when we have no user history.
### Production-ready improvements
Instead of running the ETL once, we can update the graph continuously based on new events, with proper error handling, validation, and monitoring. The API should include authentication and rate limiting. Tests and CI/CD would help avoid breaking changes, and hosting on a cloud environment with containers and auto-scaling would improve availability. Finally, we can add logging and A/B testing to evaluate recommendation quality, as well as privacy measures and backups to ensure compliance and reliability.
