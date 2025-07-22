# Pentaho-Mergeflow
ETL pipeline built using Pentaho Data Integration (PDI) to merge, clean, and transform data from Excel, CSV, text, and ZIP files. Includes fuzzy matching, value mapping, filtering, and calculated fields for unified data output.

This ETL project demonstrates a complete pipeline built with Pentaho Data Integration (PDI / Kettle) to integrate, clean, and transform data from multiple formats and sources. The goal is to unify heterogeneous datasets, apply cleaning and transformation logic, and prepare a final enriched dataset ready for analytics or storage.

🚀 Objective
To extract data from different input sources (Excel, CSV, ZIP, Text), clean and normalize values, remove duplicates, apply fuzzy matching, and derive new fields using transformation logic — all through a visual ETL workflow in Pentaho.

<img width="2160" height="1301" alt="Screenshot 2025-07-22 113221" src="https://github.com/user-attachments/assets/b13f4bb4-42dc-4098-8ad9-780f8176d994" />




🔧 Tools & Technologies
Pentaho Data Integration (PDI / Kettle)

Excel, CSV, Text, and ZIP file readers

Transformation steps: Sorting, Merging, Filtering, Value Mapping, String Replacement, Fuzzy Matching

Data enrichment and calculated field generation

🛠️ What This Project Does
✅ Data Input & Preparation
Sources Ingested:

Microsoft Excel files

CSV files

ZIP-compressed input

Plain text files

Manual Data Grid (for testing/demo values)

Preprocessing:

All input streams are passed through individual Sort Rows steps to ensure correct ordering before merging.

🔗 Data Consolidation
Sorted Merge:

Combines all sorted datasets into a unified stream.

Removes duplicates using the Unique Rows step.

🔄 Data Transformation
Value Mapper:

Standardizes field values (e.g., mapping category codes to labels).

Replace in String:

Cleans inconsistent text patterns across fields (e.g., replacing special characters or whitespace anomalies).

🔍 Fuzzy Matching
Fuzzy Match:

Matches records with a secondary Excel source to perform approximate lookups.

Useful when dealing with inconsistently spelled entries.

Select Values:

Refines the schema by selecting only required fields for further processing.

🧹 Data Cleaning & Filtering
Second Round of Replace in String & Select Values:

Applies additional cleanup logic and schema refinement.

Filter Rows:

Filters records based on logic (e.g., null checks, flags, or thresholds).

Calculator:

Derives new fields based on existing ones (e.g., conditional values, math operations).

📦 Final Output Assembly
Sorted Merge 2:

Combines clean records again for any final joining logic.

Select Values 4:

Finalizes the output schema, ready for downstream loading or export.

<img width="2160" height="1313" alt="Screenshot 2025-07-22 174038" src="https://github.com/user-attachments/assets/2ad32638-ebc5-456b-bb9a-4ff06a7c2b22" />

📌 Key Highlights
Visual drag-and-drop workflow with no coding.

Dynamic integration of five different input types.

Extensive use of Pentaho transformations including:

Fuzzy logic

String replacements

Custom calculated fields

Advanced row filtering

Ready to integrate with databases or BI dashboards.

📂 Included Files
CustomerData_West_Arizono.csv

CustomerData_West_Colorado.csv

CustomerData_West_Washington.csv

CustomerData_West_Others.csv

CustomerData_East.xlsx

customerdummy.csv

transformation.ktr (Pentaho Transformation file)

🔧 What the Pipeline Does
Data Ingestion:

Reads from 4 West region .csv files (Arizona, Colorado, Washington, Others)

Reads East region data from CustomerData_East.xlsx

Ingests an additional dummy dataset (customerdummy.csv)

Loads a hardcoded grid for test/mock data

Data Sorting & Merging:

Applies Sort Rows on each input stream

Combines all sources using Sorted Merge

Removes duplicates using Unique Rows

Value Mapping & Cleaning:

Standardizes inconsistent field values using Value Mapper

Applies multiple Replace in String steps to clean raw text

Fuzzy Matching:

Matches records between datasets using Fuzzy Match to handle variations in names/entries

Filtering & Calculations:

Filters unwanted or incomplete rows

Derives new fields using Calculator (for example, conditional logic or math ops)

Final Output:

Produces a clean, deduplicated, and enriched dataset

Schema is refined through multiple Select Values stages for consistent structure
