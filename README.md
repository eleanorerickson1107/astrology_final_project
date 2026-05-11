# Can Astrology Predict How Long a Marriage Will Last?

## 1. Research Question
Does astrology predict how many years a marriage will last? From a project I have done in SEIS 632, I have found through data visualization of divorce records from Xalapa, Mexico that there was no relationship between astrology and divorces: No star sign duos stuck out and most relationships according to astrology should have a "happily ever after." However, I wanted to take this a step further and use a permutation test and bootstrapping to see if the data was by random chance or if in fact there is a relationship between how long a marriage will last and astrology.
## 2. Hypothesis
* Overall: There is no relationship between astrological sign and years a couple will stay married based on the observed mean.
* Capicorn and Picses Couples: There is no relationship between Pisces and Capicorn couples and years a couple will stay married based on the observed median.
## 3. Data Description
Describe your data source(s):
* Data source: From Kaggle, Divorce records in Xalapa Mexico between 2000 and 2015 (https://www.kaggle.com/code/aagghh/python-vs-astrology-testing-zodiac-predictions?scriptVersionId=47561319&cellId=4)
* Observation were of straight couples and each observation had 50 columns: With each partners date of marriage, date of birth, nationality, place of birth, data of divorce, occupations, salary, voluntary or nessessary divorce, number of children, and custody of children.
* Number of observations and key variables: Originally with 4,923 observations that were cut down to 4,374 from the last project. Key variables in this project were were birthdate, years of marriage, 
* Any filtering, cleaning, or transformation steps:
  * Originally shaved down to 4,374 oberservations due to missign birthdates of one or both partners
  * Add in astological sign of a partner based on their birthdate and then combined the couples star sign that disregards star sign (Aires and Gemini or Gemini and Aires would simply be Aires and Gemini).
* More columns added (not relevent to the null hypothesis, used in other tests)
  * Age of Marriage of man partner and woman partner (Date of Marriage minus Date of Birth)
  * Age Gap (Man Partner Age minus Woman Partner Age)
  * Flagged Couples: One partner was married at less than 18 years of age and the other partner be 2 years older
## 4. Methods
Summarize how you analyzed the data:
* The test statistic for your permutation test
  * Pisces and Capicorn Couples in this dataset would stay married for 14 years based on median (the highest average from the dataset)
  * Each star sign duos respective average years of staying married in this dataset
* How you simulated or resampled under the null hypothesis
  * Replicated to have a total of 1,000 observations
  * Then took a random sample 10,000 and also included the the observed average
* The metric(s) for which you created bootstrap confidence intervals
  * Using the replicated average from Pisces and Capicorn couples and calculated the mean and then using a 95% confidence interval
* Why the CLT does not apply to at least one metric
  * For the Capicorn and Pisces, there was only 27 observations.
  * The distribution of the filtered Capicorn and Pisces data was bimodal before replication
  * Using the observed median on 14 years for Capicorn and Pisces median marriage duration
  * Replicated the Capicorn and Pisces data 10,000 based on the median with replacement
  * Resulted in a right-skewed histogram (most marrianges lasting less than the median of 14 years)
## 5. Results
Present your main findings:
* Key summary statistics and visualizations:
  * Histogram of Pisces and Capicorn couples, most of the values were less than the median of 14 years and resulted in a right-skewed histogram
* Observed test statistic and p-value (if applicable)
  * Pisces and Capicorn and the median duration of marriage resulted in a P Value of 0.58
  * Other star sign duos had P Values between 0.43 and 0.54 based on their means
  * No evidence between average duration of marriage and all star sign duos
* Bootstrap confidence intervals for relevant metrics
  * The replicated data of marriages were expected to last between 14.80640 and 15.29560 years for a Capicorn and Pisces couple with a 95% confidence interval
## 6. Uncertainty Estimation
Discuss your resampling results:
* How many resamples you used
  * For Pisces and Capicorn Marriages: 10,000 resamples, taking one value of the 1,000 replicated values
  * For all Star Sign Duo Marriages: 10,000 resamples, taking one value of the 1,000 replicated values
* What the bootstrap or randomization distributions looked like
  * For Pisces and Capicorn Marriages: Right-skewed data, most values being under the median of 14 years
  * For all Star Sign Duo Marriages: They all should have normal distributions with most values centered at the observed mean
* How you interpret the interval estimates
 * Pisces and Capicorn couples were expected to last between 14.80640 and 15.29560 years
## 7. Limitations
Briefly note any limitations in data, assumptions, or methods, including sources of
bias or missing data.
* Limited to the city of Xalapa, Mexico
* Does not apply to couples still married, that are seperated, or LGBTQIA+.
* Possibility of missing records (the entirity of 2015 was not recorded)
## 8. References
Dataset: https://www.kaggle.com/code/aagghh/python-vs-astrology-testing-zodiac-predictions?scriptVersionId=47561319&cellId=4

---
