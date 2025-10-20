# GuessThatMovie
This is the github repository for group 20 in the SIADS 696 Milesstone II fall semester 2025 class. 

Our datasets can be found here:
Movie Plot Summary Dataset:
https://huggingface.co/datasets/vishnupriyavr/wiki-movie-plots-with-summaries

Movie Quotes Datset:
https://huggingface.co/datasets/jtatman/famous_movie_quotes

Movie Metadata Datasets:
https://datasets.imdbws.com/

Additionally our project report can be found at this link:
https://docs.google.com/document/d/1Vl8aAwYMc-mPSp_PRpPiuJQyRofd13P7XXjMrxKKcwY/edit?usp=sharing


Order of code run: 
1. Run Data Preparation.ipynb--> It will create df_american_movies_post1969.csv file that contains the data for supervised learning.
2. Run Supervised Learning.ipynb. It will create the following files:
   a. SGDClassifier_Hypertuned.joblib
   b. LinearSVC_hypertuned.joblib
   c. Xgboost_Hypertuned.joblib
   d. DummyModel.joblib
   e. LE_wrapper.joblib
   f. hypertune_SGDClassifier.csv
   g. hypertuning_results_LinearSVC.csv
   h. hypertuning_results_Xgboost.csv

3. TreePloy.ipynb --> It will craete a tree plot for the user inputs using LinearSVC model. 
4. <Unsupervised learning files>
5. ClusterPlot.ipynb. It will create cluster plot. 
