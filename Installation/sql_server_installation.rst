SQl Sever Installation Steps
++++++++++++++++++++++++++++

Download SQL Server Installer
=============================
https://www.microsoft.com/en-in/sql-server/sql-server-downloads


Download SSMS
=============
https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16

While SSMS downloading, run the Installer application

Installation Steps
==================



1. Select Installation type ``Custom``
--------------------------------------
.. image:: /Images/SQL-Installation/install_type_custom.png

2. Create ``D:/DATABASE`` and Browse to that folder; Click ``Install``
----------------------------------------------------------------------
.. image:: /Images/SQL-Installation/database_select.png

**SQL Server installation center** will open up

3. Select ``New SQL Server standalone installation or Add features to an existing installation``
-------------------------------------------------------------------------------------------------------
.. image:: /Images/SQL-Installation/installation_center.png

#. installation
#. Accept licence terms
#. x Global Rules
#. x Microsoft update
#. x product updates
#. x Install Setup files
#. x install rules
#. Uncheck Azure Extension
#. Feature Selection - Check Local DB, Browse 'DATABASE' folder for 'Instance root directory'
#. Instance Configuration - Click Default instance 'MSSQLSERVER'
#. Server configuration - SQL Server Browser > Automatic()
#. If no user add current user
#. installation complete
#. close installer
#. Run SSMS Setup application
#. Set location to DATABASE
#. Click Restart
#. Open SQL Server Management Studio