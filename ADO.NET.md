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
| SQL Server    | <li>Provides data access for Microsoft SQL server.</Ii><br><li>Uses the **System.Data.SqlClient** namespace.</li><br><li>Ex:-SQLServer 2000, 2005, 2008 &Many more versions.</li>                                          |
| OLEDB         | <li>For data sources exposed by using OLEDB.</Ii><br><li>Uses the **==System.Data.OleDb==** namespace.</li><br><li>Ex:-For both relational and non-relational databases. (Oracle, Sql-Server, Excel, raw files, etc).</li> |
| ODBC          | <li>For data sources exposed by using ODBC. </li><br><li>Uses the **==System.Data.Odbc==** namespace.</li>                                                                                                                 |
|               |                                                                                                                                                                                                                            |
