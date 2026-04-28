# SEIS 631: Can Astrology Predict How Long a Marriage Will Last?

I have found a dataset on Kaggle of divorce records in Xalapa, Mexico between 2000 and 2015. In this dataset,which is unique from other datasets I found, there was birthdates of the people getting divorced.

I want to create this project as an extention to the project I did in SEIS 632. In that class, I have created visualizations if astrology and divorce have a relationship. While visuals showed no correlation between divorce and astrological sign, I haven't yet tried a permutation test. It gave me an idea of the distribution of data and possible missing data I will be dealing with (that will require bootstrapping).

I want to start by using the numerical column, Marriage Duration, and Astrology Labels. The Astrology Label column was created using a chart that was found online if a star sign couple would be a good match, an okay match, or a bad match. Depending how much marriage duration is reported on the dataset (there's about 4,000 entries) is reported on the dataset, I may need to bootstrap and interpret the results.

Next, this portion will absolutely require bootstrapping as the dataset may be too small, is shuffling the astrology duo labels (that does not consider gender) to see if there's a relationship between marriage duration and astrology labels.

There migh be another interpretation, that does not have to do with astrology, I might do to the dataset such as I noticed a few concerning data points of child marriages.
