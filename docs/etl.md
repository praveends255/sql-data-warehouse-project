# ETL Concepts and Methods

This document outlines various ETL (Extract, Transform, Load) concepts,
techniques, and methods with their definitions and explanations.

  -----------------------------------------------------------------------------
  **Stage**       **Technique / Method / Concept** **Definition / Explanation**
  --------------- -------------------------------- ----------------------------
  **Extract**     Pull Extraction                  Data is actively pulled from
                                                   source systems by the ETL
                                                   tool or script.

                  Push Extraction                  The source system pushes
                                                   data directly to the target
                                                   system or ETL pipeline.

                  Full Extraction                  Extracts the entire dataset
                                                   from the source every time.

                  Incremental Extraction           Extracts only new or changed
                                                   records since the last
                                                   extraction.

                  Manual Data Extraction           Data collected manually,
                                                   e.g., downloading reports or
                                                   files.

                  Database Querying                Using SQL or other queries
                                                   to pull data from a
                                                   database.

                  File Parsing                     Reading and processing
                                                   structured or
                                                   semi-structured files (CSV,
                                                   JSON, XML, etc.).

                  API Calls                        Fetching data
                                                   programmatically from APIs.

                  Web Scraping                     Extracting data from web
                                                   pages when APIs aren't
                                                   available.

                  Event-based Streaming            Real-time data extraction
                                                   triggered by system events.

                  Change Data Capture (CDC)        Capturing changes (inserts,
                                                   updates, deletes) from
                                                   source databases.

                  Extraction Methods / Extract     Broad terms describing how
                  Types / Extract Techniques       data is pulled from sources.

  **Transform**   Batch Processing                 Processing data in bulk at
                                                   scheduled intervals.

                  Stream Processing                Processing continuous data
                                                   streams in near real-time.

                  Data Enrichment                  Adding external or
                                                   contextual data to enhance
                                                   existing records.

                  Data Normalization &             Converting data into a
                  Standardization                  consistent and standardized
                                                   format.

                  Data Integration                 Combining data from multiple
                                                   sources into one unified
                                                   dataset.

                  Business Rules & Logic           Applying domain-specific
                                                   rules to transform or
                                                   validate data.

                  Derived Columns                  Creating new calculated
                                                   fields based on existing
                                                   data.

                  Data Aggregations                Summarizing data (e.g.,
                                                   totals, averages).

                  Remove Duplicates                Identifying and removing
                                                   duplicate records.

                  Data Cleansing                   Correcting or removing
                                                   inaccurate, incomplete, or
                                                   irrelevant data.

                  Outlier Detection                Identifying values that
                                                   deviate significantly from
                                                   the norm.

                  Data Filtering                   Selecting only the necessary
                                                   records or fields.

                  Data Type Casting                Converting data into the
                                                   correct data types.

                  Handling Missing Data            Imputing or dropping records
                                                   with null or missing values.

                  Handling Invalid/Unwanted Data   Cleaning or transforming bad
                                                   inputs.

                  Handling Unwanted Spaces         Trimming unnecessary
                                                   whitespace in text fields.

                  Slowly Changing Dimensions (SCD) Managing dimension table
                                                   changes in a data warehouse
                                                   over time.

                  SCD 0 -- No Historization        Overwriting dimension data
                                                   with no history kept.

                  SCD 1 -- Overwrite               Replacing old dimension data
                                                   with new without tracking
                                                   history.

                  SCD 2 -- Historization           Keeping full history of
                                                   dimension data changes.

  **Load**        Load Methods                     Various ways of loading
                                                   transformed data into the
                                                   target system.

                  Full Load                        Loading the entire dataset
                                                   into the target system.

                  Incremental Load                 Loading only new or changed
                                                   records since the last load.

                  Drop-Create-Insert               Dropping the table,
                                                   recreating it, then
                                                   inserting data.

                  Truncate-Insert                  Truncating (emptying) the
                                                   table and then inserting new
                                                   data.

                  Upsert (Merge)                   Inserting new records and
                                                   updating existing ones.

                  Append                           Adding new data without
                                                   altering existing records.

                  Merge                            Combining datasets during
                                                   the load phase.
  -----------------------------------------------------------------------------
