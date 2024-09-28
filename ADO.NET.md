### **ADO.NET Intro**
- ADO stands for **ActiveX Data Objects.**
- It's Database technology of .NET Framework used to connect ***application system and database server.***
- It's a part of **.NET Framework.**
- It's consists of **set of classes used to handle data access.**
- It use **XML** to **store and transfer data** among **application,** which is not only **industry standard** but also provide fast access of data for **desktop  and distributed application.** 
#### The ADO.NET architecture has two main parts:
1. Data(Managed) Provider (Connected objects or Connection oriented objects)
2. DataSet (Disconnected objects or connectionless objects)
![[Pasted image 20240928101713.png]]
![[Pasted image 20240928101615.png]]

#### Data Providers
| Data Provider | Description                                                                                                                                                                                                                |
| :------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SQL Server    | <li>Provides data access for Microsoft SQL server.</Ii><br><li>Uses the **==System.Data.SqlClient==** namespace.</li><br><li>Ex:-SQLServer 2000, 2005, 2008 &Many more versions.</li>                                      |
| OLEDB         | <li>For data sources exposed by using OLEDB.</Ii><br><li>Uses the **==System.Data.OleDb==** namespace.</li><br><li>Ex:-For both relational and non-relational databases. (Oracle, Sql-Server, Excel, raw files, etc).</li> |
| ODBC          | <li>For data sources exposed by using ODBC. </li><br><li>Uses the **==System.Data.Odbc==** namespace.</li><br><li>EX:- Only for relational databases (Sql Server, Oracle etc).</li>                                        |
| Oracle        | <li>For Oracle Data Sources.</li><br><li>Uses the **==System.Data.OracleClient==** namespace.</li><br><li>EX:- Oracle 8, 8i, 9i & Many more versions.</li>                                                                 |
- It is a component that has been explicitly designed for **data manipulation**.
- It is used for connecting to a database, executing commands, and retrieving results.
- The Data Provider has core objects like:
	- Connection
		- It is a first component Of **ADO.NET.**
		- It provide connectivity to **Data Source.**
		- It establishes a connection to a specific data source. 
		- Connection object helps in accessing and manipulating a database.
		- The base class for all Connection objects is the DbConnection class.
		- ![[Pasted image 20240928195940.png]]
	- Command
	- Data Reader