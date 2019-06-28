
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

Note that if you click on "Detect Type", it will read source file and populate the schema and you can change data types here.

![15](00-images/ref-dataset-15.png)

<hr>

Select "current partitioning" as shown below - we have a very small set of data - partitioning is an anti-pattern for small data as it degrades performance.

![16](00-images/ref-dataset-16.png)

<hr>


![17](00-images/ref-dataset-17.png)

<hr>

![21](00-images/ref-dataset-21.png)

<hr>

To preview, we have to have **debug** on.  This spinds up a Dtaabricks runtime to execute the Dataflow for developing/debugging.

![20](00-images/ref-dataset-20.png)

<hr>

You should see this dialog show up. Give it 5-10 minutes.

![18](00-images/ref-dataset-18.png)

<hr>

![19](00-images/ref-dataset-19.png)

<hr>images

#### 4a.2.4. Lets look at the sink for Payment type

![22](00-images/ref-dataset-22.png)

<hr>

![23](00-images/ref-dataset-23.png)

<hr>

![24](00-images/ref-dataset-24.png)

<hr>

![25](00-images/ref-dataset-25.png)

<hr>

### 4a.3. If you have extra time, review the rest of the sub-flows

They are essentially identical in configuration.
Otherwise, skip to the next section below.

### 4a.4. Lets test the dataflow through a pipeline

![25](00-images/ref-dataset-25.png)

<hr>

![26](00-images/ref-dataset-26.png)

<hr>

![27](00-images/ref-dataset-27.png)

<hr>

![28](00-images/ref-dataset-28.png)

<hr>

![29](00-images/ref-dataset-29.png)

<hr>

![31](00-images/ref-dataset-31.png)

<hr>

![32](00-images/ref-dataset-32.png)

<hr>

![33](00-images/ref-dataset-33.png)

<hr>

![34](00-images/ref-dataset-34.png)

<hr>

![35](00-images/ref-dataset-35.png)

<hr>

![36](00-images/ref-dataset-36.png)

<hr>

![37](00-images/ref-dataset-37.png)

<hr>

![38](00-images/ref-dataset-38.png)

<hr>

![39](00-images/ref-dataset-39.png)

<hr>

![40](00-images/ref-dataset-40.png)

<hr>

![41](00-images/ref-dataset-41.png)

<hr>

