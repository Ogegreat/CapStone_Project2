# CapStone_Project2
This Project was carried out to Analyse Subscription service dataset to discover key insights on the segments and trends of the customers' subscription. 

## Project Topic: Customers Segmentation for a Subscription Service

### Project Overview 
In this project an insights were drawn from the dataset to understand the Subscription Service trends.  Performing data analysis using powerful analytic tools such as 
 Excel, PowerBI to uncover the SubscriptionType that had increased the cancelletions, Revenue generated, Regions with highest increase in Revenue. This helps the Subscription Service to discover what best they are doing and areas that need to be improved on. 

 ### Data Sources
  The primary data used was  MicroSoft Excel file sourced from Online platform, Learning Management System (LMS) which was open to the registered students.

### Tools Used[Download Here](https://www.microsoft.com)
- Microsoft Excel
  1. Microsoft Excel was used for cleaning the data.
  2. It was used in analysis of the data.
  3. Visualization of the data.

- Power BI
  1. Power BI was used in Analysing the data.
  2. It was used to perform Data Analysis Expression such getting Measures.
  3. Visualization of the data.
 
  - Structured Query Language
    1. Structured Query language (SQL) was  used to query the data. This helped to get the retail sales amount, revenue generated, product that made highest sales etc.

  - Git Hub
    1. Git hub was used in Portfolio building.
    2. It was used for group collaboration.
   
  ### Data Cleaning And Preparations
  In this Stage the  following processes were done;
  1. Data was loaded into analytic tools such as MicroSoft Excel and checked.
  2. Checking data type, missing values.
  3. Data cleaning and formatting.
  4. Data profiling.
 
  ### Exploratory Data Analysis
  Exploratory Data Analysis entails explorying the data to get answers to the questions of the stakeholders such as;
  - what was the subscription service overview trends
  - What was the revenue generatated
  - Most popular subscription type
  - What was the subscription type with most cancelletion.
  -  Which month was the highest sales made.

  ### Data Analysis
  Some SQL Server codes and Data Analysis Expression in Power BI  used in fetching the insights from the data are written below;
  ```SQL
 select Region, count(CustomerID) As TotalCustomer from CapstoneData
group by Region 
```
```SQL
select CustomerID,count(SubscriptionType)as MostSubscriptionType from CapstoneData
 group by SubscriptionType, CustomerID order by SubscriptionType
```
```SQL
select DATEDIFF(month,SubscriptionStart, SubscriptionEnd) as Month from CapstoneData where DATEDIFF(month,SubscriptionStart, SubscriptionEnd)<=6
```
```SQL
select SubscriptionType, sum(Revenue) as TotalRevenue from CapstoneData
  group by SubscriptionType
```
```SQL
select count(Canceled) as CancelledSubscription from CapstoneData where Canceled = 1
```
```DAX
AvgSubscriptionPeriod = AVERAGE(CapstoneData[SubscriptionEnd])-AVERAGE(CapstoneData[SubscriptionStart])
```

### Data Visualization
The following visual that draws the insights from the data are displayed below;

![image](https://github.com/user-attachments/assets/6f76eef0-0f1e-4dc5-a8bb-2e6275afe426)

![image](https://github.com/user-attachments/assets/16d5fad1-41bc-48ef-a3c2-9624d2f1ab0d)


