# Movies-ETL

For this module, the Extract, Transform, Load (ETL) process was used to create multiple data pipelines. The ETL process was used to create data pipelines that helps transform the data. My Movies-ETL uses Kaggle data. The Kaggle dataset pulls from the MovieLens dataset which has millions of files with details from the TMDB Movie database. I downloaded the zip file from Kaggle, extracted, and decompressed the CSV files. I only used the movies_metadata.csv and ratings.csv files. The data provied exists in a copule places and my first step is to clean and restructure the data before I can analyze it. The three phases I will use are: Extract, Transform, and Load. First, I scraped Wikipedia data stored as a JSON, and Kaggle data stored in CSVs. Second, I used Python and Pandas to explore, document, and perform the data transformation. Thirdly, I loaded the data into a PostgreSQL table.

My five assumptions:
1) Both title options from the data look consistent, but the Kaggle data held more confidence in the title name consistency and using the code was able to confirm zero missing titles in the Kaggle data.
2) The Kaggle data have any missing release dates so I kept the Kaggle information.
