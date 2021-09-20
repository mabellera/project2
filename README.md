Analysis of the Post-Live Service Data.

Problem Definition:

This department has had a billable hours growth of 79.6% between 2018 and 2020 and a number of projects requested growth of 150%. This analysis is intended to help us identify the different factors that are causing the growth.

One of the biggest challenges is that the data sets available need data cleaning, filtering, joins and aggregation which will be performed as part of this project.

Data Sets Used:

This is a real-life project from my company. Due to rights to access the database, I had to request our data analytics team to export the .csv files for me. In order for me to know what I needed to request, I had to understand the context of what I was trying to achieve.

The data sources are:

- PostLiveData: contains: arnumber (which is the unique identifies for clients)	projectname,	startdate,	enddate,	startyear,	resourcename,	professionalservicegroup,	plannedhours,	billablehours and	status. This table contains 10564 rows with historical project data between 2018 to date.

- CustomerData: contains: arnumber,	customertype,	industrygroup,	isterminated,	supportmodel,	liveyear,	livequarter,	livemonth,	vertical. This table contains 2373 rows with historical customer data between 2018 to date.

Extract:

- 2 .csv files: PostLiveData and CustomerData.

Transform:

Data Clearning: the biggest effort was around bringing consistency to projectname. Initially, arnumber, projectname and startyear were on the same column. I used the split_part() function to separate them.

Summarization, selection, filtering and aggregation was performed in pandas (see file).

Load:

I work with pgAdmin and created a database, which I also split in different years to facilitate analysis.

![image](https://user-images.githubusercontent.com/84101029/133950938-30ab65c6-ddc5-48f3-bde4-ff08611c37a3.png)


![image](https://user-images.githubusercontent.com/84101029/133949787-fe3ebcf8-48c9-4ec9-847f-95166e5ca8d2.png)


