## Optimal EV Charging Infrastructure
*Optimisation*
<br><br>
The notebook was built using [GitHub](https://github.com/harjotdadhwal/Optimal-EV-Charging-Network)

**Introduction** 
**The mobility sector accounts for around 18% of the carbon dioxide emissions from 
burning fuel.** A considerable market share of electric vehicles (EVs) running on clean 
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

Let’s try to understand forecasting of EV charging demand and EV infrastructure 
optimisation using the above fugure. Typically for such problems, a geographic region is divided into 
equal size blocks. Total EV charging demand of each block is represented at the centre 
of the block. Let’s call these centre points as demand points, which are represented as red 
circles in the above figure. All demand points of a geographic region collectively create a demand 
map over the region of interest. For each demand point, forecasting can be done using 
the historical demand maps.
EV charging stations are typically installed at public parking locations so that EVs can be
charged during the idle parking time. These parking locations are predefined based on 
how real estate has been developed in the region. These are called supply points and 
are represented as green stars in the above figure. Each parking location has a fixed number of 
parking slots i.e. potential places to install EV charging stations. 
<br><br>
Typically, two types of 
charging station are installed based on their supply capacity: i) slow charging station 
(SCS) and ii) fast charging station (FCS). Based on how many SCS and FCS are installed
at a parking location and their respective charging capacities, we can calculate the 
maximum supply that can be given by each supply point. All supply points of a geographic 
region collectively create a supply map over a region.
Using the demand map, supply map, demand-supply constraints and objective, we can 
optimally choose to place the EV charging stations so that the designed EV infrastructure 
is best suited to cater the forecasted demand. More details on this are provided in the 
subsequent sections.





### 1. Data Collection and Preprocessing 
We were pprovided with 1 year of structured customer feedback data (1.78 lac responses) with information such as:
	- customer details like mobile no, name, date of purchase 
	- store code
	- invoice amount 
	- product/brand/category description 
	- ratings, feedback 
	- store reckoner

<img src="images/cleaning.JPG?raw=true"/>
