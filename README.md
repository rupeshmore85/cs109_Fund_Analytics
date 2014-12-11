cs109_Fund_Analytics
====================

Topic: Mutual Fund Predictive Analytics:
Course: CS109 Data Science
Harvard University Extension School

Members:

1) Ashwini Patil (ashwini.acpce@gmail.com)
2) Rupesh More (rupeshmore85@gmail.com)

Github Repository: 

CS109_Fund_Analytics : https://github.com/rupeshmore85/cs109_Fund_Analytics

**Overview and Motivation:** Provide an overview of the project goals and the motivation for it. Consider that this will be read by people who did not see your project proposal.

Overview: Predicting the best Mutual funds to invest in based on short/long term goals. The analysis was done on the historical returns data available. We selected top 10 Fund Families based on largest Asset Under Management (AUM). It had approximately 1277 funds from these 10 fund families comprising of all the different Morningstar categories like Large,MidCap,Small, Growth,Blend,Value,Index funds etc. The source of the data were from Morningstar.com, Yahoo finance. The data from Morningstar was scraped using Beautiful Soup and Pandas read_html libraries. Fund parameters like Alpha,Beta,Sharpe Ratio, Sortino Ratio,Standard Deviation, Returns information, Managemanet Information,Holdings information etc. was available in a annualized form on the website. The fund returns plots(funds comparison) were plotted using matplotlib libraries using Yahoo Finance API etc. The NAV information is available on a daily basis on Yahoo Finance servers which helped us to plot these visualizations.

Motivation : Ashwini and Rupesh have been working in finance domain companies and have a collective experience of around 5 years in the industry. We have been working in mutual fund sector on a daily basis in production so we both have a pretty good background in it's functionality. After taking the Data Science class we are highly motivated to apply the algorithms we learnt in class on fund data set. There are various parameters for each Mutual fund based on which a model can be created/based and hence predictions can be made e.g. which amongst the set of large pool of mutual funds will be the best to invest in. We think we can demonstrate this analysis to our managers.




**Related Work:** Anything that inspired you, such as a paper, a web site, or something we discussed in class.

After taking the Data Science course where we learnt different types of regression/prediction techniques. We never got an opportunity to apply such regression techniques on the fund data. We thought this to be an opportunity to predict the best funds available in market for investments. As we took the actual fund data, people can check out our analysis and think on investing :) 




**Initial Questions:** What questions are you trying to answer? How did these questions evolve over the course of the project? What new questions did you consider in the course of your analysis?

1) To filter out bad funds from the pools of different funds available in market.

2) After classification and regression using ensemble techniques, predict the best funds. To show relation between historical expense ratio and returns.

3) Create different models and pick the best one. This aligns with the course syllabus. We have used similar techniques used in Data Science class/Sections/Assignments in our analysis like Cross Validation, Random Forest Classification, Linear Regression. For Visualizations, we used scatter plot, box plot, bar plots , line charts ,histograms, heat maps etc.

4)i) New questions like which are the best funds among different top performing funds? What will be the cumulative sum (cumsum) of the portfolio if we select a subset of the calculated top perfroming funds.

ii) What is the correlation amongst the Top performing funds.

**Data:** Source, scraping method, cleanup, etc.

We used data from Morningstar.com by using web scraping. The data was not in the correct html format so we had to use different techniques in python to align the data in a dataframe for analysis. We had to handle missing values as some of the funds had merged with other funds, data was missing for some of the year. We filled the missing data with appropriate values using ffill() so as to fit the data in a regression model or totally scrap that fund from analysis. We also used Yahoo Finance daily returns data to plot the graphs. We used Beautiful soup web scraping libraries for gathering the data (to loop through different a, tr, th), we also used pandas.readhtml to read the tabular data from the html page. We used firebug lite tools to find the different URI's which had the response data we require.

**Exploratory Analysis:** What visualizations did you use to look at your data in different ways? What are the different statistical methods you considered? Justify the decisions you made, and show any major changes to your ideas. How did you reach these conclusions?

Visualizations like scatter plot, box plot, bar plots , line charts ,histograms, heat maps.
1. Box Plot: We used box plots to decide which estimators give better accuracy for Random Forest classifier using cross validation.
2. Scatter Plot: Scatter plots were used to find the relation between Expense Ratio and Returns, relationship between Risk and Returns.
3. Heat maps: We used heat maps to show the corelation between multiple Top performing funds
4. Line Charts: Line Charts to plot fund returns for multiple top performing funds.
5. Histograms : Histograms to plot distribution of Fund returns.

**Final Analysis:** What did you learn about the data? How did you answer the questions? 
How can you justify your answers?

1. We found out Top performing fund for 3 year, 5year and 10 year data available.
2. **In latest 3 years available data, the mutual fund with less Expense Ratio gives more returns on investments. However in case of 10 year investments, mutual funds with more expense ratio gives more returns.**
3. Justification: We tried Linear Regression and Random Forest Classification. Random Forest Classifer was used to predict Top performing funds with Accuracy of 92 percent. The Linear Regression which was used to predict poor performing fund had the Mean Squared Error to be approximately 0.
4. We identified 155 poor performing funds from the pool of 1277 funds which were consistently giving poor returns and was a total NO for investments.
5. We calculated the cumulative sum of the portfolio if we select a subset of Top performing funds which will help in visualizing the investor's portfolio when these funds are purchased.
