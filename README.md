# Automated-CSV-to-PostgreSQL-Data-Pipeline-Using-n8n
This project automates the process of loading CSV data received through email into a PostgreSQL database using n8n workflow automation. 
Traditionally, users manually download CSV files from emails, validate the data, and import it into a database. This process is time-consuming and prone to human errors.
This solution eliminates manual effort by automatically monitoring incoming emails, extracting CSV attachments, transforming the data into a structured format, and loading it into PostgreSQL.

# Business Problem
Organizations often receive periodic data files (daily, weekly, or monthly) via email.
Common challenges include:
•	Manual downloading of CSV files
•	Repetitive data import tasks
•	Data entry mistakes
•	Delayed reporting and analytics
•	Lack of automation in data ingestion
This project addresses these challenges by implementing an automated end-to-end ETL workflow using n8n.

# Solution Architecture
The workflow performs the following operations:
1.	Monitor incoming emails.
2.	Detect email attachments.
3.	Validate CSV files.
4.	Parse CSV content.
5.	Transform CSV records into structured JSON format.
6.	Insert records into PostgreSQL database.
7.	Log execution results.
8.	Complete the workflow automatically without user intervention.

# Architecture Diagram
<img width="1113" height="465" alt="Workflow" src="https://github.com/user-attachments/assets/d3868eb5-930f-4f82-ade1-e607fd2becd2" />

# Technologies Used
n8n	Workflow  --> Automation Platform
Gmail --> Email Monitoring
CSV Parser -->	Data Extraction
PostgreSQL -->	Data Storage
JSON Transformation -->	Data Processing
ETL Workflow -->	Automated Data Ingestion

# Workflow Implementation
# Step 1: Email Monitoring
The workflow continuously monitors a Gmail inbox for new incoming emails.
Objective:
•	Detect new emails automatically.
•	Capture email metadata and attachments

# Step 2: Retrieve Email Attachments
When a new email arrives, the workflow extracts:
•	Email Subject
•	Sender Information
•	Email Body
•	Attached Files
Objective:
•	Access all email content required for processing

# Step 3: Validate CSV File
The workflow checks whether the attachment is a CSV file.
Validation Rules:
•	File extension must be .csv
•	File should not be empty
•	File structure should match expected format
Objective:
•	Prevent invalid files from entering the database.

# Step 4: Parse CSV Data
The CSV file is converted into structured JSON records.

Objective:
•	Transform raw CSV data into a format suitable for database insertion.

# Step 5: Data Mapping
The workflow maps CSV columns to PostgreSQL table columns.
Example:
CSV Column	Database Column
id	id
name	name
sales	sales

Objective:
•	Ensure proper alignment between source and target structures.

# Step 6: Load Data into PostgreSQL
The transformed records are inserted into the PostgreSQL table.
Database Operation:
•	Connect to PostgreSQL
•	Insert records
•	Commit transaction
Objective:
•	Persist incoming data automatically.

# Step 7: Workflow Execution Validation
After loading data:
•	Verify inserted records
•	Check workflow execution logs
•	Monitor success/failure status
Objective:
•	Ensure data integrity and reliability.

# Key Features
•	Fully automated workflow
•	No manual CSV imports
•	Real-time email monitoring
•	Automatic data validation
•	PostgreSQL integration
•	Scalable ETL process
•	Reduced operational effort
•	Improved data accuracy

# Business Benefits
Efficiency --> Eliminates manual file processing and database imports.
Accuracy --> Reduces human errors during data loading.
Scalability --> Can process recurring files automatically without additional effort.
Reliability --> Provides a repeatable and standardized data ingestion process.

# Results
•	Automated CSV ingestion from email to PostgreSQL.
•	Reduced manual intervention.
•	Faster data availability for reporting and analytics.
•	Improved operational efficiency and data quality.


















