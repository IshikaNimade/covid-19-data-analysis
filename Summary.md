Detailed ProblemStatement:
A. Need to create a data flow pipeline ,where data initially resides in 
   RDBMS and needs to be brought to Hive so as to get a consolidated 
   view of covid cases details as well as testing details,taken together
   in onetable.
   
B. Optimizations during sqoop import/export , hive optimizations have to 
   be considered. Also password encryption in sqoop to be used.
   
C.The data field is not in proper format and has to be taken care 

D. Try to infer from the final consolidated table in Hive like whether 
   there is any discrepency between Number of confirmed covid cases in 
   the state Vs.Number of Positive Samples collected during testing.
   Which states hows least discrepency.
   
E. Run some more interesting queries from your end in hive to get more 
   insights on the consolidated data.
   
   
 Sample Query-
 For every state,find the total number of confirmed cases reported and also 
 total number of positive samples tested,in the entire duration of 2 months,starting with
 the state with the highest cases.
 
 
 
Steps Overview:
Step1. Data Preprocessing-
Data is assumed to be in Mysql initially. 
1. Copy the given csv files from local to hdfs
2. Creation of Mysql Tables.
3. Sqoop export of data from HDFS to Mysql.
4. Delete the data from hdfs post export, Now data resides in Mysql.

Step2. Sqoop Import
Bring the data from Mysql tables to HDFS. 

Step3. Create Hive External Tables on top of data in HDFS.

Step4. Create Optimized External tables in Hive

Step5. Load data to the optimized hive tables from normal hive tables.

Step6. Inner Join two tables in Hive and get a consolidated table.

Step 7: Analysis 
Do the required inference as mentioned in the problemstatement,run queries and see theresults.
