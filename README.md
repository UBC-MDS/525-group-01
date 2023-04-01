## 525 Group 1

### Project Description

The purpose of this project is to investigate the downfalls of working with Big Data in plain CSV and `pandas`. We looked into how long it took to download the data using the figshare API, combine the CSVs to into a single file, and load that combined CSV in order to perform EDA in R. Additionally, we tried performing these operations on multiple computers to explore what effect the RAM, processor, and existence of SSD had.

### Data
The data we are using for this project contains information about the daily rainfall in Australia. The combined data included columns: `time`, `lat_min`, `lat_max`, `lon_min`, `lon_max`, `rain (mm/day)`, and `model` (originally separated into different files). The data was downloaded using figshare API using the url: "https://api.figshare.com/v2/articles/14096681".

### Timings

| Team Member | Operating System | RAM | Processor | Is SSD |  Load CSV| Change Dtype | Select Columns | Dtype+Columns | Chunks|
|:-----------:|:----------------:|:---:|:---------:|:------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| Member 1    |  Tanmay Agarwal  | 16.00 GB | Apple M1 Pro |   Yes |   42s | 26.43s | 36.31s | 18.44s | 30.66s|
| Member 2    |  Robin Dhillon   | 16.00 GB | Intel(R) Core(TM) i7-9705h CPU @ 2.60GHz 6 Cores, 12 Logical Processors |  Yes   | 1min 4s  |  32.7 s | 1min 1s | 28.2s | 1min 13s |
| Member 3    |  Mehdi Neji      | 32.00 GB | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz 1.50 GHz |   Yes | 3min 31s| 4.56s| 34.3s| 25.79s |1min 29 s|
| Member 4    |  Ritisha Sharma  | 8.00 GB | Intel(R) Core(TM) i7-7500U CPU @ 2.70GHz | Yes | 10min 25s | 4min 13s | 7min 2s| 5min 14s |10min |

## License

This project is licensed under the terms of the [MIT](LICENSE) license.

## Authors:

This data science project is created for DSCI 525 (Web and Cloud Computing); a course in the Master of Data Science program at the University of British Columbia.

- Robin Dhillon
- Ritisha Sharma 
- Tanmay Agarwal 
- Mehdi Neji 

