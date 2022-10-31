## Optimal EV Charging Infrastructure
*Optimisation*
<br><br>
The notebook was built using [GitHub](https://github.com/harjotdadhwal/Optimal-EV-Charging-Network)

**Introduction** 
The mobility sector accounts for around 18% of the carbon dioxide emissions from 
burning fuel. A considerable market share of electric vehicles (EVs) running on clean 
power is key to mobility decarbonisation. As the number of EVs on our roads continues 
to increase, the demand for charging is following suit. Today around 10% of drivers are 
choosing EVs when buying a new car, and this is expected to grow rapidly.

**We need 
accelerated technology and infrastructure development to support EV market growth. 
While EV drivers are looking for a charging experience that is as fast and comfortable 
as possible, the main obstacle to mobility decarbonisation is inconvenience caused by 
charging infrastructure and charging time** Proper placement of charging points can 
alleviate this problem. It is a subject of current research and business interest 
simultaneously and has immense implications for the adoption of EVs, including: 
1. lowering range anxiety among EV owners,
2. optimal utilisation of EV charging points,
3. minimal travel time and waiting time for EV owners.
In addition, the challenges around this problem are evolving as EVs penetrate different 
geographies. For example, the EV charging placement in a U.S. city has different nuances than in a 
suburban town in India. 

**The demand for solving this problem at different geographies and scales will 
increase exponentially in the next decades as EVs spread from cities and urban 
areas to villages.

**Problem Statement:**
- To optimally place EV charging stations
so that the configuration remains robust to demographic changes.

<img src="images/evf.JPG?raw=true"/>

**Notations and Constraints**
<img src="images/notations.JPG?raw=true"/>


### 1. Modeling Approach 
The project output demands the following steps:
- Forecast the EV demand for each demand point  
- Estimate the distance to the nearest supply point 
- Create the demand-supply matrix 
- Given the constraints, formulate an LP problem to minimise the overall cost 


