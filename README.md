# Statistical Overview of New York City Airbnb
  Over the past 10 years, affordable short-term rental industry has bloomed, and Airbnb is emerging to become the leader of this industry. New York City is no stranger to Airbnb. In fact, New York is the platform’s largest market in the US with about 49,000 listings as of June 3rd, 2019. Airbnb also stirred up political and legal debates as the short-term rental activity has exacerbated the city’s housing crisis and eventually drives up the long-term rental price for New York residents. 

  In this notebook, I will perform an exploratory data analysis over the Airbnb dataset to gain understanding of the short-term rental scene in New York city.  

**Description of Data:**

  Airbnb does not publish any raw dataset; however, publicly available information was scraped from the company’s website and published on http://insideairbnb.com/get-the-data.html. The data used in this analysis was scraped on June 3rd, 2019. I will use the following datasets my analysis:  
1. **listings**: listings information includes various attributes. For the purpose of this EDA, I will use the following attributes: host_id, room_type, longitude, latitude, price, neighbourhood_group_cleansed, neighbourhood_cleansed, reviews_scores_rating, review_scores_location, review_scores_cleanliness, bathrooms, beds
2. **reviews**: reviews given by guests of searchable listings
3. **calendar**: dates and prices of future available dates  

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
   ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Room%20Type.png)
   
  Furthermore, I will examine the distribution of listing across New York. Brooklyn and Manhattan, two already densely populated areas, have the greatest number of listings. 
  ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Listings%20per%20Borough.png)
   ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Choropleth%20Map.png)

  **2.	Price and Demand**

In this section, I will dive deeper into price and booking activity analysis for Airbnb listings. First, let us have a quick glance at how much it costs to rent a room in each borough. I apply the three-sigma rule to remove outliers as there were some properties costs $0/night or $10,000/night.  Manhattan has the highest median price per night of $150, followed by Brooklyn with $90. Queens and Staten Island appears to have the same median for price per night of $70. Bronx has the lowest median price per night of approximately $60. 
  ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Distribution%20of%20Price.png)

   
Now, let us take a closer look at the price distribution across the New York City to see which are the most expensive areas. Generally, it is more costly to stay near Downtown Manhattan area. The most expensive neighborhoods are Tribeca, Financial District and south of Staten Island. The price range for these areas are $230 - $275. It is no surprise that Downtown Manhattan offers the most expensive properties due to its proximity to major attractions such as Times Square, the Empire State Building, Rockefeller, and many great bars and restaurants. South of Staten Island, on the other hand, offer larger and rather more luxurious rooms which can accommodate more guests as compared to smaller rooms in pre-war buildings in Manhattan or Brooklyn. 
  
   ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Choropleth%20Map%202.png)

  The next step is to explore the review trend over the year to see how fast Airbnb has been growing. Overall, the review trend reflects the increasing demand for Airbnb over the past 10 years. The annual growth rate is roughly 40%. Additionally, there is a ‘wave’ in the graph, indicated that there is a seasonal demand for short-term rental. 
     ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Demand%20Trend.png)

Similarly, let us learn more about the annual price trend. Due to limitation in the availability of data, I can only perform the price trend for 2019. It seems like the best time to travel to New York City is in January, when the price and demand are at their lowest points. There is a peak in August (when the holiday season started) and New Year Eve. 
     ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Price%20Trend.png)

**3.	Reviews – the voice of customers**

Customers’ reviews provide tremendous insight into what customers like and dislike. In this section, I utilize the power of wordcloud to see what keywords are featured frequently. I take 1,000 random reviews to perform this analysis. Most frequently mentioned keywords such as “Times Square”, “Central Park”, “Columbus Circle”, “great location”, “subway” and “walking distance” indicate that customers strongly emphasize on the importance of location and connectivity to the top attractions. “Great hosts” and “great place” – nice and comfy accommodation – also play an important role in shaping customers’ experience. 
 ![alt text](https://github.com/anhquynhtran/EDA-NYC-Airbnb/blob/master/Word%20Cloud.png)

  
