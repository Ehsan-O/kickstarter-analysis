# **Fundraising Campaign**
## **Overview of Project**
in this project we are helping a client with her fundrasing campaign

### **Purpose**
Our client is a playwright who wants to start a crowdfunding campaign to help fund her play. She wants to know if there is any relations between the launch date and funding goals of the campaigns and their success rate.
We extracted and used the data from a corowdfunding campaign website to perform our analysis.

## **Analysis and Challenges**
Our analysis consists of two parts as follows
1. Analysis of outcomes based on launch Date of the campaigns related to theater
2. Analysis of outcomes based on fundig goals of play campagins

we elaborate on each in the following sections.

### **Analysis of Outcomes Based on Launch Date**
The launch dates provided in the data (column"J" of the "kickstarter" sheet excel file: kickstarter challenge.xlsx) are unix timestamps so first we needed to convert them to gregorian date format (Column "S" of the kickstarter sheet). then we add another column labaled "years" containing only the year each campaign started so we can filter our data by year if it is needed.
<p float="left">
  <img src="/other/launch-unix.PNG" width="200">
  <img src="/other/date-converted.PNG" width="350">
  <img src="/other/year.PNG" width="140">
</p>  
then we used a pivot table to interprete the data by setting the columns of the table to show the outcomes of the campaign and the rows to show the launch date of them. values in the pivot table are number of each outcome. in the later versions of excel the software automatically groups the dates in row labels and show the months of the year so there is no need to group them manually.we also picked the years and parent category as parameters for filtering the pivot table and set the parent category to "theater". Here is a figure of the pivot table:  


<img src="/other/pivot.PNG" width="500">  

Finally a pivot chart was created based on the pivot table:  


<img src="/resources/Theater_Outcomes_vs_Launch.png">

### **Analysis of Outcomes Based on Goals**
To perform this analysis we dicided the funding goal data into set of intervals and a tabale was created to show the number of successful, failed and canceled campaigns within each interval:  


<img src="/other/goal-table.PNG">  

As mentioned before we created this table based on the data belong to "play" subcategory, a good way to do so is to use "COUNTIFS" function. Here you can see the formula written to calculate the number of successful play campaigns with funding goals in the range of $1000 to $4999:  

<img src="/other/countifs.PNG">  

After calculating the percentage for each outcome by dividing the number of occurance of the outcome by the total number of projects (see the above table) a chart was created to show the percentage of each outcome vs. the funding goal intervals:  

<img src="/resources/Outcomes_vs_Goals.png">  



### **Challenges and Difficulties Encountered**
When using "COUNTIFS" or generally any formula that uses conditional statements one should always make sure that the conditional statements are correct just a making a simple mistake by writing ">" instead of ">=" may cause a big error in final result, something that happened once in our analysis and it took some time to find the source of error.

## **Results**

- Accoording to the chart created to show number of outcomes vs. launch date of campaigns it can be clearly seen that the most number of successful theater campaigns were started in May.
- Also the chart illustrates that December may not be a good time to start a campaign as the number of successful events drops considerably in December.

- The graph for Outcomes vs.funding goals shows that there is a higher probability of success if a playy campaign goal is less than $10000

- the graph also shows that chance of success for a play campaign with a funding goal in the range of $35000 to $44999 is 67 percent but the lack Of data in this range makes this conclusion quastionable.(there are only 9 records in the dataset for tis range compare to almost 900 records for goals under $10000)

- To reach a morb accurate conlusion in our analysis for theater campaigns outcomes based on launch date another graph could have been added to show the prcentage of outcomes vs. lunch date 
