## About the code
(unfinished project)
Inspired by articles about police departments manipulating their crime and solve rates, I created a case study in an attempt to detect such manipulation. CompStat is a computerization and quantification program set up in the 1990s by the New York Police Department (NYPD) to track crime throughout their jurisdiction. It was one of the first instances of police using data science methods to predict, monitor and attempt to lower crime rates. CompStat and variations thereof were subsequently adopted by many police departments throughout the United States. 

Although CompStat was created with good intentions, there have been subsequent reports of police departments manipulating their data in order to create the impression of low crime rates in their jurisdiction. For example, police departments engage in systematic downgrading, where they file cases as less severe crimes to help lower their numbers for violent or dangerous crimes. 

Because the articles highlighted manipulation of CompStat figures as a potentially significant issue in New York, I decided to compare NYPD to other major cities to see if there were statistically significant differences in their CompStat rates. What was suspicious was that NYPD had a very linearly declining rate of crime for their nonviolent crimes. However, NYPD’s violent crimes were more sporadic and unpredictable. There are potential explanations for this pattern beyond CompStat manipulations. Perhaps petty crimes were going down in New York, or perhaps there were changes in citation and charging policies.  

I took the public police report records and used Natural Language Process (NLP) to sort the crimes based on the charge. I cateogrized all crimes involving murder, attempted murder, rape, battery and/or assault into violent/severe crimes, and other less severe crimes, such as citations for fortune telling, into the less severe crime category. I made a timeline for each month, and made sure to calculate for the population such that the information was sorted into crime per capita. 

I assumed that all the other police departments would have a specific pattern, and for NYPD’s pattern to deviate from that. However, when I input the data, I found that none of the cities had a pattern except NYPD,, leaving me with no way to compare departments and find statistically significant deviation in NYPD’s rates. This meant that anomaly detection was not the best approach to this problem. 

I am continuing to work on this project because I am passionate about this subject of police accountability and the criminal justice system. I started this project before the pandemic and the ensuing events of Summer 2020 regarding racial injustice and police reform only highlighted the importance of this issue. Moving forward, I want to continue to work on my algorithm to try and predict how well future crime rates in cities such as New York correlate to their actual CompStats. 


## Reference

1. [*NYC Open Data NYPD Complaint Data Historical (2006-2017)*](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)
2. [*NYC Open Data NYPD Complaint Data 2018*](https://data.cityofnewyork.us/Public-Safety/NYC-crime/qb7u-rbmr)
3. [*Data Scraping vs Data Crawling* Scraping Etiquette](https://www.datahen.com/data-scraping-vs-data-crawling/)
4. [*San Francisco Complaint Data Historical (2003-2018*](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry)
5. [*Baltimore Open Data Complaint Data Historical (2013-2018)*](https://data.baltimorecity.gov/Public-Safety/Crimes-to-date-in-2013/3h27-ehp2)
6. [*LAPD Open Data Complaint Data Hortorical (2010-2018)*](https://data.lacity.org/A-Safe-City/Crime-Data-from-2010-to-Present/y8tr-7khq)


