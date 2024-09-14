# Uber Data Analytics | Data Engineering GCP Project

## Introduction

This project focuses on performing data analytics on Uber trip data using various tools and technologies on Google Cloud Platform (GCP). The project demonstrates the use of GCP Storage, Python, Compute Instances, Mage Data Pipeline Tool, BigQuery, and Looker Studio for an end-to-end data engineering and analytics workflow.

## Architecture

The architecture of the project is as follows:

![Architecture diagramming](https://github.com/user-attachments/assets/b094f62d-572a-4f84-99ba-cf42d3f81371)


## Technology Used

- **Programming Language**: Python
- **Google Cloud Platform (GCP)**:
  - Google Cloud Storage
  - Compute Instance
  - BigQuery
  - Looker Studio
- **Modern Data Pipeline Tool**: [Mage](https://www.mage.ai/)


## Dataset Used

The dataset used in this project is the TLC Trip Record Data.

- **Website**: [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

## Data Model

![Data Model](https://github.com/user-attachments/assets/b68bbf7d-de70-40ec-a8de-922555e617c3)



## Getting Started

### Prerequisites

- A Google Cloud Platform account. 
- Access to Google Cloud Storage, BigQuery, and Looker Studio.
- Mage.ai account for data pipeline management.

## Project Steps

### 1. **Setup Google Cloud Platform (GCP)**

   - **Create a Google Cloud Project:**
     - Go to the [Google Cloud Console](https://console.cloud.google.com/).
     - Create a new project or select an existing one.

   - **Enable Required APIs:**
     - Enable the following APIs:
       - Google Cloud Storage
       - BigQuery API
       - Compute Engine API

   - **Create Service Accounts:**
     - Create a service account with roles for accessing Google Cloud Storage, BigQuery, and Compute Engine.
     - Download the JSON key file for authentication.

<img width="919" alt="Google cloud" src="https://github.com/user-attachments/assets/b86b8dd5-da48-4f6c-bc23-8eb58b3d01da">


### 2. **Prepare the Environment**

   - **Install Google Cloud SDK:**
     - Follow the [installation instructions](https://cloud.google.com/sdk/docs/install) for the Google Cloud SDK.

   - **Authenticate Google Cloud SDK:**
     - Authenticate using the service account key:
       ```bash
       gcloud auth activate-service-account --key-file=path-to-your-service-account-key.json
       ```

   - **Install Python and Required Libraries:**
     - Ensure Python is installed.
     - Install required libraries using `pip`:
       ```bash
       pip install google-cloud-storage google-cloud-bigquery pandas
       ```

### 3. **Upload Data to Google Cloud Storage**

   - **Create a Storage Bucket:**
     - Go to the [Google Cloud Storage Console](https://console.cloud.google.com/storage).
     - Create a new bucket to store your raw data.

   - **Upload Dataset:**
     - Upload your dataset (`uber_data.csv`) to the created bucket.

### 4. **Setup Mage Data Pipeline**

   - **Create a Mage.ai Account:**
     - Sign up for an account at [Mage.ai](https://www.mage.ai/).

   - **Configure Data Pipeline:**

     --------------------------------------------------------<img width="136" alt="mage pipeline" src="https://github.com/user-attachments/assets/3fe03858-ebdc-48f7-b2fa-9a95a7d6fc9e">------------------------------------------------------------


     <img width="908" alt="mage-ui" src="https://github.com/user-attachments/assets/f7647750-f153-4f16-94d5-aa00fd9d29d5">


     - Create a new project in Mage.ai.
     - Set up a data pipeline to:
       - Load raw data from Google Cloud Storage.
       - Transform data as required.
       - Load the transformed data into Google BigQuery.
     - Follow Mage.ai’s documentation for detailed configuration.

### 5. **Data Analysis in BigQuery**

   - **Create a BigQuery Dataset:**
     - Go to the [BigQuery Console](https://console.cloud.google.com/bigquery).
     - Create a new dataset to store your analyzed data.

   - **Load Data into BigQuery:**
     - Verify that Mage.ai has successfully loaded the data into BigQuery.

   - **Run SQL Queries:**
     - Use BigQuery’s SQL editor to perform data analysis. Example queries could include aggregations, filtering, and joining datasets.

### 6. **Data Visualization with Looker Studio**

   - **Create a Looker Studio Account:**
     - Sign up for [Looker Studio](https://lookerstudio.google.com/) if you don’t already have an account.

   - **Connect to BigQuery:**
     - Create a new report in Looker Studio and connect it to your BigQuery dataset.

   - **Design Dashboards:**
     - Use Looker Studio to create visualizations and dashboards based on your BigQuery analysis.

## Conclusion

This project provided a comprehensive experience in building robust and scalable data engineering solutions using Google Cloud Platform (GCP) and modern data tools. By integrating Google Cloud Storage, BigQuery, Mage.ai, and Looker Studio, I was able to handle and analyze large datasets effectively.

Thank you for exploring this project. If you have any questions or suggestions, please feel free to reach out or contribute to the repository.



