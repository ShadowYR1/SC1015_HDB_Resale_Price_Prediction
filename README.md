# HDB Resale Price Prediction

# About
This is a mini project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on HDB resale flats that were sold as listed in [Resale flat prices based on registration date from Jan-2017 onwards](https://data.gov.sg/datasets/d_8b84c4ee58e3cfc0ece0d773c8ca6abc/view). (Data up to 2024 Q2 was used)

Please go through the notebooks in this order:
1. [Preprocessing_Scraping](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Preprocess_Scraping.ipynb) (Dataset already has scraped data combined)
2. [EDA](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_EDA.ipynb)
3. [Feature Experimentation (Distance To School)](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Experimental_EDA.ipynb)
4. [Feature_Selection_Model_Training](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Feature_Selection_Model_Training.ipynb)

# Contributors:
- @ShadowYR1 - Dataset Curation (Scraping + Merging), EDA, ML Model Training
- @ignit333 - EDA, Feature Experimentation, Presentation Slides
- @Lazermaster - EDA, Hyperparameter Tuning (GridSearchCV)

# Motivations:
Help buyers make more informed decisions on:
1. Which resale HDB flat to choose
2. Whether a resale HDB flat is worth its listed price

# Problem Definition:
- Given a set of features about the flat, can we determine its price adjusted for inflation (base of 2017 Q1)

# Models Used:
- Decision Trees<br>
&nbsp;&nbsp;&nbsp; - Used due to EDA proving splits help boost correlation with continuous features. A combination as such &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;using Decision Trees may prove useful.
- Random Forest<br>
&nbsp;&nbsp;&nbsp; - Used knowing that a ensemble of Decision Trees may better aid predictions on certain flats 
- XGBoost<br>
&nbsp;&nbsp;&nbsp; - Weak learners (e.g. decision trees) are stacked sequential that may help improve on predictions of a &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;single iteration of output from decision tree

# Conclusion:
<b>1.</b> Flat types, Remaining lease and Town are the top 3 features in predicting the price of the resale HDB flats<br><br>
<b>2.</b> Central areas tend to command higher prices. This might be due to proximity to other parts in Singapore or the Central business district<br><br>
<b>3.</b> In general, flats of higher prices produce larger errors<br><br>
<b>4.</b> Distance features may not be as important to narrow down the prediction of adjusted_price to values near actual adjusted_price<br><br>
<b>5.</b> The model can be used to identify if HDB Resale Flat is worth its listed price with exceptions to Multi-generation. This may be due to the limited data available.


# What did we learn:
<b>1.</b> Feature engineering such as clustering, ordinal encoding by medians, feature creation<br><br>
<b>2.</b> How to work with models such as XGBoost and Random Forest<br><br>
<b>3.</b> How to tune hyperparameter of models using methods like GridSearchCV

# References
https://github.com/chengguan/pyonemap/blob/main/pyonemap/onemap.py<br><br>
https://www.businesstimes.com.sg/property/hdb-resale-prices-continue-rising-october-while-transaction-volume-falls-srx-99-co<br><br>
https://www.channelnewsasia.com/commentary/singapore-hdb-flats-million-dollar-resale-deals-public-housing-sentiment-affordability-4728281<br><br>
https://www.straitstimes.com/singapore/housing/number-of-million-dollar-hdb-flats-resold-hit-all-time-high-in-june-prices-up-18-srx-99co<br><br>
https://www.moe.gov.sg/primary/p1-registration/distance<br><br>
https://www.creativecampus.com.sg/best-primary-schools-in-singapore-2024<br><br>
https://www.creativecampus.com.sg/best-secondary-schools-in-singapore-2024<br><br>
https://www.creativecampus.com.sg/top-junior-colleges-jc-in-singapore-2024<br><br>

# Datasets Used:
[ResaleflatpricesbasedonregistrationdatefromJan2017onwards](https://data.gov.sg/datasets/d_8b84c4ee58e3cfc0ece0d773c8ca6abc/view)

[Generalinformationofschools](https://data.gov.sg/datasets/d_688b934f82c1059ed0a6993d2a829089/view)

[HDBResalePriceIndex1Q2009100Quarterly](https://data.gov.sg/datasets/d_14f63e595975691e7c24a27ae4c07c79/view)
(before recent update for 2024 Q3)

[LTAMRTStationExitGEOJSON](https://data.gov.sg/datasets/d_b39d3a0871985372d7e1637193335da5/view)

[NParksParksandNatureReserves](https://data.gov.sg/datasets/d_77d7ec97be83d44f61b85454f844382f/view)

[Parks](https://data.gov.sg/datasets/d_0542d48f0991541706b58059381a6eca/view)

[SportsFieldsSG](https://data.gov.sg/datasets/d_f71b449b4b43a69b5ecfe411b440d249/view)

[SportSGSportFacilitiesGEOJSON](https://data.gov.sg/datasets/d_9b87bab59d036a60fad2a91530e10773/view)
