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

### 2. Current NPS Status
The overall NPS score stood at 58.59%, which could be interpreted as ~60% of consumers were likely promote the brand to others. This was dismal. The ask was to extract key topics which influenced a poor or a great NPS rating. The challenge was to get the underlying and hidden nuances from the text data.   
<br><br>
<img src="images/current_nps.JPG?raw=true"/>

### 3. Modeling Approach 
The overall modeling framework adopted for this study can be summarized in the below infographic.
<br><br>
<img src="images/nps.JPG?raw=true"/>


### Part 1.1. - CSD extraction using Topic Modelling (Latent Dirichlet Allocation)
6 Customer Satisfaction Dimensions have been identified through LDA namely - 
<br><br>
**1.Generic - appearing as a dominant topic in 11% of the responses 
<img src="images/topic0.JPG?raw=true"/>
<br><br>
**2.Product - appearing as a dominant topic in 15% of the responses 
<img src="images/topic1.JPG?raw=true"/>
<br><br>
**3.Experience - appearing as a dominant topic in 7% of the responses 
<img src="images/topic2.JPG?raw=true"/>
<br><br>
**4.Availability - appearing as a dominant topic in 20% of the responses 
<img src="images/topic3.JPG?raw=true"/>
<br><br>
**5.Discount - appearing as a dominant topic in 7% of the responses 
<img src="images/topic4.JPG?raw=true"/>
<br><br>
**6.Service - appearing as a dominant topic in 40% of the responses 
<img src="images/topic5.JPG?raw=true"/>

