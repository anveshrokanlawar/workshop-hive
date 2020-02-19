# Practice with Hive
- 44517 - 01
- 02 - Practice with Hive

<br/>

### Team Members:
1. Rajender Ravi Varma Devulapally
1. Leela Krishna Kosaraju
1. Anvesh Rokanlawar
1. Akhil Kumar Reddy Busireddy

<br/>

### Link to this Repo:

https://github.com/anveshrokanlawar/workshop-hive

<br/>


Before getting started to work on hive get the setup ready by installing the flavoured linux OS OVM file from cloudera.

Then check whether Java, Hadoop and Hive are installed on the Virtual machine.

Below are the commands that are need to be executed to verify them

java -version
hadoop version
hive --version

If interested installing the desired set of linux flavour then make sure to download the Java, hadoop and hive and then set the local path and Environmental variables.

Below link can be used as a reference to complete the setup.

https://www.tutorialspoint.com/hive/hive_installation.htm

## Working with hive

Initially get the data on which you are interested to work on performing hive mapreduce operations. Then consider the type of data available then look for the delimiters like '\t',',' etc.. in th data to store them into a table. 

- Command to create a table.

    create table demo (store String,category String,cost double,paymenttype String)ROW FORMAT DELIMITED FIELDS TERMINATED BY ',' STORED AS TEXTFILE;
    
- Loading of data into table.

    LOAD DATA LOCAL INPATH '/home/cloudera/Desktop/d.txt' OVERWRITE INTO TABLE demo;
    
- verifying the successful loading of data into the table.

    select * from demo;
    
- Performing the aggregate function using hive on the loaded data.

    select category, max(cost) from demo group by category;


