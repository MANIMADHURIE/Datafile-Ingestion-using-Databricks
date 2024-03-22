# Datafile-Ingestion-using-Databricks

## AGENDA:
The major goal of this project is to simplify the process of transforming numerous files and sending them to the locations that were specified for them. To accomplish this goal, Azure Data Factory is used to manage the processing of files as they are moved from the input container in Azure Data Lake to the output container in the same location. To guarantee that everything is in its place, the folder structure is always updated so that it corresponds with the IDs of the file formats.

Data bricks are used to directly access files and conduct data transformations, which ultimately results in the data being converted into a format that is organized and simple to comprehend. To arrange CSV, Excel, and JSON files, code written in PySpark is used. In addition to that, the project includes procedures for checking null and nan values, which have the effect of reducing unnecessary values.

To further refine the data, several transformations, including union, duplication check, identifier merging, and JSON value extraction, are developed. Views are constructed on top of the data frames after the phases of file purification and processing have been finished. These views provide quick access as well as the ability to do analysis.

## TOOLS USED:

Following tools were employed in the project, and they formed the foundation of the project's data management and processing infrastructure, ensuring efficient and reliable data movement, transformation, and analysis.
- Azure Data Lake
- Azure Data Factory
- Databricks
  
## ETL PROCESS:

Ensures that data is extracted, transformed, and loaded efficiently, and that data quality is maintained throughout the process.
- Extraction: extracts data from multiple files stored in Azure Data Lake.
- Transformation: Extracted data is transformed using PySpark code to process CSV, excel, and JSON files into a structured format, and applies transformations including union, detecting duplication, merging 
  headers, and parsing JSON contents.
- Loading: The transformed data is then loaded to the output container of Azure Data Lake into specific folders of file format.


![image](https://github.com/MANIMADHURIE/Datafile-Ingestion-using-Databricks/assets/37103568/94a6be30-6860-4fed-a096-ea35ec1ed926)

## DATA INGESTION WITH DATABRICKS:

Using PySpark code, CSV, Excel, and JSON files are processed and transformed into a structured format. The project utilizes various data transformation techniques such as union, duplicate check, identifier merge, and JSON value extraction, which can be easily implemented using Databricks. Databricks also supports null and nan check processing, which is used to eliminate redundant values and improve the quality of the processed data.

## DATA INGESTION PIPELINE:

In our project, we focused on developing an **Azure Data Factory** (ADF) pipeline with a specific activity known as "**ForEach**" to handle and manage multiple files efficiently. This pipeline was designed to handle large-scale data processing tasks and automate the loading of the extracted files into a designated location.

The "ForEach" activity within the ADF pipeline played a crucial role in iterating through each file within the Data Lake and applying the required transformations based on the defined input data requirements. This dynamic and iterative approach allowed us to handle an arbitrary number of files, ensuring the scalability and flexibility of the data processing pipeline.

By triggering the pipeline/activity multiple times, we were able to systematically transform and load each file in the Data Lake, ensuring that all files were processed according to the specified data requirements. This approach enabled us to streamline the data integration process and optimize the overall efficiency of the ETL workflow.

![image](https://github.com/MANIMADHURIE/Datafile-Ingestion-using-Databricks/assets/37103568/ff98189d-7b92-496e-9f90-4ed452d8a867)

## DATA INGESTION PROCESS:

The project utilizes PySpark code in conjunction with Databricks to transform CSV, Excel, and JSON files into a structured format, enabling sophisticated data processing and analytics. Through operations like union and duplicate checks, redundant data records are identified and managed efficiently. Additionally, identifiers consolidate operations facilitate data integration based on shared identifiers. JSON value extraction enables targeted analysis, while Databricks' capabilities ensure the removal of redundant or invalid values, enhancing overall data quality and integrity. By combining PySpark, Databricks, and these transformation techniques, the project achieves efficient and accurate data processing, resulting in structured and reliable datasets ready for analysis.

![image](https://github.com/MANIMADHURIE/Datafile-Ingestion-using-Databricks/assets/37103568/c24223e0-4cec-4158-906d-2d6c2ea39cba)

**Input Container:**

![image](https://github.com/MANIMADHURIE/Datafile-Ingestion-using-Databricks/assets/37103568/00939ea0-eb07-4cff-836e-24e222155800)

**Output Container:**

![image](https://github.com/MANIMADHURIE/Datafile-Ingestion-using-Databricks/assets/37103568/f5f177b0-1113-483e-b776-84f6a58a85ba)

## RESULTS AND CONCLUSION:

We have successfully extracted data from multiple files and loaded them into their final destinations after processing and transforming the data. This was achieved using PySpark code to process CSV, Excel, and JSON files into a structured format that is amenable to further analysis. In addition, we implemented null and naan check processing to eliminate redundant values and ensure that the processed data is of high quality. Various data transformation techniques such as union, checking duplicates, merging headers, and parsing JSON values were also built into the project to improve the efficiency and accuracy of the data processing. Furthermore, we created views on top of the processed data frames to enable easy access and analysis of the data. These views provide a convenient and intuitive interface for data exploration and visualization, which is crucial for making informed decisions based on the processed data. Overall, the project has successfully achieved its objective of transforming and processing multiple files into a clean and structured format that is suitable for downstream analysis.

## FUTURE SCOPE:

- The current project work can be improved by parameterizing the Spark code to make it more customizable for parsing and processing multiple sheets within an Excel file. This would allow for the easy modification of the code to accommodate changes in file formats or data processing requirements.
- In the future, We can route the output files in the form of delta files to improve the performance of data processing and minimize the storage footprint of the processed data.	
- Expand the work to different file formats like ZIP, Fixed width, XML.










