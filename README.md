# Coffee Production and Trade data
An interactive dashboard created in Excel that shows trends and information about countries that produce, export, and import coffee.\
[Link to dashboard](https://onedrive.live.com/edit.aspx?resid=784924BC0EF8BD53!3652&cid=784924bc0ef8bd53&CT=1700339340611&OR=ItemsView)\
\
Data Source - [Kaggle link](https://www.kaggle.com/datasets/michals22/coffee-dataset/data) \
OG Source - [International Coffee Organization](https://icocoffee.org/)

I begin every day with a cup of hot steaming coffee. I mean, there's no other way to start the day! 
So when I came across this dataset, I decided to dive into it and explore some interesting trends in the data.

---

### Design of the dashboard
I wanted to design the dashboard in a way that presents some obvious facts and allows one to explore some trends in the data based on individual interests. 
Hence, I start with the **Top 5** countries for each of the trade activities. Then I move to the **interactive** elements of the dashboard that allow for *Exploratory Data Analysis*.

#### Specific components of the dashboard
Here, I explain the data preparation process and the specific formula to create a chart or component.

##### 1. Charts showing the top 5 countries producing, exporting, and importing coffee.
![image](https://github.com/rutagokhale/coffee-data-dashboard/assets/33475585/15708ab4-e183-4fc1-91c8-c675997b04e6)

I created 3 `Pivot Tables`
| Country | Total Production |
| --- | --- |

| Country | Total Export |
| --- | --- |

| Country | Total Import |
| --- | --- |

and filtered the results in `descending` order of the `total` and chose the `top 5` results for each table. I used the filtered data to create a `horizontal bar chart`.

##### 2. A dynamic chart that shows the top 5 countries for the selected coffee type.
![image](https://github.com/rutagokhale/coffee-data-dashboard/assets/33475585/b18609dc-c183-4aae-a8f4-100404cb9afa)

First, I created a `Pivot Table`
| Coffee Type | Country | Total Production |
| --- | --- | --- |

and filtered the results in `descending` order of the `total` and chose the `top 5` countries for each coffee type.\
Next, I added a `Data Validation` selector for choosing a `coffee type`. Based on the selection, I used a `FILTER` formula to display the top 5 countries for the selected coffee type from the table. I used this data to create a `bar chart`.

##### 3. A dynamic chart that shows the trend of coffee imports for the selected country between the years 2019 to 2020.
![image](https://github.com/rutagokhale/coffee-data-dashboard/assets/33475585/35b35c0f-ac4e-4c9d-8557-36006a8950fe)

First, I created a `Pivot Table`
| Country | 1990 --- 2019 |
| --- | --- |

Next, I added a `Data Validation` selector for choosing a `Country`. Based on the selection, I used a `FILTER` formula to display the coffee import quantity for each year from 1990 to 2019. I used this data to create a `line chart` that shows the import trend for the selected country.

##### 4. A dynamic chart that shows coffee production vs domestic consumption of the selected country.
![image](https://github.com/rutagokhale/coffee-data-dashboard/assets/33475585/a23ecb72-8834-486c-9c9b-19a6ba2a3174)

I created a table
| Country | Total Production | Total Domestic Consumption |
| --- | --- | --- |

using `INDEX` and `MATCH` formulae. I added a `Data Validation` selector for choosing a `Country`. Based on this selection, I used a `FILTER` formula to display the production and domestic consumption for the selected country. I used this data to create a `pie chart` to show coffee production vs. domestic consumption quantities.

##### 5. A dynamic chart that shows the trend of coffee exports for the selected country between the years 2019 to 2020.
![image](https://github.com/rutagokhale/coffee-data-dashboard/assets/33475585/b498792d-13a5-4fc1-aef7-8b4d5a1f4a6d)

I re-used the `Country` selector from the previous chart. Based on the selection, I used a `FILTER` formula to display the coffee export quantity for each year from 1990 to 2019. I used this data to create a `line chart` that shows the export trend for the selected country.

---

### Limitations and further improvements
- Amongst the four datasets, there were 2 different kinds of time series. So it wasn't possible to combine data from all the datasets.
- To improve this analysis further, I would start with developing a "guided" visualization, where one can get answers to more specific questions.


