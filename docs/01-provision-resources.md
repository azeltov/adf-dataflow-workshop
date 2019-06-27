# Module 1: Provision resources for the workshop

You will need to provision the following resources:<br>
1.  Resource Group
2.  Storage Account (HNS enabled - ADLS gen2)
3.  Azure SQL Database
4.  Azure Data Factory

### 1.0. Provision a resource group in your Azure subscription

![RG-1](00-images/00-rg-1.png)

<hr>

![RG-2](00-images/00-rg-2.png)

### 2.0. Provision a storage account (v2, hot tier, with HNS enabled) in your resource group

2.0.1. Go to the resource group and click on "Add"<br>

![SA-1](00-images/01-storage-1.png)

<hr>

2.0.2. Look for storage account<br>

![SA-2](00-images/01-storage-2.png)

<hr>

2.0.3. Click create<br>

![SA-3](00-images/01-storage-3.png)

<hr>

2.0.4. Fill in the details<br>

![SA-4](00-images/01-storage-4.png)

<hr>

2.0.5. Enable HNS<br>

![SA-5](00-images/01-storage-5.png)

<hr>

2.0.6. Validate and create<br>

![SA-6](00-images/01-storage-6.png)

<hr>

2.0.7.  Storage account should be visible in your resource group

![SA-7](00-images/01-storage-7.png)

### 3.0. Provision a SQl database

3.0.1. Go to the resource group and click on "Add", then search for "SQL database"<br>

![RDBMS-1](00-images/02-rdbms-1.png)

<hr>

3.0.2. Click create<br>

![RDBMS-2](00-images/02-rdbms-2.png)

<hr>

3.0.3. Create a new logical database server<br>

![RDBMS-2](00-images/02-rdbms-3.png)

<hr>

3.0.4. Enter server details<br>

![RDBMS-2](00-images/02-rdbms-4.png)

<hr>

3.0.2. Click create<br>

![RDBMS-2](00-images/02-rdbms-5.png)

<hr>

3.0.2. Click create<br>

![RDBMS-2](00-images/02-rdbms-6.png)

<hr>

3.0.2. Click create<br>

![RDBMS-2](00-images/02-rdbms-7.png)

<hr>

### 4.0. Provision a Data Factory

4.0.1. Go to the resource group and click on "Add"<br>

![ADF-1](00-images/03-adf-1.png)

<hr>

4.0.2. Search for "data Factory"<br>

![ADF-2](00-images/03-adf-2.png)

<hr>

4.0.3. Enter details<br>

![ADF-3](00-images/03-adf-3.png)

<hr>

4.0.4. Click create<br>

![ADF-4](00-images/03-adf-4.png)

<hr>

4.0.5. You shoudl see the service in your resource group<br>

![ADF-5](00-images/03-adf-5.png)

<hr>

