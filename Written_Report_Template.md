# Kickstarting with Excel

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
The launch dates provided in the data (column"J" of the "kickstarter" sheet excel file: kickstarter challenge.xlsx) are unix timestamps so first we needed to convert them to gregorian date format (Column "S" and "T" of the kickstarter sheet). then we add another column labaled "years" containing only the year each campaign started so wecan filter our data by year if it is needed.
<p float="left">
  <img src="/other/launch-unix.PNG" width="200">
  <img src="/other/date-converted.PNG" width="350">
  <img src="/other/year.PNG" width="140">
</p>  
then we used a pivot table to interprete the data by setting the columns of the table to show the outcomes of the campaign and the rows to show the launch date of them. values in the pivot table are number of each outcome. in the later versions of excel the software automatically groups the dates in row labels and show the months of the year so there is no need to group them manually.we also picked the years and parent category as parameters for filtering the pivot table and set the parent category to "theater". Here is a figure of the pivot table:  


<img src="/other/pivot.PNG" width="500">  

Finally a pivot chart was created based on the pivot table:  


<img src="/resourses/Theater_Outcomes_vs_Launch.png">

### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
