# Simple Browser Forensic Scripts

This project explores digital forensics by extracting browsing data from Firefox databases.
It currently consists of two planned scripts focused on analyzing Firefox’s places.sqlite 
and formhistory.sqlite files.

## Scripts

# 1. Places.sqlite Analyzer

This script reads Firefox’s places.sqlite database to extract:

+ URLs
+ Page titles
+ Visit counts
+ Timestamps of the last visit

The extracted data is saved into a CSV file for easy analysis.

# 2. Form History Analyzer (planned)

This script will analyze Firefox’s form history (formhistory.sqlite) and is planned for future implementation.

## Usage

### 1. Preparing the database files

Copy the following files from your Firefox profile directory into the browser_profile folder in this project.
**For the Places.sqlite Analyzer:**

+ places.sqlite
+ places.sqlite-wal
+ places.sqlite-shm

**For the Form History Analyzer (when available):**

+ formhistory.sqlite
+ formhistory.sqlite-wal
+ formhistory.sqlite-shm
These files must be copied **while Firefox is closed**, or the data may be locked or incomplete.

### 2. Running the scripts

```bash
python3 places_analyzer.py
or
python3 from_analyzer.py
```
