# GuessThatMovie
This is the GitHub repository for group 20 in the SIADS 696 Milestone II fall semester 2025 class. 

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
 **Output**: It will create df_american_movies_post1969.csv file that contains the base data for supervised and unsupervised learning. A sample of the first 100 rows of this dataset is provided ( First_100_Prepared_Data.csv)

2. Run 2.Supervised Learning.ipynb.
   **Input**: df_american_movies_post1969.csv
   **Output**: It will create the following files:
   a. SGDClassifier_Hypertuned.joblib
   b. LinearSVC_hypertuned.joblib
   c. Xgboost_Hypertuned.joblib
   d. DummyModel.joblib
   e. LE_wrapper_hypertuned.joblib
   f. hypertune_SGDClassifier.csv
   g. hypertuning_results_LinearSVC.csv
   h. hypertuning_results_Xgboost.csv

3. Run 3.TreePloy.ipynb
   **Inputs**: "LinearSVC_hypertuned.joblib", "LE_wrapper_hypertuned.joblib", 5 user inputs ( raw string, 0 or 1 (corresponding to whether the movie was released before the year 2000), movie genre, actor, director)
   **Output:** It will create a tree plot for the user inputs using the LinearSVC model. 
4. Run 4.Unsupervised learning files
   **Inputs**: df_american_movies_post1969.csv
   **Outputs**: Contains function that returns 5 most similar movies to user input
Extra. ClusterPlot.ipynb. It will create a cluster plot. Not used in final report.
