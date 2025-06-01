Shipping Label CSV Parser
==========================
A lightweight Streamlit web app that:
    - Collects sender address info
    - Parses and validates customer data from .csv, .xlsx, or .txt files
    - Allows duplication based on a Copies column
    - Exports two clean CSVs: valid rows and rows with missing data


Features
--------
    - Streamlit interface with form-based sender input
    - Uploads Excel, CSV, or TXT files with customer data
    - Cleans, validates, and highlights incomplete entries
    - Duplicates rows based on editable "Copies" field
    - Exports two CSVs: one clean and one with missing fields (fixable inline)


Requirements
------------
- Python 3.8 or higher must be installed

Install dependencies using pip:

    pip install -r requirements.txt

Minimum required packages (in requirements.txt):
 - streamlit
 - pandas
 - openpyxl



How to Run
----------

1. Clone or download the project folder
2. Open a terminal in the project directory
3. Run the app:

       streamlit run app.py

4. Fill in the Sender Info form
5. Upload a customer file
6. Edit and review parsed rows
7. Download the final cleaned CSVs

File Structure
--------------

    csv_parser_gig/
        app.py                - Main Streamlit app UI
        parse.py              - Core parsing and validation logic
        from_address.json     - Auto-saved sender data
        requirements.txt      - List of required packages

Notes
-----

    - The "Copies" column defaults to 1 and is editable before exporting
    - Any rows with missing required fields are shown in a separate editor
    - Sender info is stored persistently in from_address.json after first run
