# Hotel-Bookings
# Data Description
Type of Hotel - Type of Hotel (Villa or Motel)
 Year - Year of arrival date
 Month - Month of arrival date
 Reservation Date-Date on which booking is done
 Arrival Week - Week number of year for arrival date
 Arrival date - Day of arrival date
 Weekend stays - Number of weekend nights (Saturday or Sunday) the guest staved or booked to stay at the hotel
 Weekday stays - Number of week-nights (Monday to Friday) the guest stayed or booked to stay at the hotel
 Meal - Meals opted( All meals, only room etc)
 Booking Payment-No Deposit / Refundable/ Non-Refundable
 Adults - Number of adults
 Children - Count of accompanying kids above 5 years
 Kids - Count of accompanying kids below 5 years
 Country - Country of Guest
 Booking Type- Booking Source (Online, offline, corporate etc)
 Repeated Guest -Indicator Variable (0:No, 1:yes)
 Prev Cancel- Count of past cancellations
 History-Previous booking history
 Reserved Room-Type of Room selected during reservation
 Assigned Room - Type of Room allocated at arrival
 Booking changes-Count of how many times user changes their preferences
 Waiting list- Days in which booking is confirmed
 Customer-Type of customer
 Per Day Charges - Average Daily Rate
 Parking at premises - How Many cars needed to be parked
 Physical Challenged-Count of physical challenged people accompanying
 Reservation Status-Whether customer turns up or not (Target Variable)
 Cancellation - Value indicating if the booking was canceled (1) or not (0)
 Booking Done- Number of days between the booking and when they are scheduled to arrive at the property

# Analysis
We begin with treating  missing values by suitable values.
We perform some EDA for having some prior knowledge about the data.
By using countplot of year with respect to hotel type we found that in 2016 bookings are more in Motels.
Per day charges are same for Villas and Motels.
By using pie chart we can see that those who have not paid deposit have high Cancellation. But paid deposit and refundable still they are not cancelling but who paid deposit and they know their amount is non refundable still they cancell their bookings.
We also see descriptive statistics for numerical values.
we then use some chi square hypothesis test to test whether  the cancellation rates across all years is equal or unequal.
We see that the pvalue for our test is extremely small compared to our significance level. Hence we have to reject our null hypothesis. In conclusion, the rate of cancellation is different across all years.
Also we test whether the cancellation rate across both types of hotels is equal or unequal.
We see that the pvalue for our test is extremely small compared to our significance level. Hence, we have to reject our null hypothesis. In conclusion, the rate of cancellation across both types hotels is different.
we then clean the data and use label encoding for some features.
Target variable is seperated from the data for further analysis.
Now we split the data in train test split form and do RandomForestClassifier algorithm.
We then perform confusion matrix and find the accuracy with 99%.
