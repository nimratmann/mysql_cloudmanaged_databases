# mysql_cloudmanaged_databases
MySQL on Cloud Platforms - Azure and GCP

# Azure Configuration Setup Process
Resource Type: Azure Database for MySql; Deployment option: Flexible, Tier: Burstable Compute: B1S [$6.21 p/month] or B1MS [$12.41 p/month]

1. In the Azure portal, click on the "+ Create a resource" button on the left-hand menu.
2. In Azure services, select 'Azure Database for MySQL servers' and then hit '+create'
4. Choose 'Flexible server'
5. In Basics:
      - Select 'Azure for Students' as the Subscription.
      - Name the server and choose 'for development or hobby projects' as the workload.
      - For compute + storage, choose 'Burstable, B1ms.'
      - Create an admin username and password.
6. In Networking: Under firewall rules: select '+add 0.0.0.0' (public IP address)
7. Azure will validate your configuration to check for any errors or conflicts.
8. Click the "Create" button to deploy the MySQL instance

Setting Up MySQL Workbench Connection:
1. Open MySQL Workbench.
2. Create a new connection.
3. Name it for Azure.
4. Set the Hostname to the Server Name provided in the Azure instance.
5. Use Port 3306.
6. Ensure the Username matches the Azure server admin login.
7. Securely store the password.
8. Click 'Test Connection' to confirm connectivity.
9. Click 'OK' to create the connection.




# GCP Configuration Setup Process
Resource Type: MySQL; DB-standard-1 (vCPU 1, RAM 3.75 GB) 10gb storage No backups [$9.37 month]DB-standard-1 (vCPU 1, RAM 3.75 GB)

1. Sign in to your GCP account and navigate to the project (under the AHI_GCP folder).
2. In the left navigation menu, click on "SQL."
3. Choose "Create instance" and select "MySQL" as the database engine.
4. Provide an instance ID and set a password.
5. To lower costs:
      - Change the Cloud SQL edition to "Enterprise."
      - Under "Preset," select "Sandbox."
      - Set the zonal availability to "Single Zone."
      - Click "Show configuration options."
6. In "Machine Configuration," choose "Shared Core" and select "1 vCPU, 0.614 GB."
7. In "Storage," select "10 GB."
8. Configuring network options:
      - In "Connections," click "Add a Network."
      - Name the connection, e.g., "Allow All."
      - Set the network to "0.0.0.0/0."
      - Click "Done."
9. click "Create Instance" to finish

Setting Up MySQL Workbench Connection:
1. Open MySQL Workbench.
2. Create a new connection.
3. Name the connection to indicate it's for GCP.
4. Set the Hostname to the Public IP address provided for the GCP instance.
5. Use Port 3306.
6. For the password, select "Store in Vault" and enter the instance password.
7. Click "Test Connection" to ensure the connection works.
8. Click "OK" to create the connection.


# Experience Using MySQL Workbench
Using MySQL Workbench I was successfully able to create and display databases, design tables, and generate two separate entity-relationship diagrams (ERDs) using both GCP and Azure. Screenshots of both the GCP and Azure database configurations are located in their respective folders.

# Challenges Using MySQL Workbench
One error I initially faced was creating the ERD. I rewatched the lecture from last week and followed the following steps to overcome this challenge:

1. Go to the "Database" menu and select "Reverse Engineer." This will open the Reverse Engineering Wizard.
3. In the wizard, you'll be prompted to select a connection. Choose the database connection you previously established.
4. Click "Next" to start the process. MySQL Workbench will fetch the structure and objects of the selected database.
5. You can select which schema objects you want to include in your ERD. Typically, you'll want to include tables, views, and routines. Click "Next" to proceed.
6. Specify how your ERD should be named and where it should be placed within MySQL Workbench. Click "Next" to continue.
7. Review your settings and click "Execute" to generate the ERD. MySQL Workbench will analyze the database and create the visual ERD representation.
8.  After completion, your ERD will appear in MySQL Workbench. You can customize it by rearranging tables, adjusting layouts, and adding annotations as needed.





