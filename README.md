IAB Architectural Firm Data Cleaning Process
This document outlines the step-by-step procedure to clean and structure architectural firm data for further use in analysis and reporting, including generating insights via Looker dashboards. The process involves extraction, pattern identification, data validation, and cleaning.

Step 1: Data Extraction
Extract PDFs: Merge PDF files using I Love PDF.
Check Copy Capability: Test if text can be copied from the PDF.
Copy and Paste: If successful, copy the text to Notepad, then paste the Notepad data into Google Sheets.

Step 2: Identifying Patterns & Initial Cleanup
Remove Unnecessary Data: Clean out irrelevant items.
Apply Filters: Use CTRL + T to convert data into a table and filter:
Identify specific text patterns like IAB REGISTERED ARCHITECTURAL CONSULTANTS (Valid up to 31st December, 2020) and In Alphabetical Order.
Highlight these patterns in yellow for easier identification.
Use filtering to identify rows with values (1-8) in column B and mark them with a different color.
Review and delete any rows marked in yellow (unnecessary data).

Step 3: Processing Page 2 Data
Filter Specific Patterns: Identify and highlight rows marked as IAB-RP.
Assign Row Numbers: Ensure each row has a sequential identifier.

Step 4: Calculating Distances in Data
Sum Values in Column C: Filter data by yellow-marked rows, then calculate the sum of a series (e.g., B3 + B4 + ... + B10).
Remove Specific Rows: Use filtering to remove rows marked with IAB-KP and ensure designated rows (e.g., B2, B11, B20) are empty.

Step 5: Pattern Creation
Structure Data Fields:
IAB ID
Company Name
Address
Email
Website
Name of Proprietor
Designation
Full-Time Status
Total Employees
Ensure that the sum of rows meets expected values. For instance, the sum of rows should equal 8 to confirm consistency across the dataset.

Step 6: Build Database in Column F
Auto-Populate Fields: Use formulas (e.g., F2 = A2, F3 = A3) to populate columns from the cleaned dataset into the structured database.

Step 7: Duplicate and Refine Data
Create New Sheet: Duplicate the current sheet as Cleaning Data-2.
Refine Columns: Remove unnecessary columns such as A, B, C, and D.

Step 8: Address Cleaning
Find and Replace: Clean the Office Address and Email ID columns by using CTRL + F to find and replace blanks as needed.

Step 9: Attribute Designation Cleanup
Merge Columns: Move values from Name of Proprietor into the Designation column, then delete the Name of Proprietor column.
Remove Redundant Columns: Delete the Full-Time Status column after transferring relevant data.

Step 10: Company Name and Establishment Year Separation
Create Establish Year Column: Separate the establishment year from the company name and ensure proper structuring.

Step 12: Add Google Maps Data
Geocode Address: Use the office address to look up coordinates on Google Maps, then add the results to the dataset.

Step 13: Separate Contact Information
Clean Contact Data: Organize the Contact Number column by removing unnecessary data and pasting values into the main dataset.

Step 14: Split Proprietor Names
Proprietor Name Column: Create a new column for the name of the proprietor and transfer values accordingly.

Step 15-18: Further Cleanup and Structuring
Website Column Cleanup: Ensure the website data is accurate and properly formatted.
Full-Time Data Cleanup: Validate and clean up data for full-time employees.
Thana and Postcode Separation: Extract these details from the office address column and organize them into separate columns.

Step 19: Final Data Review
Pivot Table for Review: Use a pivot table to fix any remaining inconsistencies, such as converting text numbers into numerical values, removing duplicates, and filling missing values.
Visualization & Reporting
The cleaned data can now be visualized using the Looker dashboard for comprehensive reporting and analysis.

https://lookerstudio.google.com/reporting/bc4da135-715e-4e91-9826-be7a1c76745c
