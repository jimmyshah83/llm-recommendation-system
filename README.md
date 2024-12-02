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


#### Sample prompt

prompt = ChatPromptTemplate.from_template(
    """You are a ecommerce system that help users to find products that match their preferences. 
Use the following pieces of context to answer the question at the end. 
If you don't know the answer, just say that you don't know, don't try to make up an answer.

Context: {context}

Question: {question}"""


#### Sample question
What is the price for TrailMaster X4 Tent?
What are some of the purchases made by Jane Doe?
What are the features of the TrailMaster X4 Tent?
What are some products bought by people in Suburbia?