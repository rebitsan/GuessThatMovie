# GuessThatMovie
This is the github repository for group 20 in the SIADS 696 Milesstone II fall semester 2025 class. 

Our datasets can be found here:
Movie Plot Summary Dataset:
https://huggingface.co/datasets/vishnupriyavr/wiki-movie-plots-with-summaries

Movie Metadata Datasets:
https://datasets.imdbws.com/

Additionally our project report can be found at this link:
https://docs.google.com/document/d/1Vl8aAwYMc-mPSp_PRpPiuJQyRofd13P7XXjMrxKKcwY/edit?usp=sharing


**The Order of code run:** 
1. Run Data 1.Preparation.ipynb.
 **Inputs**: Requires the following input data files:
 a. 0000.parquet - https://huggingface.co/datasets/vishnupriyavr/wiki-movie-plots-with-summaries/tree/refs%2Fconvert%2Fparquet/default/train
 b. title.basics.tsv.gz - https://datasets.imdbws.com/
 c. title.crew.tsv.gz - https://datasets.imdbws.com/
 d. title.principals.tsv.gz - https://datasets.imdbws.com/
 e. name.basics.tsv.gz - https://datasets.imdbws.com/
 **Output**: It will create df_american_movies_post1969.csv file that contains the data for supervised learning. A sample of first 100 rows of this dataset is provided ( First_100_Prepared_Data.csv)

2. Run 2.Supervised Learning.ipynb.
   **Output**: It will create the following files:
   a. SGDClassifier_Hypertuned.joblib
   b. LinearSVC_hypertuned.joblib
   c. Xgboost_Hypertuned.joblib
   d. DummyModel.joblib
   e. LE_wrapper_hypertuned.joblib
   f. hypertune_SGDClassifier.csv
   g. hypertuning_results_LinearSVC.csv
   h. hypertuning_results_Xgboost.csv

4. Run 3.TreePloy.ipynb
   **Output:** It will create a tree plot for the user inputs using the LinearSVC model. 
5. Unsupervised learning files
6. ClusterPlot.ipynb. It will create a cluster plot. 
