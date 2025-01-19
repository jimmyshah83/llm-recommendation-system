#### Cohere Embeddings
Dimensions: 1024
Embeddings: 250 000 000 (250 million)
Each dimension as float32 with 4 bytes per dimension 
~= 1TB of memory

Float = 4 bytes per dimension

This is a huge amount of data to store in memory.
Reducing the dimensions could be a solution to reduce the memory usage however, it is not a good idea to reduce the dimensions as it will reduce the quality of the embeddings. Other approach is to use an embedding model, that has been trained on using fewer bytes of memory per embedding.

- int8: 1 byte per dimension
By reducing the size we can save 4x more memory, reduce cost and still have 99.99% accuracy and 30% speed up in search

- binary: 1 bit per dimension
Reduces the memory usage by 32x, however, the accuracy is reduced to 90%


#### HNSW (Hierarchical navigable small world)
- Performs approximate nearest neighbor search 
- Slightly different from KNN brute force which compares every dimension with other dimensions, in the entire vector space, for semantic search, HNSW maintains great accuracy and is faster than brute force
- It uses a graph to search for a subset of nodes that are close to the query node
- Uses cosine (angle between 2 vectors), euclidean (distance between 2 vectors) or dot (length of each pair and the angle between them (vectors)) product similarity


#### AI Search features
- Vector Search using HNSW
- Semantic ranker (Uses the context or semantic meaning of a query to compute a new relevance score over preranked results.) Promote semantically relavant results by ranking and scoring the responses from vector search OR hybrid search
- Search types
1. Semantic search: Search for similar items
2. Hybrid search: Execute semantic and Vector search in parallel
3. Vector search


#### Small vs Large embeddings
- Dimensions: For tasks requiring high-quality embeddings across multiple languages and tasks, text-embedding-3-large might be preferable despite its higher cost. In contrast, for applications with tighter budget constraints or where ultra-high precision might not be as critical, text-embedding-ada-002 or text-embedding-3-small could be more suitable options.
- Context window: Smaller context windows are for more focussed embeddings and faster computation, however, potential loss of information for applications that require deeper understanding and meaning


#### Data 
1. Customer purchase history
2. Detailed Product information with reviews

2. Nice to have
- Customer Browising History and reviews data  to answer questions like `Given my past reviews and ratings, what are some products that might interest me and that I haven't considered before?`

#### Measuring ROI
------ can the productivity gains from its use cases and applications outpace the rising technical costs of production at scale? 
- Productivity Gains
- *Calculating Cost requires a clear understanding of target goals, widespread workforce adoption, continuous model refinement, infrastructure expansion, and significant computing power.

- Approach to calculating ROI   
1. Define Clear Objectives: Improving customer retention and sales by enhancing the relevance of product search
2. KPIs: Customer Retention Rate, Conversion Rate, Customer Satisfaction Score (CSAT)
3. Calculate Costs: Development Costs, Operational Costs, Data Security Costs
4. Estimate Benefits: Increased Revenue, Cost Savings (Reduction in Customer support costs)

- ROI Calculation Formula Example
1. **Total Costs for Year 1**: $100,000 (Development) + $20,000 (Operational) + $10,000 (Security) = $130,000  
2. **Total Benefits for Year 1**: $250,000 (Revenue Increase)  
3. **Net Profit**: $250,000 - $130,000 = $120,000  
ROI = 120,000/130,000 * 100 =~ 92.3%  