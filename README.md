# MySQL to Microsoft SQL Server data migration Using the Wizard

### Basic Differences Between MySQL and SQL
There are many ways to migrate a MySQL Database to SQL Server, one of them can be using SQL Server Migration Assistant (SSMA). However, in this section, we will explain how to manually transfer data from MySQL to Microsoft SQL Server through SQL Server Management Studio's Import Data feature.

### Why do we need to migrate MySQL database to MS SQL Server?
There may be several reasons for someone to consider transferring a MySQL database to Microsoft SQL Server:
1. An organization's specific requirements or preferences may demand the use of SQL Server rather than MySQL. This could be due to compatibility with other Microsoft products or requests from stakeholders.
2. SQL Server may outperform MySQL in terms of performance and scalability for some workloads. Depending on the application and its requirements, SQL Server may be more suitable for handling large amounts of data or high concurrency scenarios.
3. SQL Server and MySQL provide different sets of features and capabilities. If an application requires extensive analysis, integration with other Microsoft products, or enterprise-level functionality, migration to SQL Server may be necessary.
4. SQL Server provides a robust ecosystem with Microsoft support, which may appeal to companies that rely heavily on Microsoft technologies or are looking for a full support alternative.
5. In businesses with varied database setups, there may be an effort to standardize on a single database platform to facilitate manageability, maintenance and cost savings. In many situations, moving MySQL databases to SQL Server may be part of a larger consolidation effort. (Source : [Link](https://www-linkedin-com.translate.goog/pulse/how-migrate-mysql-database-sql-server-get-best-solution-nfmqc?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=id&_x_tr_pto=sge#:~:text=Metode%20Profesional%20Khusus%20untuk%20Mentransfer,para%20ahli%20berikut%20untuk%20migrasi:))

### Transfer MySQL Data to SQL Server Using Import/Export Utility:
Berikut ini adalah langkah-langkah yang digunakan untuk Memigrasikan Database dari MySQL ke SQL Server dengan metode Impor/Ekspor:
Step 1: Download and Install the MySQL ODBC Connector. 

Pertama, unduh dan instal konektor ODBC. Tersedia di [Click here](https://downloads.mysql.com/archives/c-odbc/)

Step 2: Open ODBC Data Source Administrator and Browse MySQL ODBC Driver.

Now, open your ODBC Data source administrator from the Control Panel>>Administative tools. On the system DSN tab click Add, Browse the “MySQL ODBC driver” and press the finish button.

![image alt](https://github.com/Biancaninna/Data-Migration-Using-Wizard/blob/5f57e691398b85cd8d16215b74512ce572021fe2/Images/CREATE%20ODBC%20CONNECTOR%20FOR%20MYSQL%20.png) 

Step 3: Input MySQL Server Connection Details.

Input your MySQL Server connection details, check it, and click OK.

![image alt](https://github.com/Biancaninna/Data-Migration-Using-Wizard/blob/5f57e691398b85cd8d16215b74512ce572021fe2/Images/ODBC%20MYSQL.png) 

Step 4: Perform the same steps for the SQL Server connection

On the system DSN tab click Add, Browse the “SQL Server” and press the finish button.

![image alt](https://github.com/Biancaninna/MySQL-to-SQL-Server-Data-Migration/blob/830c44bb8215c0ae28c21bf2c043ba4d12c429fd/Images/CREATE%20ODBC%20CONNECTOR%20FOR%20SQL%20SERVER%20.png) 


Step 5: Input SQL Server Connection Details.

Input your SQL Server connection details, check it, and click OK.

![image alt](https://github.com/Biancaninna/MySQL-to-SQL-Server-Data-Migration/blob/830c44bb8215c0ae28c21bf2c043ba4d12c429fd/Images/ODBC%20SQL%20SERVER.png) 

Step 5: Launch the SQL Server Management Studio

Next, Launch the SQL server management studio.

Step 6: Create a New Database 

Click on NEXT, create a new Database, or use an existing database.

Step 7: Click Import Data to Launch the SQL Server Import and Export Software.

Right-click on the destination Database and select task then click Import Data to launch the Data Server Import and Export Wizard.

![image alt](https://github.com/Biancaninna/MySQL-to-SQL-Server-Data-Migration/blob/830c44bb8215c0ae28c21bf2c043ba4d12c429fd/Images/IMPORT%20DATA%20FROM%20MYSQL%20TO%20SQL%20SERVER.png) 

Step 8: Choose the .NET Data provider for ODBC 

Choose the .NET Data provider for ODBC as a Data source and specify the DSN created before.

![image alt](https://github.com/Biancaninna/MySQL-to-SQL-Server-Data-Migration/blob/830c44bb8215c0ae28c21bf2c043ba4d12c429fd/Images/MYSQL%20DATA%20SOURCE.png) 

Step 9: Enter the piece of information from your SQL Server Database

Now users have to choose the SQL server native client 10 as a destination, enter the details of their SQL Server Database, and then click Next.

Step 10: Copy the Data from one or more tables

Then, select Copy Data from one or more tables or view and click Next.

Step 11: Choose the Source and Destination Tables

Further, select the source and destination tables. Users can enable the Identity insert using the edit mapping option.

Step 12: Execution of the Package

At last, execute the package and save it for the future if needed.










