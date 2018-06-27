## Sqoop

​	You can use Sqoop to import data from a relational database management system (RDBMS) such as MySQL or Oracle or a mainframe into the Hadoop Distributed File System (HDFS), transform the data in Hadoop MapReduce, and then export the data back into an RDBMS.其实就是在HDFS和RDBMS之间数据的导入导出。For databases, row-by-row; For mainframe datasets, each mainframe dataset  one by one.

​	格式：text files , binary Avro , SequenceFiles containing serialized record data.

​	Sqoop导出过程：Sqoop’s export process will   1.  read a set of delimited text files from HDFS in parallel,  2. parse them into records, and  3. insert them as new rows in a target database table。

​	Sqoop uses MapReduce to import and export the data,which provides parallel operation as well as fault tolerance.

常用命令以及查看特定命令详细信息

> #### Available commands:

>  codegen            Generate code to interact with database records

> create-hive-table  Import a table definition into Hive

>  eval               Evaluate a SQL statement and display the results

>  export             Export an HDFS directory to a database table

>  help               List available commands

>  import             Import a table from a database to HDFS

>  import-all-tables  Import tables from a database to HDFS

>  import-mainframe   Import datasets from a mainframe server to HDFS

>  job                Work with saved jobs

>  list-databases     List available databases on a server

>  list-tables        List available tables in a database

>  merge              Merge results of incremental imports

>  metastore          Run a standalone Sqoop metastore

>  version            Display version information

> #### See 'sqoop help COMMAND' for information on a specific command.



### 1、检查数据库情况

##### sqoop-list-databases

> sqoop  list-databases  --connect jdbc:mysql://10.20.12.13/telemarket  --username  bi  --password bi@sx##3



> 报错，解决方法：加白名单

> Host '10.20.12.19' is not allowed to connect to this MySQL server

##### sqoop-list-tables

同list-databases





