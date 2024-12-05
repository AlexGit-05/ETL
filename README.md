# ETL Repository for Data Extraction, Transformation, and Loading

## Introduction to ETL

**ETL** stands for **Extraction, Transformation, and Loading**. It is a process used in data integration that involves extracting data from various sources, transforming it into a usable format, and then loading it into a destination system for analysis or reporting. ETL is a crucial part of data workflows in fields such as data warehousing, business intelligence, and data analytics.

### The ETL Process

1. **Extraction**:
   The first step is to extract data from source systems. This could involve reading data from files (e.g., CSV, Excel, PDF), databases, APIs, or web scraping. The goal is to gather raw data, no matter its structure, that can be further processed.

2. **Transformation**:
   Once the data is extracted, it often needs to be cleaned, organized, and transformed to make it useful. This step can involve several tasks:
   - Handling missing or incorrect data
   - Filtering and removing unnecessary records
   - Aggregating, grouping, or summarizing data
   - Changing formats or data types to fit the required schema
   - Merging data from multiple sources

   The transformation step ensures that the data is in a structured format suitable for analysis or reporting.

3. **Loading**:
   After transformation, the data is loaded into a destination system, which could be a data warehouse, a database, or even a file (CSV, Excel, etc.). The loaded data is now ready to be analyzed, reported on, or further processed for insights.

This repository automates the ETL process by extracting data from PDF documents and a website, transforming it into a cleaner format, and providing the data in a structured form for analysis.

---

## Overview

This repository contains a series of scripts designed for **Extracting**, **Transforming**, and **Loading** (ETL) data. The repository includes Python and R scripts for extracting data from PDF tables, transforming it into a cleaner format, and scraping data from a rental house website.

- **Data Extraction**: Python notebook for extracting data from tables in PDF documents.
- **Manager history**: R script for transforming the data into a more structured and clean format.
- **Webscrapping BuyRentKenya**: Python notebook that scrapes data on rental houses from the BuyRentKenya website.

## Key Features

### 📄 **Data Extraction (Python Notebook)**

- Extracts tables from PDF documents.
- Uses libraries such as `PyPDF2` and `Tabula` to extract structured data from PDFs.
- Outputs data in a usable format (e.g., CSV, JSON).

### 🔄 **Manager history (R Script)**

- Cleans and transforms the extracted data into a more structured format by filtering the data frame for the given FundID, then splitting the manager history into separate rows, then filtering the managers who were employed on the given date, and finally counting the number of rows.
- Uses the `dplyr`, `tidyr`, and `readr` R packages.

### 🏠 **Webscrapping BuyRentKenya (Python Notebook)**

- Scrapes data on rental houses from the BuyRentKenya website.
- Collects data such as house prices, locations, and property details.
- Outputs the data in a structured format like CSV or JSON for analysis.

## Technologies & Libraries Used

- **Python**:
   - `PyPDF2`, `Tabula`, `Pandas`, `BeautifulSoup`, `requests`, and `Selenium` for scraping and PDF table extraction.
- **R**:
   - `dplyr`, `tidyr`, `readr` for transforming and cleaning data.

## Installation

To use the scripts, you'll need to install the following dependencies:

### Python Dependencies:
```bash
pip install PyPDF2 tabula-py pandas beautifulsoup4 requests selenium
