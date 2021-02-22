# scooter_trip_analysis

## Summary 
Micormobility companies - Company A and Company B are two scooter companies operating in the Metro area of Louisville, KY. Based on their partial operation historical data, the goal is to analyzed the dynamic of the market of Louisville. I analyzed metrics such as ridership, trip duration, trip distance, and concentration of trips.

The objective and scope of this analysis is an initial exploration to understand the operations of both companies's scooter businesss as well as the market. Due to the limitiation of data provided, it prevents us from diving deeper and tease out more insightful patterns (more details will be stated in the Constrants section)

This initial analysis opens many angles for us to explore. I've brainstormed and provided a few intersting thoughts of next steps. We will set up meetings to sort out priority.


## Objective
  * Learn the dynamic of the market of Lousiville, KY, in which the two companies operate
  * Estimate the number of scooters company b operates in Louisville, KY.


## Main Analysis Steps

Here are the key steps I performed for this analysis:

 * Exploratory Analysis

 * Data Preparation and Cleaning

 * Feature Engineering

 * Define Metrics

 * Analysis and Visualization

 * Estimation of num of scooters with Company B


## Key Takeaways

Ridership, Trip duration, and distance may have different patterns across seasons, day fo week, and hours of day. 
 * Company A scooters

  * Ridership fluctuation followed the seasons of Lousiville, KY closely. (note that we don't have a complete year of data, it is hard to make a comprehensive intrepretation). From the starting of Aug (summer), the average monthly ridership of Company A increased rapidly from about 3,000 to 50,000 in a month, and hit peak in Oct, Nov 2018. In Fall, with the return of students to Louisville, Ridership reached about 6,000 in October, increased by about 50% compared to that of summer. Since Dec the return of cold weather dramatically brought ridership down to less than 4,000 in December.
  * Trip Duration: Average trip duration has been decreasing since 2018-08, and it reaches the lowest in 2018-12. 
  * Distance in miles: The average distance starts decreasing since weather starts getting colder, and it hits the lowest around 2018-12 for Company A.


 * Company B scooters
  * Ridership: We don't have enough Company B data to tell the ridership patten with seasons, but we noticed that Dec is the valley and ridership increased significantly in Jan 2019.
  * Trip Duration: Average trip duration started decreasing in 2018-12, and it reaches the lowest in 2019-01.
  * Distance in miles: The average distance starts decreasing since weather starts getting colder, and it hits the lowest around 2019-01 for Company B

 * Comparison between Company A and Compnay B
  * Ridership: 
    * For Company A, Friday and Saturday peaked with average around 170 - 180 rides per day, while for company B, the peak is around Tuesday and Thursday. It might be the case that Comany A and Company B focus on different operation locations
    * Company B has a clear peak around noon while Company A stays high-volumn the entire afternoon and starts dropping around 5pm. Note that it might be lack of data, but we notice that there's no rides at all from 10pm to 3am for Company A. I suspect that holds similar possibility of different focus of operation location
  * Trip Duration: 
    * To compare these two Companies, we can only look at 2018-12, the month that we have data for both companies. Company B outperformed Company A on average trip duration (Company A: 11.85; Company B: 16.27) 
    * Company A and Company B are quite similar in terms of trip duration pattern over days of week. Looks like Weekends riders tend to take longer rides than workdays. Possibly, people were hanging out around without checking out their scooters.
    * Similarlly, Both Company A and Company B have peaks around evening commute hours, and specifically Company A also have peak around early morning commute hours. Clearly, scooters don't get affected by normal traffic as much as other vehicle types, but there's somehow still some minor effect.
  * Distance in miles:
    * Scooters ran by Company A tend to have longer distance than Company B's. Besides the possiblity that Company A has data for the good weather months, It could be the case that the battery duration of Company A's scooters is longer.
    * Looks like the morning commuters using Company A's scooters typically have longer commute distance, as well as their evening commuters, but not as much. While riders riding Company B's scooters tend to ride for consistent shorter range.


## Constraints
* Sample size: For both companies, the sample size is small. We should gather at least one year of data, ideally more than two years for pattern consistency and seasonality
* Small overlap date range: From a time series perspective, one month of date range overlap would make it hard to make an apple-to-apple comparison on the operations between the two companies. Without the time/date covariates somehow controlled, the interpretation of the differnce on their operation performance could vary
* Not enough data for further exploration and analysis.


## Recommendation and Next steps

On a high level, my recomendation is we should 
1. Connect the current findings with our autonomous driving product
2. Define our business objective and ORK for further actions
3. Collect more data, and keep exploring
4. Further analysis to meet OKRs


I've brainstormed a few next steps for us to consider. Depending on our OKRs, we shall decide which of the next steps should be prioritized.


* Brainstorm within the team and PMs to connect current finding with our autonomous driving products

* Data Collection for further analysis to better understand Company A and Company B:
  * At least 2 years of historical data - date range overlapping between A and B(capture seasonality)
  * Weather data
    * Temperature
    * Precipitation
    * Snow depth
  * Elevation change
  * Rider ID
  * Neigborhood identifier (although this could be approximated by coordinates)
  * Profitability: Cost of each ride
  * Product Behavior:
    * Battery usage
    * Charging status
  * Customer behavior
    * Stationary vs. non-stationary
    * Placeback/replacement 

* More competitor analysis
  * Major players: Bird, Lime, etc.
  * Small players: Higher expenditure incurred on marketing and promotions of these services in comparison to the revenues generated by the major market players is reducing the sustainability of smaller players; this factor is expected to act as a restraint to the growth of the market
  * Analyze where to position our product in the market and what is our competitive advantage (not just against Company A or Company B)
  * Address how we can leverage our advantage to take lead in the market over Company A and Company B
