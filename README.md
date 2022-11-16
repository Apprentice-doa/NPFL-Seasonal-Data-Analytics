# NPFL-Seasonal-Data-Analytics

This project is intended to show the activities of the NPFL (Nigeria Professional Football League), Nigeria's top-flight football league.By conducting an EDA (Exploratory Data Analysis) into the League, this project exposes the performance of NPFL teams in the 2018/2019, 2019/2020, 2020/2021, 2021/2022 seasons.

Some of the KPI's to watch out for include:
+ Final League Position
+ Total number of Goals Scored
+ Average Goals Scored per Match

This project for the public most especially Sports analysts, Club owners, Club managers, League officials, Sports Journalists, Data Scientists, and Sports Enthusiasts with much recommendations for people aiming to get into the field of sports analytics, and also club managers that want to see how an interactive dashboard can give insights into the performance of their clubs.

# Documentation

## Data Source 

The data was sourced by performing web scraping operations across several news sites, sports betting sites, blog sites, and wikipedia. 
The data was compiled together and published on [kaggle](https://www.kaggle.com/), an open source platform for getting open source public datasets, for anyone intending to conduct further analysis on the dataset.
The links to the dataset are: [2018/2019 Season](https://www.kaggle.com/datasets/danielakhabue/npfl-2018-2019-season), [2019/2020 Season](https://www.kaggle.com/datasets/danielakhabue/npfl-nigeria-professional-football-league-19-20), [2020/2021 Season](https://www.kaggle.com/datasets/danielakhabue/npfl-2020-2021-season), [2021/2022 Season](https://www.kaggle.com/datasets/danielakhabue/npfl-2021-2022-season).

## Data Extraction
The dataset was compiled in CSV (.csv)  spreadsheet(.xlsx) formats and imported into PowerBI. 

## Data Transformation
Before the dataset was loaded into PowerBI, it was first transformed.
+ The columns that were not needed for the analysis were removed [Transaction Id, Customer_ Id, Year_Month, Time].
+ The columns were converted to the right datatypes especiall the date column which was converted to the date datatype.
+ The value of Transaction_result was changed as 0 = Transaction failed and 1 = Transaction Successful.
+ The value of Transaction Start was changed to Transaction start.
+ The City['Los Angles'] was changed to City['Los Angeles'] for effective representation of the city on a map chart.
+ A date table was created using PowerBI date query code. 
You can find the code here: [PowerBI Date query code](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/45be5e8cdba7cd96d9386aeb8132e80b1dcd63ea/PowerBI%20Date%20Query%20Code)
+ A new table was created by duplicating the main table and the Transaction result was filtered to have just Transaction Successful.
+ The transformed data was then apllied to the visualization panel.

## Data Modelling
New relationships were created between the tables, and date was used as the relationship between the three (3) tables.

## Data visualization
+ A measure table was created and total revenue, number of Successful transactions, number products sold, average daily transactions were all calculated using DAX.
+ Charts were used to check for:
+ Expected Revenue by Transaction result
+ Revenue by City
+ Revenue by Device Type
+ Revenue by Date
+ Revenue by Category
+ Revenue by Gender
+ Date and Customer Login type filters were created as well.

# Useful Insights
## Revenue Trends
Revenue trended down between Tuesday, December 17, 2013 and Monday, January 13, 2014 with a drop of $875,719.
![Downward trend](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward%20Trend.png)
+ Analytical Explanations:
    + Male customers contributed immensely to the downward trend with a significant -64.32 % Revenue change (from $653,712 to $329, 361) as compared to Female customers  whose revenue contribution fell to -46.49 % ($606, 216 to $324, 360).
    + ![Downward Gender](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward_Gender.png)
    + The analysis also shows that the downward trend in revenue significantly came from the members, a category that accounted for a major revenue block of $1,472,887 out of the total $1,529,440 in revenue. This analysis shows that revenue from members fell to $635,409 (-58.86 %) compared to guests which contributed an initial $56,443 in revenue, and then dropped to $18, 312 (-67.62 %).
    + ![Downward customer](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward_Customer.png)
    + Fashion, and Clothing also accounted for a major decrease in revenue by category of products, with Fashion taking a pro-gravity jump to -60.39 % with $376.767 loss and Clothing following suit with -51.85 % and $283, 628 loss in revenue.
    + ![Downward category](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward_Category.png) 
    + ![Downward category2](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward_Category%20(2).png)
    + The revenue gotten customers in Los Angeles which contributed a large chunk in revenue saw a downward trend 0f -59.42 % of total revenue change ($1,353,564 to $549,323) compared to New york with revenue change of $175,876 to $104,394.
    + ![Downward city](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Downward_City.png)
+ The longest and consistent upward trend occured between Saturday, October 12, 2013 and Saturday, October 26, 2013 with a rise of $405,462.
    + ![upward trend](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Upward%20Trend.png)
+ This upward trend saw a 65.82 % in revenue change from female customers with fashion products having a 37.29 % increase which amounts to $952,027 from $692,708, and wearables also having an amazing 106.81 % increase in revenue ($106,396 to $220,038).
    + ![upward category](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Upward_Category.png)
+ A careful look at this analysis shows that within this time fame of upward trends in revenue, the revenue gotten from the male customers fell from $644, 043 to $563,094 indicating a -12.57% revenue growth.
    + ![upward gender](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Upward_Gender.png)
+ Also, the revenue gotten from customers in Seattle, Washington, fell by -7% i.e $1,172,619 to %1,090,541 compared to Los Angeles and New York which had revenue growth of 221.28 % and 368.29 % respectively.
    + ![upward city](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Upward_City.png)
## Other Insights
+ The web-based platform was the most used medium of purchase by customers contributing 81.09% of total revenue.
    +![device_analysis](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Device%20Analysis.png)
+ Fashion, and Clothing products were the major source of revenue accumulating a total of $197,319,259 in revenue.
    +![category_analysis](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/Category%20Analysis.png)
+ Seattle was the most revenue-generating city raking in $140,456,574.
+ ![city_analysis](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/images/City_Analysis.png)

## Data Publishing
The data was published from the PowerBI environment and a link was generated for others to view and interact with the dashboard.
Link to my dashboard: [E-Commerce Dashboard](https://bit.ly/ecommerce_intelligence)

## Feedback

If you have any feedback, please reach out to me at: akdaniel0009@gmail.com

## Author

- [@Apprentice-doa](https://github.com/Apprentice-doa)

## 🚀 About Me
I'm a Data Scientist with experience in building end -to- end data analytics projects and machine learning models.

## Badges

Introduction to Data Science :  [cognitveclass.ai](https://courses.cognitiveclass.ai/certificates/365fbc9951984872b676b58bf6b750b0)

Data Science Tools : [cognitveclass.ai](https://courses.cognitiveclass.ai/certificates/b548573757be44ac8f00dd771ceba37c)

Top 50% AI and ML with Python Regression Hackathon : [datasciencenigeria.org](https://cert.datasciencenigeria.ai/) (ID for Authorization: DSNAI0009981)

# Hi, I'm Daniel! 👋

## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://bit.ly/daniel-akhabue)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/daniel-akhabue/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/doa_apprentice/)

## 🛠 Skills
Python (OOP), Data Analytics, Machine Learning, Features engineering.

## Related

Here are some related projects

[Awesome README](https://github.com/Apprentice-doa/PowerBI-E-Commerce-Data-Analytics/blob/main/README.md)

