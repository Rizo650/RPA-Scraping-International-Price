# PlattsConnect Price Scraper - UiPath RPA

This RPA project automates the process of scraping **commodity pricing data** from the **PlattsConnect** website. It filters the data according to defined rules and exports the result as a CSV file to a **shared folder**.

The process is built using **UiPath REFramework** to ensure reliability, logging, and modularity.

---

## Project Description

The automation accesses the PlattsConnect website, performs user login (if needed), navigates to the pricing data section, scrapes relevant data, applies filtering rules (e.g., by product or region), and exports the cleaned dataset to a shared directory in CSV format.

A success email is optionally sent after the process completes.

---

## Key Features

- Automated login and data scraping from PlattsConnect
- Filtering of pricing data based on business rules
- CSV export to shared folder
- Email notification on successful completion
- REFramework-based for robust error handling and modularity

---

## Project Structure

| Folder/File               | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| Main.xaml                 | Main entry point of the automation                          |
| Modular/EmailSuccess.xaml | Sends notification email after successful export            |
| Framework/                | Standard REFramework components                            |
| Data/Config.xlsx          | Stores URLs, credentials, filter parameters, paths, etc.    |
| project.json              | Project metadata and dependencies                           |
| README.md                 | Project documentation                                        |

---

## Process Workflow

1. **Initialization**  
   - Loads settings from `Config.xlsx`  
   - Initializes logs and variables

2. **Access & Scraping**  
   - Navigates to PlattsConnect website  
   - Logs in if needed  
   - Extracts pricing data from a specific section

3. **Filtering**  
   - Applies filtering logic (e.g., by commodity type, currency, location)  
   - Validates that relevant rows are found

4. **Export to CSV**  
   - Saves filtered results to a predefined **shared folder** as `.csv`

5. **Notification**  
   - Sends success email using `EmailSuccess.xaml` (optional/configurable)

---

## How to Run

> Designed for scheduled runs via **UiPath Orchestrator**, but also testable manually.

1. Open project in **UiPath Studio**
2. Update values in `Data/Config.xlsx`:
   - PlattsConnect URL and credentials (if needed)
   - Filtering parameters
   - Shared folder path
   - Email configuration (if used)
3. Run `Main.xaml`
4. Check shared folder for CSV output

---

## Requirements

- UiPath Studio 2022.10+
- Chrome/Edge browser with UiPath extension
- Access to PlattsConnect account and target data
- Network access to the shared folder
- Email SMTP/Outlook setup (for optional success email)

---

## Contact

For inquiries or collaboration:

- **Email:** fadillah650@gmail.com  
- **LinkedIn:** [Enrico Naufal Fadilla](https://linkedin.com/in/enrico-naufal-fadilla-54338a256)
