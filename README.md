## Table of Contents
1.Problem Statement
2.Result
3.Data
4.Modeling process
5.Evaluation
6.Next Steps
7.About ME
8.Reference


## 1. Problem Statement

New York City has received publicity for systematically downgrading crimes. In layman's terms, New York cops are writing up people for crimes they did not commit to reach a certain quota. Many officers refuse to speak up but some risked their lives to bring light into this corruption.

For those who have spoken up, they have risked their safety. When they call for backup, less officers show up, and the ones that do show up, their lives are at risk as well when they are outnumbered. It deters officers from helping the whistleblowers. And beyond that, some of them distance themselves from their loved ones, concerned that the danger they brought onto themselves will be transferred onto their loved ones.

I wanted to see how they manipulate the data. I’ve read about instances from officers who have spoken out, but I wanted to see how the crime machine works and what numbers are be fabricated.


## 2. Result

At first I considered the potential that perhaps crime is genuinely going down at a somewhat linear rate, maybe the police department gets more funding in New York, or maybe it’s related to the population rate.

I started to be skeptical if there was a significant different to the police report collected in New York compared to other cities. When I skimmed my dataset I found out fortune telling is a crime. New York had more interesting crime descriptions compared to other cities. What is “theft of service”? It’s actually rape, literally. The only difference is if a prostitute gets rape they try to report it as “theft of service” instead of rape.

I cleaned my data and set aside the harsher crimes like things involving the world: murder, homicide rape, kidnapping, or assault. I did this for all the cities, I seperate the crimes that were a huge red card to public safety and from ones that were yellow card. All the cities I observed did not have a pattern except New York. New York’s violent crimes didn’t have a pattern, meaning they aren’t lowering the rates of murder, homicide rape, kidnapping, or assault. New York’s violent crimes had spikes up and down. But the “yellow card” crimes were consistently going down.

It’s more difficult to downgrade or not file a report on murder, homicide, rape, kidnapping, or assault. It would be inhumane to try to fabricate those files when someone has been hurt. But they tried to file rape “theft of service”, so maybe this is a more dangerous issue than a bunch of people in blue uniforms playing with numbers.



## 3. Data

Data was pretty simple to get because it's public records. I searched for Open Data of the city and it's under "Public Safety". The data cost 2G, especially New York. After uploading it to a pandas dataframe I cleaned the dataframe and only kept the absolute information. I kept the data, and the criime description.


## 4. Data Analysis

Initially after cleaning up and graphing the data I tried implementing the Augmented Dickey Fuller Time Series Test to figure out if the graph is stationary or not, basically to see if there is a pattern to the graph. But regardless if there is a pattern or not, it doesn't prove if the New York police report is systematically downgrading.

My next idea was Kolmogorov-Smirnov t-test. Kolmogorov-Smirnov t-test would test the average flux of the graph's movement month-to-month. Through that I would get the p-value, and if the p-value is above the threshold of 0.05 I reject the null hypothesis and the city of New York should re-evaluate the Police Department's priority.


## 5. Evaluation
The p-value did not overcome the 0.05 threshold. Month-to-month has more variance. New York has more severe seasons while in the contrary California has more mild weather. Crime reports does is higher in warmer weathers for the colder areas. My dataset would probably perform better if I didn't seperate the years into months but I don't have enough months lined up.

Severe Crimes (Red Card)
NY /LA 	pvalue=2.791e-21
NY/SF		pvalue=1.010e-67
NY/Balt 	pvalue=1.209e-39

Lesser Crimes (Yellow Card)
NY/LA		pvalue=1.945e-29
NY/SF		pvalue=3.980e-75
NY/Balt	pvalue=2.207e-06

## 6. Next Steps
I would have to be careful with adjusting my p-vales and lower my threshold to make it more difficult to reject my null hypothesis, but I would like to go into each crime and see the statics on each one of them and the rate of change. I would also look into more cities to have data to compare it to. I was thinking of waiting another 5 years and updating with a bigger dataset.



## 7. About the Author

**Jenny Cho** I am a data scientist with a physics background.

To this day I am incapable of sounding words out. I usually know the word or take it apart and look for other words that have similar grouping of letters like prefixes and suffixes. This is how I learned how to read, just a series of memorizing patterns. If you're wondering, yes, I do have dyslexia.

I've always been a visual person, I like visualizing a combination of relationships between letters and numbers. I never considered going into the STEM field until sophmore year of college in my electromagnetism class when I saw all the different directions a charge can go and how it interacts with all the charges around it, I imagined it like dancing. I didn't know what I was going to do in the future with a physics degree, I knew I didn't want to go to grad school for physics but I knew that staying on this path would lead me in the right direction.

I loved my Statistical Thermodyamics Physics class. It wasn't just a class I found interesting but I knew I wanted to do similar math to statistics and quantum mechanics but with more application and less theortical. It was a series of trying to find what that meant, I knew I wanted a job that was about using numbers to create/build something and then optimizing it. Slowly I found my way to Galvanize.


## 8. References

1. [*NYC Open Data NYPD Complaint Data Historical (2006-2017)*](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)
2. [*NYC Open Data NYPD Complaint Data 2018*](https://data.cityofnewyork.us/Public-Safety/NYC-crime/qb7u-rbmr)
3. [*Data Scraping vs Data Crawling* Scraping Etiquette](https://www.datahen.com/data-scraping-vs-data-crawling/)
4. [*San Francisco Complaint Data Historical (2003-2018*](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry)
5. [*Baltimore Open Data Complaint Data Historical (2013-2018)*](https://data.baltimorecity.gov/Public-Safety/Crimes-to-date-in-2013/3h27-ehp2)
6. [*LAPD Open Data Complaint Data Hortorical (2010-2018)*](https://data.lacity.org/A-Safe-City/Crime-Data-from-2010-to-Present/y8tr-7khq)


