<img src="[images/readme_icon.png](readme_image.svg)" width="500" style="display: block; margin: 0;" />

# Exploring Airbnb Properties with Tableau

## :dart: Project/Goals

In this project [^1], I chose Option 2 to answer a series of questions about the relationship between Airbnb property location and prices through a comprehensive study and analysis of data from a provided dataset (source: Inside Airbnb). This table contains 30,478 Airbnb listings in New York City. This exercise is part of learning and mastering Tableau, a professional data analysis and visualization software.

Core submitted files include:

- [x] README file
- [x] transformed data file in MS Excel format
- [x] a presentation (in pdf)
- [x] Tableau workbook (with dashboard and story presentation)
- [x] related images and static visualizations

## :art: Process

- **Data Transformation and cleaning:**
    - preview data in Tableau, create basic visualizations to assess the quality of a dataset
    - pinpoint required changes, modify dataset either in Pandas or directly in Excel
      
   :pushpin: **JUMP TO:** [data](https://github.com/ankamercier/)
 
- **Load data back to Tableau:**
    - Use "Data Source" option to change a source file
    - Set a correct country location (defalut: Canada), and make sure zipcode is set to data type "geo"
- **Create sheets and dashboards:**
    - Use parameters (e.g. Price Range)
    - Create calculated fields (e.g. Price Quartiles)
    - use a consistent color scheme across all visualizations
    - ensure a smooth transition and interaction between visualizations on certain dashboards (cross-filtering)
    - add labels, legends and titles where necessary
    - include a brief explanation or key insights
- **Connect dashboards to create a Story**
  
  :pushpin: **JUMP TO:** [results](https://github.com/ankamercier/)

## Results

I chose Option 2, selected dataset: Airbnb Listing in NYC. 

### Created visualizations:

**1. Interactive Map**
**Choice justification**: map shows geographical distribution of listings based on zip code and neighbourhood (geo dimention) and average price (measure). It has two parameters: Room Type and Price Range. Tooltip allows to filter listings by neighbourhood and shows average price per night in given years (2008-2015).

**2. Stacked Bar Chart**
**Choice justification**: stacked bar chart shows room type distribution by neighbourhood. It allows to compare amount of listings in each neighbourhood, it's stacked by Room Type. 

**3. Line Chart**
**Choice justification**: in case of line chart, I checked listing growth over time, with horizontal axis showing years, and vertical axis showing sum of listings. Additionally, we can see a forecast for each room type using this visualization.

**4. Table**
**Choice justification**: I initially wanted to create custom icons that would be "filled" based on percentage of listings available in each property type (this is different from room type, please check data source for reference). Unfortunately, its not possible in Tableau - the tool recognizes the icon, but cannot modify it's contents, apart from color. Choice was made to approach it differently: I created custom icons for selected property types (6 out of 19), added a label that shows their amount, color-coded it by amount, and used is as interactive part of the dashboard. Chosen property types: Apartment, Boat, Castle, House, Lighthouse, and Treehouse.

**5. Bar chart**
**Choice justification**: from a business perspective (to show which neighbourhoods have higher prices), I created a simple bar chart that shows average prices across neighborhoods. Combined with popularity, this visualization can provide vital insights for new entrants on Airbnb market, and support a decision making process regarding the choice of neighbourhood and property type based on profitability and occupancy rate.

**6. Another line chart**
**Choice justification**: this optional visualization shows an average price per amount of beds.

**7. Highlight table**
**Choice justification**: this interesting table provides an overview of selected property types an their "popularity" (or "occupancy rate"). There is no data available on how many times a listing was actually booked, so number of reviews served as a reference here. In my understanding reviews are written by visitors that stayed in the property, so technically we can use it as a certain dimention of popularity.

### Based on above mentioned visualizations, I was able to answer following questions:

**1. How does the average price of Airbnb listings vary across different neighborhoods in New York City?**
<br>Answer: *interactive map shows a full variability in prices. Listings are in general more expensive in Manhattan, but i noted some outliers based on property type or room type.*

> [!IMPORTANT]
> The price of listings change as you move further from popular landmarks or city centers.

**2. Is there a correlation between the number of beds and the price of listings?**
<br>Answer: *to investigate this, we can analyze our bed/price chart. In general, price increases with amount of bes available. But there are some interesting points: the price rapidly increases for properties with 8 beds, and with 12 beds. This means that if an new entrant on the market plans to invest in a property, and he chooses among either 4-7 beds (not to mistake with bedrooms)or 8, it's better to go for 8 bds in NYC. This may also vary by property type (but this correlation wasn't explored).*

**3. What is the distribution of room types (Entire home/apt, Private room, etc.) across different neighborhoods?**
<br>Answer: *it's a no-brainer that majority of listings are located on Manhattan.  However, analysis shows that while "Entire homes/apts" and "Shared rooms" have indeed a majority of listings there [10,268 and 436, respectively], most of "Private rooms" are actually in Brooklyn [5,726 listings].*

**4. How has the number of Airbnb listings grown over time, based on the "Host Since" dates?**
<br>Answer: *While "Entire home/apt" and "Private room" were steadily growing over time, "Shared room" growth was almost unnoticable.*

**5. Which property types command the highest average number of reviews?**
<br>Answer: *Among chosen property types, most "popular" is (surprisingly) a boat (avg number of reviews: 18.25). Then comes House (14.91) and apartment (14.91), Fancy a boat?*

**6. How many property types there are in each neighborhood?**
<br>Answer: *interactive map in a dashboard allows to view which property types are listed there. For instance, Bronx has only houses and apartments, and Manhattan offers these + one castle, 2 boats, and 2 treehouses!*

**7. Are there any outliers in terms of price or review scores, and what characteristics do they share?**
<br>Answer: *One area in Manhattan (zipcode: 10119) has unusually high prices with average price per night at $1500. There were many outliers based on wrong zip codes - they were either modified based on a listing name (it was obvious that "sunny apartment 5 mins away from NYU" is in Manhattan and not in San Francisco), or excluded (if listing name was ambigous or there was no other way to identify it). There are no private or shared rooms that would fall within a range of $500-$1000 per night. Once a filter is applied to show "entire home/apt" listings within a range of up to $100/night, map shows quite a lot of results on the outskirts of metro NYC area (Bronx, Flushing in Queens, Staten Island and Long Island). This means that either these are some micro-apartments, or basements and treehouses.*

#### Dropped ideas:
Is there a correlation between a host's experience (time since becoming a host) and their listing's review scores? No correlation.

> **Price-wise, there are few exciting facts which I noted along the way:**
> - you could rent a lighthouse for as low as $39 per night
> - there are 4 treehouses listed on Airbnb in NYC
> - if you want to stay in a castle, be ready to pay $150/night
> - in New York, you can spend a night on a boat (choose among 8 in Manhattan, Brooklyn or Queens!)
> - other unexpectedly odd property types not listed in here were: tents, RVs, dorms, and huts.

## :medal_sports: Skills & Methods used
- Data collection and integration.
- Data cleaning and preprocessing.
- ETL techniques for data transformation (using Pandas)
- Exploratory Data Analysis (EDA).
- Data visualization.
- Tableau Public

## :construction: Challenges 
During creation of the first visualization (map), I immediately noticed that some zip codes are either not within range, or invalid (assigned to wrong neighborhood or too short). Biggest (fixable) challenge was to fill missing zip codes in Excel or chosen IDE. As a less complex solution, I chose to do it in Pandas and use neighbourhood as a reference using a following code (and quickly learned a new library along the way, `geopandas`):

```python
import pandas as pd
import numpy as np
from shapely.geometry import Point
from geopandas import GeoDataFrame

def clean_zip_codes(df):
    # define the boundaries for New York Metro Area to flag zipcodes that don't fall within our range
    ny_bbox = {
        'min_lat': 40.4774, 'max_lat': 40.9176,
        'min_lon': -74.2591, 'max_lon': -73.7004
    }
    
    # function to check if a point is within the boundary
    def is_in_ny(lat, lon):
        return (ny_bbox['min_lat'] <= lat <= ny_bbox['max_lat'] and
                ny_bbox['min_lon'] <= lon <= ny_bbox['max_lon'])
    
    # flag invalid zip codes
    df['valid_zip'] = df.apply(lambda row: is_in_ny(row['latitude'], row['longitude']) and 
                                           len(str(row['zipcode'])) == 5, axis=1)
    
    # dictionary to map neighborhoods (to assign a default zip code based on neighbourhood)
    neighborhood_to_zip = {
        'Manhattan': '10001',
        'Brooklyn': '11201',
        'Queens': '11101',
        'Bronx': '10451',
        'Staten Island': '10301'
    }
    
    # replacing invalid zip codes with default neighborhood zip codes
    df.loc[~df['valid_zip'], 'zipcode'] = df.loc[~df['valid_zip'], 'neighbourhood'].map(neighborhood_to_zip)
    
    # function to assign zip code based on listing title
    def assign_zip_from_title(row):
        title = row['name'].lower()
        if 'meatpacking' in title:
            return '10014'
        # I quickly realized that I would have to include too many conditions, and quick Excel filtering was easier at this point (only 120 wrong zip codes were not worth the fuss)
        return row['zipcode']
    
    # apply the function to rows where zipcode is still invalid
    df.loc[df['zipcode'].isnull(), 'zipcode'] = df.loc[df['zipcode'].isnull()].apply(assign_zip_from_title, axis=1)
    
    # drop the temporary 'valid_zip' column
    df = df.drop('valid_zip', axis=1)
    
    return df

# using the function
df = pd.read_csv('airbnb.csv')
cleaned_df = clean_zip_codes(df)
```
Thanks to Pandas, we could:
- automatically flag zip codes that are not within given longitude-latitude (New York Metro Area, state of New York) 
- replace values of invalid flagged zipcodes with ones that match with neighbourhood in their respected row, in "Neighbourhood" column (e.g. Manhattan would be given a zipcode 10001)

For remaining unassigned zip codes, I decided to manually check the listing titles and find correlation to assign correct zip code value (e.g. "Stay in Meatpacking District!" would get a 10014 zip code). Zip codes that are too short or invalid (null or not 5 figits long), or located too far we can either manually check in Excel, or simply delete them
There were only 120 wrong zipcodes or mismatched neighbourhoods (e.g. visible on a map as part of Manhattan, but Tooltip states "Queens").

After data cleaning, I had to switch the data source for my created sheets in Tableau.

Also, available data did not allow to check seasonal trends:
Are there any seasonal trends in pricing across different neighborhoods?

## :rocket: Future Goals
Build animations, more sophisticated navigation across the workbook, and use more recent data that would include bookings and dates!

[^1]: Disclaimer: this assignment is part of a final Tableau project at Lighthouse Labs
