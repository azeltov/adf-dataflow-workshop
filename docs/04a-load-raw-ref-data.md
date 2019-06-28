
# Module 4a: Load reference data from staging to raw zone into Paruet

In this module - we will review all the artifacts we imported for reference data in a detailed fashion.<br>

The data engineering work done in this module is -<br>
Load CSV data in staging zone as parquet to the raw zone.<br>

### 4.1. Lets review our storage account setup

There are 4 file sstems - one for each information zone.<br>
staging<br>
raw<br>
curated<br>
consumption<br>

We will read from staging and persist to parquet in the raw infomation zone.

![1](00-images/ref-dataset-1.png)

<hr>

![2](00-images/ref-dataset-2.png)

<hr>


![3](00-images/ref-dataset-3.png)

<hr>


### 4.2. Lets review the data in the staging directory


### 4.3. Create datasets

This is a foundational task.  In your case, the dataset configuration artifacts have been imported, so you dont really have to import anything.  Notice how they are organized into directories/folders?  Simplies organization and should you ever need to delete - can do easily at a directory level.<br><br>

For each entity, we have one staging dataset and one raw dataset - consider these metadata.<br>
Lets take one dataset and review both the raw and staging configuration.

#### 4.3.1. Payment type - staging



#### 4.3.3. Payment type - raw
