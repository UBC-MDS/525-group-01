## 525 Group 1

### Project Description

The purpose of this project is to investigate the downfalls of working with Big Data in plain CSV and `pandas`. We looked into how long it took to download the data using the figshare API, combine the CSVs to into a single file, and load that combined CSV in order to perform EDA in R. Additionally, we tried performing these operations on multiple computers to explore what effect the RAM, processor, and existence of SSD had.

### Data
The data we are using for this project contains information about the daily rainfall in Australia. The combined data included columns: `time`, `lat_min`, `lat_max`, `lon_min`, `lon_max`, `rain (mm/day)`, and `model` (originally separated into different files). The data was downloaded using figshare API using the url: "https://api.figshare.com/v2/articles/14096681".

#### Problems and Challenges
There were plenty of challenges we faced in completing these tasks. The notebook does not display the EDA results in R. Running those cells caused the computer to freeze and crash, or it was taking more than 30 mins. Other tasks also took very long to run so it was difficult to debug the code and examine whether we were getting the right results. The strain of the tasks caused one of the team member's computer to freeze. One way we tackled these challenges was to run parrallel on multiple computers: each team member created a separate notebook to record how long it took their computer to perform the operations mentioned above. 

#### Parquet
We chose to use Parquet file-format to transfer the dataframe. It is a hybrid file-format which means that we can benefit from the pros of columnar and row-based approaches. It also works with any programming language. 

### Timings

| Team Member | Operating System | RAM | Processor | Is SSD |  Load CSV| Change Dtype | Select Columns | Dtype+Columns | Chunks|
|:-----------:|:----------------:|:---:|:---------:|:------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| Member 1    |  Tanmay Agarwal  | 16.00 GB | Apple M1 Pro |   Yes |   52s | 26.43s | 56.31s | 18.44s | 30.66s|
| Member 2    |  Robin Dhillon   | 16.00 GB | Intel(R) Core(TM) i7-9705h CPU @ 2.60GHz 6 Cores, 12 Logical Processors |  Yes   | 1min 4s  |  32.7 s | 1min 1s | 28.2s | 1min 13s |
| Member 3    |  Mehdi Neji      | 32.00 GB | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz 1.50 GHz |   Yes | 3min 31s| 4.56s| 34.3s| 25.79s |1min 29 s|
| Member 4    |  Ritisha Sharma  | 8.00 GB | Intel(R) Core(TM) i7-7500U CPU @ 2.70GHz | Yes | 10min 25s | 4min 13s | 7min 2s| 5min 14s |10min |

#### Summary of Observations
There are large differences in the time it took to combine the data and load it to perform EDA between all the team members. The fastest time to combine the data was 5min 19s with 16.00 GB RAM, Apple M1 Pro processor, and with SSD. The slowest was 26 min with 32.00 GB RAM, Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz 1.50 GHz, and with SSD. The slowest method of loading the combined CSV  was to just naively load it using `pandas`. Changing the datatype lead to a large improvement in performance. Some team members were able to load the data using the improved methods in under a minute. 

## License

This project is licensed under the terms of the [MIT](LICENSE) license.

## Authors:

This data science project is created for DSCI 525 (Web and Cloud Computing); a course in the Master of Data Science program at the University of British Columbia.

- Robin Dhillon
- Ritisha Sharma 
- Tanmay Agarwal 
- Mehdi Neji 

