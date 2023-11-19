# Coffee Production and Trade data
An interactive dashboard created in Excel that shows trends and information about countries that produce, export, and import coffee.\
[Link to dashboard](https://onedrive.live.com/edit.aspx?resid=784924BC0EF8BD53!3652&cid=784924bc0ef8bd53&CT=1700339340611&OR=ItemsView)\
\
Data Source - [Kaggle link](https://www.kaggle.com/datasets/michals22/coffee-dataset/data) \
OG Source - [International Coffee Organization](https://icocoffee.org/)

I begin every day with a cup of hot steaming coffee. I mean, there's no other way to start the day! 
So when I came across this dataset, I decided to dive into it and explore some interesting trends in the data.

---

#### Design of the dashboard
I wanted to design the dashboard in a way that presents some obvious facts and allows one to explore some trends in the data based on individual interests. 
Hence, I start with the **Top 5** countries for each of the trade activities. Then I move to the **interactive** elements of the dashboard that allow for *Exploratory Data Analysis*.


4. A dynamic chart that shows coffee production vs domestic consumption of the selected country.
5. A dynamic chart that shows the trend of coffee exports for the selected country between the years 2019 to 2020.
   *The same country selection is used for the dynamic charts in 4 and 5.

#### Specific components of the dashboard
Here, I explain the data preparation process and the specific formula to create a chart or component.

##### 1. Charts showing the top 5 countries producing, exporting, and importing coffee.
I created 3 `Pivot Tables`
| Country | Total Production |
| --- | --- |

| Country | Total Export |
| --- | --- |

| Country | Total Import |
| --- | --- |

and filtered the results in `descending` order of the `total` and chose the `top 5` results for each table. I used the filtered data to create a `horizontal bar chart`.

##### 2. A dynamic chart that shows the top 5 countries for the selected coffee type.
First, I created a `Pivot Table`
| Coffee Type | Country | Total Production |
| --- | --- | --- |

and filtered the results in `descending` order of the `total` and chose the `top 5` countries for each coffee type.\
Next, I added a `Data Validation` selector for the `coffee type`. Based on the selection, I added a `FILTER` formula to display the top 5 countries for the selected coffee type from the table. I used the filtered data to create a `bar chart`.

##### 3. A dynamic chart that shows the trend of coffee imports for the selected country between the years 2019 to 2020.



#### Limitations and further improvements
