# Exclusivity Detections Monthly Process


Exclusivity detections are tested on a monthly basis by finding Wayfair products under exclusivity agreements with our suppliers on Amazon. Our current process samples the PartNumbers we test into two parts:

  - **WPP: Wayfair Preferred Partners** - A sample of SKUs that are exclusive under WPP agreements with suppliers
  - **FSB: Flagship Brands** - All PartNumbers that have active exclusivity agreements within any of our Flagship Brands

Once we have our sample, we coordinate with our Matching team to look for these products on Amazon and log all detections and violations for our reporting.

# Scripts Overview
**Python (jupyter lab)**
  - Detections Monthly Process - Goes through the sampling, compiling parts to send for Matching, logging detections,and generating the reports in Excel format.
  - MoM - Formats reports so that they can be looked at in Tableau with month-over-month metrics
  - Violations Tableau Dashboard - Creates a junk table for our suppliers dashboard to read from

**SQL**
 - **Detections Sampling**
     > Exclusivity Detections sampling - part 1.sql
     > Exclusivity Detections sampling - part 2 (FSB).sql
     > Exclusivity Detections sampling - part 3 (WPP).sql
     > Get Exclusivity Detections.sql 
 - **Reporting**
    > SRM report.sql
    > Marketing Categories report.sql
    > Average GRS report.sql
    > ED stats.sql

**Junk tables (SQLMERCHANDISING)**
 - all_exclusive_products_mmyy
 - ED_sample_mmyy
 - exclusive_detection_log_mmyy
 - ED_buckets_mmyy
 
**Manual steps required monthly:**
  - Sending list of ManufacturerPartIDs to Matching team
  - Formatting Excel output
  - Draft email on Google doc and visuals on Tableau

### To-dos

 - Add price competitiveness metric to violations
 - Get a tech review
 - Automate more of the process



