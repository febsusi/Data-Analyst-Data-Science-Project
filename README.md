# Febriyeni Susi Data Analyst-Data Science Portfolio

Hi, I'm Febriyeni! I have a technical background and hold a Bachelor of Science degree in Applied Statistics (Politeknik Statistika STIS). This is a repository to showcase skills, share projects and track my progress in Data Analytics / Data Science related topics.

# Table of Contents
- Portfolio Projects
  - Koin Project (Python and Tableau)
  - Clustering and Credit Scoring Fintech
  - Commuter Indonesia
  - Customers Satisfaction Research
- SQL
- Certificates
- Contacts

# Portfolio Projects
In this section I will list some data analytics and data science projects briefly describing the technology stack used to solve cases.

- Koin Project (Python and Tableau)

Code: Febriyeni-Koin Projects-CIA.ipynb;

Description: The dataset contains 2511 records as of May 2021. There is a list of lenders with user_name,	loan_duration,	loan_grade,	lender_interest, total_purchase, order_status,	order_type,	order_date,	product, and	sub_product. The project includes the following steps: data loading, data cleaning and preprocessing, EDA (exploratory data analysis), Encoding variable, Scaling variable, Split Data Train and Test, Predictive modelling using the K-Nearest Neighbor (KNN) algorithm.

Skills: data cleaning, data analysis, descriptive statistics, data visualization, supervised learning model. Technology: Tableau, Python, Pandas, Numpy, Seaborn, Matplotlib.
Results: Predictive modeling with the k-nearest neighbors' algorithm as supervised learning. In this project, I need to identify which users have the potential to be Mass/White/Silver/Gold lenders so that the company can upsell these lenders based on their predicted class.

- Clustering and Credit Scoring Fintech

Code: Febriyeni Susi-Credit Scoring Fintech.ipynb

Description: Customer segmentation using the KMeans algorithm as part of clustering analysis and finding the feature importance by comparing different algorithms. The dataset contains 1000 records data. There is a list of lenders with Age, Sex,	Job,	Housing,	Saving accounts,	Checking account,	Credit amount,	Duration,	Purpose, and	Risk. The project includes the following steps: data loading, data cleaning and preprocessing, filling missing values, EDA (exploratory data analysis), encoding variable, clustering analysis, and predicting model.

Skills: data cleaning, detecting data anomalies, python coding, data visualization, descriptive statistics, encoding variable, clustering analysis, and predicting model.
Technology: Python, Pandas, Numpy, Seaborn, Matplotlib, Supervised Learning Model, Unsupervised Learning Model.
Results: According to the evaluation metrics, the Naive-Bayes classifier works best because it gives the highest recall. However, when plotting the ROC curve and calculating AUC for all models, it is seen that XGB gives the highest AUC. So, the three features that have the most significant percentage using XGBoost are Duration, Saving Accounts, and Housing

- Commuter Indonesia

Code: CLUSTERING COMMUTER INDONESIA - FEBRIYENI.ipynb

Description: Clustering indicators of the quality of life of commuters in Indonesia using the DBSCAN algorithm as unsupervised learning model. The dataset contains 384 records data.

Skills and Technology: Python, Pandas, Numpy, Matplotlib, Data Visualization, Principal Component Analysis (PCA), DBSCAN algorithm.
Results: Based on the results of the calculation of the DBSCAN algorithm method, the number of clusters is 3 clusters. With each cluster member 0, 1, and -1 there are 281, 98, and 5 members. Cluster 0 is each observation that has the highest cluster, followed by Cluster 1, while Cluster -1 is each observation that has the lowest cluster. Based on the silhouette score of 0.333, it can be concluded that the objects in the cluster have a relatively weak level of similarity with each other, but each observation is in the right cluster.

- Customers Satisfaction Research

Tableau Public: dashboard, Minitab, Eviews, and SPSS

Description: The purpose of this research report is to measure the satisfaction level of customers and understand the customer’s needs for evaluation and improve the service of KoinRobo products. This report also analyzes the reasons and factors that influence customers’ satisfaction and allow insight into customers. This research was conducted with statistical and descriptive methods.

# SQL

- A customer complained for her failed order to our customer service, and the customer service ask data team to provide the order information (price, order_id, product name, when the product is bought). The customer only informs the CS her email id. Please write the syntax to get the information about the failed order.

 
SELECT

	a.name, a.price, b.order_id

FROM

	products a LEFT JOIN order_items b 
    
	    ON a.id = b.product_id
    
	LEFT JOIN orders d
    
	    ON d.id = b.order_id
	
    LEFT JOIN users c
	
        ON c.id = d.user_id

WHERE
	
    c.email =’email_id_cust’ AND d.status = ‘Failed’

- To get the top 5 of merchants in this month (May) based on the highest successful orders (successful can be seen by order status)


SELECT TOP 5

	a.merchant_name

FROM

	merchants a LEFT JOIN orders b 
    
        ON a.admin_id = b.user_id
	
    LEFT JOIN  order_items c
	
        ON b.id = c.order_id

WHERE
	
    b.created_at= ‘May’ and b.status=’Success’

GROUP BY 
	
    a.merchant_name

ORDER BY 

    SUM(c.quantity) DESC

- List of customers with average money spent per order is above Rp 1 million
 

SELECT 

    a.full_name, a.id, AVG(b.quantity*c.price) as Average_Amount

FROM

	Users a INNER JOIN orders d

    ON a.id = d.user_id JOIN order_items b
	
    ON d.id = b.order_id JOIN products c
	
    ON b.product_id = c.id

GROUP BY

    a.full_name, a.id 

HAVING
	
    AVG(b.quantity*c.price) > 1000000 

- Customers’ most purchased products


SELECT TOP 1
    
    a.name, SUM(b.quantity) as Total_Quantity
    
FROM
    
    products a 

JOIN order_items b 

    ON a. id = b.product_id
    
GROUP BY 
    
    a.name

ORDER BY 
    
    SUM(b.quantity) DESC





# Certificates
I believe that the best way to showcase skills is by doing and sharing your job done but sometimes certificates appear to be as an indirect result:) So here is a list of the ones I have (in reverse-chronological order, with the date of completion in brackets):

- Diploma in Using Python for Data Science	(2021) (Alison)
- HCIE-Big Data-Data Mining Course	(2021) (Huawei)
- Business Intelligence and Knowledge Management System 	(2021) (Alison)
- Python for Everyone	(2021) (Esri)	
- Machine Learning in Python Environment	(2021) (Alison)
- Introduction to Data Engineering	(2021) (Dell Technologies)
- Getting Started with Spatial Analysis	(2021) (Esri)	
- Understanding the Concepts of AI and ML	(2021) (Dell Technologies)
- Introducing Data Science and Big Data Analytics for Business Transformation	(2021) (Dell Technologies)
- INTRODUCTORY CERTIFICATE IN BUSINESS ANALYSIS	(2021) (Charles Sturt University)
- Introduction to Data Governance for Monitoring The SDGS	(2021) (United Nations Institute for Training and Research (UNITAR))
- Intro to Data Analytics Course	(2021) (RevoU)

# Contacts
- LinkedIn: https://www.linkedin.com/in/febriyenisusi/
- E-mail: febsusi87@gmail.com
