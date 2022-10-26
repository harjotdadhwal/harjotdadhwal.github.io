## Electricity Load and Price Forecasting for Short Term Period ***(Time Series Forecasting)***

**Project abstract:** 
Electricity trading has grown with superlative rapidity. It is a special form of commodity 
as it cannot be stored, and electricity price is too volatile. The cost of over-contracting 
or under-contracting and then buying or selling electricity is so high that it can even lead to 
bankruptcy. ***This project aims to make a high-frequency short-range price forecast to take electricity trading 
decisions at asset as well as macro-level for the deregulated Alberta Canada market.***

> Using an accurate price forecast, energy supply companies would be able to optimize their 
procurement strategies. Companies can also schedule their operations according to the low-price 
zones. In a nutshell, it will enable users to make informed energy trading decisions.

**Analytics Problem Statement:**
• To predict hourly electricity load for Alberta Canada 
• To forecast hourly electricity price based on above predicted load

### 1. Feature space 
Forecasting energy prices is a function of load prediction. Various parameters like historical load, 
climate data, and calendar information were considered for forecasting load at an hourly interval of 
time and in succession load, and other variables were considered to forecast price for the day-ahead 
market in Alberta Canada. 

### 2. Modeling approach 
The overall modeling framework adopted for this study can be summarized in the below infographic.
<br><br>
<img src="images/dummy_thumbnail.png?raw=true"/>

### 3. Data preparation 
• **Missing values** - for weather parameters were imputed using MICE. Also, certain parameters like visibility, humidity, wind chill, and station pressure that had over 75% data missing - were removed.<br><br>
• **Upscaling of weather data** -  it was required to upscale the data from lower to the broader level i.e., from station level to the province level. k-means clustering was used to perform data upscaling to establish data scale uniformity 

### 4. Mechanics of Electricity Pricing
• **High volatility in pool prices -** Electricity prices in Alberta have been increasing over the years. 2021 has witnessed an 
unprecedented surge in electricity prices because of a *seemingly unending polar vortex, the 
continuing shift from coal- to natural gas-fired power, as well as record-breaking electricity demand 
(PPA).* Additionally, the tight supply cushion within the Albertan electricity market has caused extreme 
volatility on the wholesale market, with the flat pool price averaging at $96/MWh with variability of 
$142/MWh (i.e., 1.5 times the average pool price)
<br><br>
<img src="images/price_volatility.JPG?raw=true"/>
• **Relationship of price with its lagged values -**  It was observed a strong positive autocorrelation (0.8) of price (t) with its lag (t-1). The chosen lags 
i.e., t-1, t-24, t-48, t-72, t-96, t-120, t-144, and t-168 are also coherent with the literature on price 
forecasting. 
<br><br>
<img src="images/lagged_values.JPG?raw=true"/>
• **Price Spikes -**  Another characteristic of the Power Pool is price spikes. Shocks in demand and supply, the prevalence 
of Polar Vortex resulting in sudden extreme temperatures, and unplanned outages along transmission 
lines result in highly volatile prices in certain periods.
For example, temperature between -20 and -30˚C on February 9th, 2021, led to a 61% increase in 
prices compared to last year, averaging $254.25/MWh.
<br><br>
<img src="images/price_spikes.JPG?raw=true"/>

### 4. Feature engineering

<img src="images/fe.JPG?raw=true"/>

### 5. Hypothesis Testing
<img src="images/ht.JPG?raw=true"/>

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
