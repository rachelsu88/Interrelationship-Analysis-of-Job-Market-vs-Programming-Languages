# Introduction
This data files is about the US National estimates of rates for job openings, hires, and total separations. And Total separations are broken out into quits, layoffs and discharges, and other separations. All data are presented on a monthly basis. The data range is from 2020-2023. And as required, we mainly focus on the information industry.

# Goals of the analysis
- To find meaningful insights from job openings, hires, and total separations.

- Are there trends in the last decade from the tech (information) industry ?

- What are the connections/relationships between Stack Overflow data files and this datasets ?

# Analysis
## Findings
There was a big spike in total separations in 2020. Then I created a bar chart to show month-by-month total separations in that year and it was clear that March and April had particularly high separation rates. COVID-19 just started to spread in the US during that time.
![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/82e28aaa-d593-43a7-9709-fc52a00c51db)

By-month total separations rate in 2020. March and April had particularly high separation rate.
![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/b77f2371-bfec-4457-867c-8da598ff63e5)

To figure out the reason for the unusual spike from earlier separation rate, created this line chart to further break down the total separation rate into 3 subcategories: quits, layoffs, and other. It became obvious that the spike in 2020 came from layoffs. At the beginning of COVID, businesses had to lay off their employees to survive shutdowns and uncertainties(Grey line spike).
![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/7376a908-ddcf-4d6a-b658-baa7231c1f54)


# Perform Hypothesis 
Using Mann-Kendall Trend Statistical Test:
The Mann-Kendall Trend Test is used to determine whether or not a trend exists in time series data. It does not require that the data be normally distributed or linear. It does require that there is no autocorrelation. 
Mann Kendall Test Result:
![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/07f49deb-b682-4e2f-9af7-64b6f1df9038)


From this result, there is a significant trend in this dataset. Because the p-value is smaller than alpha=0.05, meaning reject null hypothesis and accept the alternative hypothesis. Which indicates “There is a trend in Job Opening”.  The trend is “increasing” and Mann Kendall Test also tells us the value of trend which shows as slope is 0.6.
If making this hypothesis into a graph as below, The blue line in the graph is the actual job opening fluctuation through the year and the red line indicates the increasing trend over the last decade. And the similar for the hire and separartion trend. 

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/0fa318e2-6aae-43a2-a69b-335f2e19ca0d)

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/2e4351b5-136b-44ff-88b8-73b4707e08ef)

verall, statistically speaking, three indicators in jolts data all have increasing trends in the past 10 years. Meanwhile, job opening has the most prominent increasing trend compared to hire and separation. I would conclude that in the information industry, the demand for candidates is greater than the supply could fulfill. 

# Finding the next popular programming languages
Using Mann_Kendall_Test to identify up or donward trends of GO, Rust and Kotlin languages

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/0ef901b1-5d8f-4396-af71-ae2d8f583fe1)

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/5fc19ed2-13b8-4c35-a721-798d1d982d73)

Rust is gaining more interest year over year.

# Relationships Investigation
Using Spearman Coefficient to invest the following corraltions

- If python langusge popularity in the last decase has correlation with Jop opening / Hire trend?
- If R language popularity in the last decase has correlation with Jop opening / Hire trend?
- If SQL language popularity in the last decase has correlation with Jop opening / Hire trend?
- Since Rust was If RUST language popularity in the last decase has correlation with Hire trend?


H0:
There is no correlation existing.

H1:
There is a correlation existing.

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/89566869-03f7-4b5a-a2f7-1d2d5aae6c5d)


![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/8385414f-f0fd-48db-af6f-a7394ebd751e)

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/30bd9951-c4ef-402e-bff3-318fe000d5d5)

![image](https://github.com/rachelsu88/Job-Openings-and-Labor-Turnover-Analysis/assets/157779213/889c4342-9028-4c28-9ec0-af1412f38bb5)









