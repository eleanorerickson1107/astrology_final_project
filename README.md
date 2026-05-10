# Can Astrology Predict How Long a Marriage Will Last?

## 1. Research Question
Does astrology predict how many years a marriage will last? From a project I have done in SEIS 632, I have found through data visualization of divorce records from Xalapa, Mexico that there was no relationship between astrology and divorces: No star sign duos stuck out and most relationships according to astrology should have a "happily ever after." However, I wanted to take this a step further and use a permutation test and bootstrapping to see if the data was by random chance or if in fact there is a relationship between how long a marriage will last and astrology.
## 2. Hypothesis
Overall: There is no relationship between astrological sign and years a couple will stay married.
## 3. Data Description
Describe your data source(s):
* Where it comes from (URL, API, dataset name): Kaggle, Divorce records in Xalapa Mexico between 2000 and 2015: https://www.kaggle.com/code/aagghh/python-vs-astrology-testing-zodiac-predictions?scriptVersionId=47561319&cellId=4
* Observation were of straight couples: With each partners date of marriage, date of birth, nationality, place of birth, data of divorce, occupations, salary, voluntary or nessessary divorce, number of children, and custody of children.
* Number of observations and key variables: Originally with 4,923 obervations that were cut down to 4,374 from the last project. Key variables in this project were were birthdate, years of marriage, 
* Any filtering, cleaning, or transformation steps: Originally shaved down to 4,374 oberservations due to missign birthdates of one or both partners. Did add in astological sign of a partner based on their birthdate and then combined the couples star sign that disregards star sign (Aires and Gemini or Gemini and Aires would simply be Aires and Gemini). I did add some more columns along the way......
## 4. Methods
Summarize how you analyzed the data:
* The test statistic for your permutation test
  * Pisces and Capicorn Couples in this dataset on average stay married for 15.78 years (the highest average from the dataset)
  * Each star sign duos respective average years of staying married in this dataset
* How you simulated or resampled under the null hypothesis
  * Replicated to have a total of 1,000 observations
  * Then took a random sample 10,000 and also included the the observed average
* The metric(s) for which you created bootstrap confidence intervals
  * Using the replicated average from Pisces and Capicorn couples and calculated the mean and then using a 95% confidence interval
* Why the CLT does not apply to at least one metric
  * For the Capicorn and Pisces, there was only 27 observations.
  * The distribution of the filtered Capicorn and Pisces data was bimodal
## 5. Results
Present your main findings:
* Key summary statistics and visualizations:
  * 
* Observed test statistic and p-value (if applicable)
  * Pisces and Capicorn and the average duration of marriage resulted in a P Value of 0.52
  * Other star sign duos had P Values between 0.43 and 0.53
  * No evidence between average duration of marriage and all star sign duos
* Bootstrap confidence intervals for relevant metrics
  * For a Capicorn and Pisces couple, the marriages lasted between 15.71076 and 15.92412 years
## 6. Uncertainty Estimation
Discuss your resampling results:
* How many resamples you used
  * 10,000 resamples
* What the bootstrap or randomization distributions looked like
  * Normal distribution with most values around the mean
* How you interpret the interval estimates
## 7. Limitations
Briefly note any limitations in data, assumptions, or methods, including sources of
bias or missing data.
* Limited to the city of Xalapa, Mexico
* Does not apply to couples still married, that are seperated, or LGBTQIA+.
* Possibility of missing records (the entirity of 2015 was not recorded)
## 8. References
List all datasets, tools, libraries, or papers you cited.
---
**Reminder:** Your README should be clear enough that someone unfamiliar with your
work could understand
