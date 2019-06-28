
# Module 4a: Load reference data from staging to raw zone into Paruet

In this module - we will review all the artifacts we imported for reference data in a detailed fashion and learn from them.<br>

The data engineering work done in this module is -<br>
Read reference data in CSV format in the staging zone, transform to a more optimal format (space and query efficient), parquet to the raw zone.<br>

## 4a.1: Dataset review

### 4a.1.1. Lets review our storage account setup

There are 4 file sstems - one for each information zone.<br>
staging<br>
raw<br>
curated<br>
consumption<br>

We will read from staging and persist to parquet in the raw infomation zone.

![1](00-images/ref-dataset-1.png)

<hr>

### 4a.1.2. Lets review the data in the staging directory

Lets look at the data in the staging zone.

![2](00-images/ref-dataset-2.png)

<hr>

Peek a little deeper.

![3](00-images/ref-dataset-3.png)

<hr>


### 4a.1.3. Create datasets

This is a foundational task.  In your case, the dataset configuration artifacts have been imported, so you dont really have to import anything.  Notice how they are organized into directories/folders?  Simplies organization and should you ever need to delete - can do easily at a directory level.<br><br>

For each entity, we have one staging dataset and one raw dataset - consider these metadata.<br>
Lets take one dataset and review both the raw and staging configuration.

#### 4a.1.3.1. Payment type - staging

![4](00-images/ref-dataset-4.png)

<hr>

![5](00-images/ref-dataset-5.png)

<hr>

![5a](00-images/ref-dataset-5a.png)

<hr>

![6](00-images/ref-dataset-6.png)

<hr>


#### 4a.1.3.2. Payment type - raw


![7](00-images/ref-dataset-7.png)

<hr>


![8](00-images/ref-dataset-8.png)

<hr>


## 4a.2: Dataflow review

#### 4a.2.1. Navigate to the Load Reference Data Dataflow

Expand the Data Flow section, then expand the "01-LoadFromStaging" directory and click on "Load-Reference-Data"

![11](00-images/ref-dataset-11.png)

<hr>

#### 4a.2.2. Note that there are 6 reference datasets and you should see a sub-flow for each

These will run in parallel.

![12](00-images/ref-dataset-12.png)

<hr>

We will zone in on Payment Type and learn.

#### 4a.2.3. Lets look at the source  for Payment type

![13](00-images/ref-dataset-13.png)

<hr>

![14](00-images/ref-dataset-14.png)

<hr>

![15](00-images/ref-dataset-15.png)

<hr>

![16](00-images/ref-dataset-16.png)

<hr>


![17](00-images/ref-dataset-17.png)

<hr>

![18](00-images/ref-dataset-18.png)

<hr>
