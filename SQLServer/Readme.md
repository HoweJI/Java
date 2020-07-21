# SQLServer
Learning progress

1.install SQL Server

  i am using the developer version. also you could select express,but experss version may not support the full function(max memory:1410MB, max 10G).
  after install the SQL Server developer, you'd better install the SSMS(SQL Server Management Studio) to use the GUI manage the database.

    a.search the database name from D:\Microsoft SQL Server\MSSQL15.MSSQLSERVER\MSSQL\Log\ERRORLOG
    please search "Server name" the latest ERRORLOG file.
    everytime SQL Server start, it will create a new ERRORLOG file.
    Tips: you may could not open the LOG folder first time, please remember to change the permission.

    b.create a new SQL user in the "security", after that add the user into your database security/user
    Tips: remember to modify the database security from only windows authentication to windows and SQL Server in the database properties.