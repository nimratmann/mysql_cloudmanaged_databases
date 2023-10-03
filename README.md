# mysql_cloudmanaged_databases
MySQL on Cloud Platforms - Azure and GCP

# Azure Configuration Setup Process
Resource Type: Azure Database for MySql; Deployment option: Flexible, Tier: Burstable Compute: B1S [$6.21 p/month] or B1MS [$12.41 p/month]

1. 
2. 
3. 
4.
5.




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
