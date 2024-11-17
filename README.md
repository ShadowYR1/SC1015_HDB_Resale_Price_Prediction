# HDB Resale Price Prediction

# About
This is a mini project for SC1015 (Introduction to Data Science and Artificial Intelligence which focuses on resale flats that were sold as listed in [Resale flat prices based on registration date from Jan-2017 onwards](https://data.gov.sg/datasets/d_8b84c4ee58e3cfc0ece0d773c8ca6abc/view). (Data up to 2024 Q2 was used)

Please go through the notebooks in this order:
1. [Preprocessing_Scraping](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Preprocess_Scraping.ipynb) (Dataset already has scraped data combined)
2. [EDA](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_EDA.ipynb)
3. [Feature_Selection_Model_Training](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Feature_Selection_Model_Training.ipynb)

# Contributors:
- @ShadowYR1 - Data Scraping and collating, EDA, Base model training
- @ignit333 - EDA, [Expermental EDA on Distance to Schools](https://github.com/ShadowYR1/SC1015_HDB_Resale_Price_Prediction/blob/main/SC1015_Experimental_EDA.ipynb), Presentation slides
- @Lazermaster - EDA, Hyperparameter tuning, GridSearch
# Motivations:
<b>1.</b> How can we help buyers know if a flat is worth its price?
<b>2.</b> How can we help buyers better negotiate prices of resale flats?

# Problem Definition:
- Given a set of features about the flat, can we determine its price adjusted for inflation (base of 2017 Q1)

# Models Used:
- Decision Trees
- Random Forest
- XGBoost

# Conclusion:
<b>1.</b> Flat types plays a major role in the price of the resale flat<br><br>
<b>2.</b> Central areas tend to command higher prices. This might be due to proximity to other parts in Singapore or the Central business district<br><br>
<b>3.</b> Higher value resale flats such as those near a million dollars in general have higher errors and larger error standard deviation. This might also suggest the value of such flats are more subjective and less deterministic. It might also be the relatively lesser amounts of data of such flats.<br><br>
<b>4.</b> Distance features may not be as significant in pricing. 

# What did we learn:
<b>1.</b> Feature engineering such as clustering categories and ordinal encoding by medians<br><br>
<b>2.</b> How to work with models such as Random Forest and XGBoost<br><br>
<b>3.</b> How to hyperparameter tune with methods such as scikit-learn’s RandomizedSearchCV

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
