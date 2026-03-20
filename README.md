# pharma-category-seasonal-sales
An automated, end-to-end pipeline that ingests daily point-of-sale data, rolls it up to identify broader weekly or monthly trends, predicts the upcoming season's demand volume

# Capstone Project: Pharmacy Inventory Optimization via Machine Learning

## Question 1: Problem Definition
**The Problem:** Retail pharmacies face significant inventory management challenges with highly seasonal medications (e.g., antihistamines and analgesics). Demand fluctuates wildly based on environmental factors and viral seasons. 
**The Context:** Relying on static, historical averages for purchasing leads to critical imbalances. Overstocking results in expired product and wasted capital, while understocking means turning away symptomatic patients.
**The Beneficiaries:** This project directly benefits Pharmacy Inventory Managers and Supply Chain Planners.
**The Outcome:** An automated pipeline that ingests transactional data, discovers correlated buying behaviors using unsupervised machine learning, and translates those mathematical clusters into actionable, AI-generated merchandising strategies.

## Question 2: Approach & Tool Selection
**The Approach:** First, raw daily transactional data was aggregated into weekly totals to expose broader trends. Next, a K-Means Clustering algorithm was deployed to discover "Hidden Seasons" based purely on correlated buying habits across 8 drug categories, ignoring date/time inputs. Finally, Generative AI was used to synthesize these mathematical clusters into a real-world business strategy.
**Tool Selection:** * **Data Processing:** Python, Pandas (for time-series resampling), and Matplotlib (for visualization).
* **Machine Learning:** Scikit-Learn's `StandardScaler` and `KMeans` algorithms were selected to group the data without temporal bias. 
* **Generative AI:** A Large Language Model was used for the "System Integration/Ideation" phase, contextualizing the raw cluster data for retail floor optimization.
**Alternatives Considered:** I initially considered using a Random Forest Regressor to forecast specific unit volumes. However, I pivoted to K-Means Clustering because discovering correlated buying behaviors across *all* categories simultaneously provided a more holistic, actionable insight for merchandising than a single-item forecast.

## Question 3: Reflection
**What worked better or worse than expected:** The K-Means algorithm worked exceptionally well. By removing the dates and scaling the data, the model successfully identified distinct "Spring Allergy" and "Winter Viral" seasons based entirely on the mathematical correlation of the items being purchased together. 
**Challenges and Limitations:** A core limitation of this clustering approach is that while it identifies *what* happens together, it doesn't predict *when* it will happen next. It provides a strategic grouping, but not a time-series forecast.
**Improvements for Next Time:** Next time, I would combine both approaches: using clustering to bundle the medications into "Seasons," and then training a multi-variate regression model (incorporating external weather/pollen data) to predict exactly which week that specific cluster will peak.

## Business Strategy, brainstormed using AI:
Recent machine learning analysis of our last six years of transactional data has identified distinct, highly correlated purchasing clusters that we must leverage to optimize our retail footprint. Specifically, the model isolated Cluster 0 (our "Winter Viral Season"), demonstrating a massive concurrent demand for acetaminophen and airway medications, and Cluster 3 (our "Spring Allergy Season"), which shows a synchronized spike in systemic antihistamines. Moving forward, we will use these mathematical pairings to drive our front-of-house merchandising. When predictive indicators signal the onset of these seasons, store managers are directed to build high-visibility endcap displays that physically bundle these specific items together. By cross-merchandising acetaminophen with asthma relief products during viral peaks, we capture secondary purchases and improve the customer experience by functioning as a one-stop wellness destination.

To successfully support this retail strategy, our warehouse procurement protocols will be dynamically aligned with these newly discovered clusters. Rather than utilizing static, historical order quantities for individual SKUs, supply chain planners will now execute bulk, clustered purchasing blocks four weeks ahead of the anticipated seasonal shifts. By front-running the demand for an entire cluster's product suite simultaneously, we can negotiate better vendor freight rates, drastically reduce out-of-stock events during critical public health windows, and maintain leaner, more agile backroom inventories year-round.

Dataset : Kaggle - https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data/data