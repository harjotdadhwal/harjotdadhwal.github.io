## NPS Driver Analysis using effect-based Kano Model 
*Topic Modeling*

**Project Abstract:** 
The advent of e-commerce has resulted in a smaller, but more competitive battleground for retailers. 
Therefore, determining how effective your business is at making customers happy is essential.
This is why, the Net Promoter Score (NPS) is so valuable. NPS is used to measure customer loyalty
and how likely they are to refer your products and services to others. An NPS customer feedback survey aims to answer two questions: 
<br><br>
i.	How likely are your customers to recommend your product or service?
<br><br>
ii.	What are the key factors influencing your customers’ likelihood to recommend your product or service?
<br><br>
<img src="images/nps.png?raw=true"/>
<br><br>

Computing the Net Promoter Score indicates how likely your customers are to recommend your product or service,
but doesn’t explain the ‘why’ behind their response. The underlying goal of driver analysis is to determine the
key attributes of your product or service that determine your NPS. These attributes are referred to as ‘drivers’. 
<br><br>
To identify key drivers to a differentiated product or service, it is imperative to extract customer satisfaction
dimensions (CSDs) from the factors influencing their likelihood to recommend. In this project, CSDs are firs
t extracted from comments based on latent dirichlet allocation (LDA). The sentiment orientations of the extracted 
CSDs are identified using a support vector machine (SVM). Then, considering the existence of complex relationships among different CSDs 
and the customer satisfaction, an ensemble neural network based model (ENNM) is proposed. On this basis, category of each CSD can be identified using an 
effect-based Kano model (EKM), which can be further used to influence how to tailor products and improve services.

**Business Objective:**
- To identify actionable drivers of NPS for different geographies


**Analytics Objective:**
- To extract customer satisfaction dimensions (CSDs) from customer feedback data and establish its relationship 
with customer satisfaction to identify key ‘drivers’ of NPS



### 1. Data Collection and Preprocessing 
We were pprovided with 1 year of structured customer feedback data (1.78 lac responses) with information such as:
	- customer details like mobile no, name, date of purchase 
	- store code
	- invoice amount 
	- product/brand/category description 
	- ratings, feedback 
	- store reckoner

<img src="images/cleaning.JPG?raw=true"/>


### 2. Modeling Approach 
The overall modeling framework adopted for this study can be summarized in the below infographic.
<br><br>
<img src="images/dummy_thumbnail.png?raw=true"/>

### 3. Data Preparation 
• **Missing values** - for weather parameters were imputed using MICE. Also, certain parameters like visibility, humidity, wind chill, and station pressure that had over 75% data missing - were removed.<br><br>
• **Upscaling of weather data** -  it was required to upscale the data from lower to the broader level i.e., from station level to the province level. k-means clustering was used to perform data upscaling to establish data scale uniformity 
