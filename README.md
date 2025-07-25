# Simple Browser Forensic Scripts

This project explores digital forensics by extracting browsing data from Firefox databases.
It currently consists of two planned scripts focused on analyzing Firefox’s places.sqlite 
and formhistory.sqlite files.

# Scripts

## 1. Places.sqlite Analyzer

This script reads Firefox’s places.sqlite database to extract:

+ URLs - The visited web address
+ Page Title - The title of the visited page
+ Visit Count - How often the page was visited
+ Last Visit Date - Timestamp of the last visit

The extracted data is saved into a CSV file for easy analysis.

## 2. Form History Analyzer

This script reads Firefox's formhistory.sqlite database to extract:

+ Fieldname - The name of the form field where text was entered
+ Value - The text that was typed into the field
+ Times Used - How often this entry was used
+ First Used - Timestap of the first usage
+ Last Used - Timestamp of the last usage

The extracted data is saved into a CSV file for easy analysis.

### Usage

#### 1. Preparing the database files

Copy the following files from your Firefox profile directory into the _**browser_profile**_ folder in this project.
**For the Places.sqlite Analyzer:**

+ places.sqlite
+ places.sqlite-wal
+ places.sqlite-shm

**For the Form History Analyzer (when available):**

+ formhistory.sqlite
+ formhistory.sqlite-wal
+ formhistory.sqlite-shm
These files must be copied **while Firefox is closed**, or the data may be locked or incomplete.

#### 2. Running the scripts

```bash
python3 places_analyzer.py
or
python3 from_analyzer.py
```
