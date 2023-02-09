# Analyzing_Web_Server_Logs_with_Apache_Spark

Using Spark to analyze real-world production logs from NASA on Databrick community version. The logs are in common log format [1]. Practice the extract, transform, and load (ETL) process [2] in Spark enviroment. Here is a summary: 


## About the code  

1. Load the log dataset. View the meta data and sample data.  
2. Start data transformation <br>
  a. Define regex patterns to extract information from input log string. The column data that are extracted are: host, timestamp, method, endpoint, protocol, status, content_size. <br>
  b. Find missing values. Fill the null cells by mapping them with 0 value.  <br>
  c. Parse the original non-standard timestamp column into a standard timestamp column.  <br>
3. Perform exploratory data analysis (EDA) [3] on the logs <br>
  a. Use describe to compute the statistics of the columns. Can also be done using pyspark.sql functions.  <br>
  b. Analyze HTTP status code <br>
  c. Analyze frequent hosts, frequent endpoints, and error endpoints.  <br>
  d. Analyze number of unique daily hosts <br>
  e. Analyze 404 errors per day <br>
4. Load data into DBFS in the csv and json format 






## References 
[1] https://en.wikipedia.org/wiki/Common_Log_Format <br>
[2] https://en.wikipedia.org/wiki/Extract,_transform,_load </br>
[3] https://en.wikipedia.org/wiki/Exploratory_data_analysis <br>



