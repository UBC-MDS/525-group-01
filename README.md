## 525 Group 1
Authors:
- Tanmay Agarwal
- Robin Dhillon
- Mehdi Neji
- Ritisha Sharma

### Project Description

The purpose of this project is to investigate the downfalls of working with Big Data in plain CSV and `pandas`. We looked into how long it took to download the data using the figshare API, combine the CSVs to into a single file, and load that combined CSV in order to perform EDA in R. Additionally, we tried performing these operations on multiple computers to explore what effect the RAM, processor, and existence of SSD had.

#### Problems and Challenges
There were plenty of challenges we faced in completing these tasks. Since it took very long to run, it was difficult to debug the code and examine whether we were getting the right results. The strain of the tasks caused one of the team member's computer to freeze. One way we tackled these challenges was to run parrallel on multiple computers: each team member created a separate notebook to record how long it took their computer to perform the operations mentioned above. 

#### Parquet
We chose to use Parquet file-format to transfer the dataframe. It is a hybrid file-format which means that we can benefit from the pros of columnar and row-based approaches. It also works with any programming language. 

### Timings

| Team Member | Operating System | RAM | Processor | Is SSD | Time to combine data CSVs | Time to load combined CSV and perform EDA|
|:-----------:|:----------------:|:---:|:---------:|:------:|:----------:|:----------:|
| Member 1    |  Tanmay Agarwal  | 16.00 GB    | Apple M1 Pro          |   Yes     |  5min 19s          | 42s|
| Member 2    |  Robin Dhillon   | 16.00 GB | Intel(R) Core(TM) i7-9705h CPU @ 2.60GHz 6 Cores, 12 Logical Processors |  Yes   |  9min 43s  |1min 4s |
| Member 3    |  Mehdi Neji      | 32.00 GB | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz   1.50 GHz   |   Yes      |    26 min        | 1 min and 53 s|
| Member 4    |  Ritisha Sharma  | 8.00 GB | Intel(R) Core(TM) i7-7500U CPU @ 2.70GHz | Yes | 22min 13s | 10min 25s |

#### Summary of Observations
There are large differences in the time it took to combine the data and load it to perform EDA between all the team members. The fastest time to combine the data was 5min 19s with 16.00 GB RAM, Apple M1 Pro processor, and with SSD. The slowest was 26 min with 32.00 GB RAM, Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz 1.50 GHz, and with SSD. The slowest time to load combined CSV and perform the EDA was 10min and 25s with 8.00 GB RAM, Intel(R) Core(TM) i7-7500U CPU @ 2.70GHz, and with SSD. Others were able to perform this task in the range of 1 to 2 minutes so this was slower by a considerable margin. 
