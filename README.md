# Movies-ETL

For this module, the Extract, Transform, Load (ETL) process was used to create multiple data pipelines. The ETL process was used to create data pipelines that helps transform the data. My Movies-ETL uses Kaggle data. The Kaggle dataset pulls from the MovieLens dataset which has millions of files with details from the TMDB Movie database. I downloaded the zip file from Kaggle, extracted, and decompressed the CSV files. I only used the movies_metadata.csv and ratings.csv files. The data provided exists in a few different places and my first step is to clean and restructure the data before I can analyze it. The three phases I will use are: Extract, Transform, and Load. First, I scraped Wikipedia data stored as a JSON, and Kaggle data stored in CSVs. Second, I used Python and Pandas to explore, document, and perform the data transformation. Thirdly, I loaded the data into a PostgreSQL table.

My five assumptions:
1) Both title options from the data look consistent, but the Kaggle data held a higher degree of confidence in the title name consistency and using the code was able to confirm zero missing titles in the Kaggle data.
2) The Kaggle data didn't have any missing release dates so I kept the Kaggle information.
3) The budget_wiki and budget_kaggle are both numeric so we used a scatter plot to compare the values:
I found that the Wikipedia data has more outliers versus the Kaggle data. Upon further review, I found that in the Kaggle columnm, there are quite a few movies without key pieces of information. So I used Wikipedia’s data.
4) Due to the Kaggle consistency in data, and the difficulty in translating the inconsistent Wikipedia data into the same unique format I decided to drop the Wikipedia data.
5) Most runtimes were fairly similar in time; however, the Wikipedia data did have some outliers, so the Kaggle data is assumed to be a better option in the merge. Unfortunately, I saw from the scatter plots that Kaggle has 0 for the runtime but Wikipedia actually had the data, so I used the Wikipedia data.
