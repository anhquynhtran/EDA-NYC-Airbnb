# Statistical Overview of New York City Airbnb
  Over the past 10 years, affordable short-term rental industry has bloomed, and Airbnb is emerging to become the leader of this industry. New York City is no stranger to Airbnb. In fact, New York is the platform’s largest market in the US with about 49,000 listings as of June 3rd, 2019. Airbnb also stirred up political and legal debates as the short-term rental activity has exacerbated the city’s housing crisis and eventually drives up the long-term rental price for New York residents. 

  In this notebook, I will perform an exploratory data analysis over the Airbnb dataset to gain understanding of the short-term rental scene in New York city.  

**Description of Data:**

  Airbnb does not publish any raw dataset; however, publicly available information was scraped from the company’s website and published on http://insideairbnb.com/get-the-data.html. The data used in this analysis was scraped on June 3rd, 2019. I will use the following datasets my analysis:  
1. listings: listings information includes various attributes. For the purpose of this EDA, I will use the following attributes: host_id, room_type, longitude, latitude, price, neighbourhood_group_cleansed, neighbourhood_cleansed, reviews_scores_rating, review_scores_location, review_scores_cleanliness, bathrooms, beds
2. reviews: reviews given by guests of searchable listings
3. calendar: dates and prices of future available dates  

There are no available data for booking activity, so I will use review activity as an indicator of Airbnb activity instead. 

**Exploratory Data Analysis:**
**1.	Hosts and listings**

  Airbnb’s business model connects hosts who rent out their private property to short-term subletters. Assuming that most listings are non-licensed, we expect that the majority of the listing are private or shared room which allows host to continue living in her own home. The graph below is in line with our expectations:
 
 ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Listings%20per%20Host.png)

  There are approximately 27,000 single listings and 4,000 multiple listings. Let us explore the host with multiple listings further: 
   ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Top%20Hosts.png)
   The top host listed up to 170 listings on Airbnb. These top hosts are hotel managers who rent out their condo hotel. 
	 Now let us examine the type of accommodations in New York City. Airbnb's users do not like sharing room with others as we can see that it is only 2% of the listings. Private room – a legal type of rental in New York, captures 46% of the listings. Entire room captures 52% of the listings. This number is surprisingly high as New York state law regarding short-term
housing stated that it is almost always illegal to rent a full apartment when the host is not present 
for less than 30 days. 
