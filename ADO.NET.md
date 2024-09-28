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
	- Command
	- Data Reader
- Connection
	- It is a first component Of **ADO.NET.**
	- It provide connectivity to **Data Source.**
	- It establishes a connection to a specific data source. 
	- Connection object helps in accessing and manipulating a database.
	- The base class for all Connection objects is the DbConnection class.
	- Methods of Connection Object
		- **Open():** this method opens connection using information provided by connection string. 
		- **Close():** this method closes already opened connection
	- Properties Of Connection Object

| Properties         | Description                                                                                                                                                      |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ConnectionString   | Connection String is collection of name/value pairs separated by semicolon which gives information of data source with which connection needs to be established. |
| DataSource         | It specifies name of computer and SQL server instance with which connection is required.                                                                         |
| IntegratedSecurity | It specifies that connection will be established using windows authentication of SQL Server username/password.                                                   |
| Initial Catalog    | It specifies name of database with which connection is required.                                                                                                 |
| UserID             | It specifies username to connect with database.                                                                                                                  |
| Password           | It specifies password to connect with database.                                                                                                                  |
	