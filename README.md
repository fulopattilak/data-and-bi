# Report documentation with DAX Studio

## Summary and usage

Here, you can find a DAX script that I wrote for report documentation purposes: <br>
[DAX SCRIPT]()

1. Install DAX Studio
    * I currently use '[MikeCarlo/BusinessOps](https://github.com/MikeCarlo/BusinessOps/releases)' to manage my PBI extensions.
3. Open DAX Studio and connect to the report to be documented
4. Copy the DAX SCRIPT to the editor in DAX Studio
5. Change the Output to 'Static Excel'
6. Press the Run button (play icon) in DAX Studio to run the code
7. Save the Excel file that was generated

The script uses information functions to return the following in a tabular form:
* Tables loaded in the reprot
    * Tables loaded via Power Query or calculated with DAX
* Tables in Power Query that are not loaded
* Columns in loaded tables
    * Calculated columns too
* DAX measures
* Relationships between tables
* RLS roles and their rules
* Incremental load rules for tables

The first column in the output is BLANK. It holds the respective table's name.

## Justification

A newly created report often requires some sort of documentation. This can take many forms. Be it a page inside the report, a document created separately or a page in a wiki.

I tend to create documentation outside of a report, on a platform where access via a link can be provided.
* Maintaining a document that is not dependent on the PBIX / PBIP file is easier and does not require developer competencies
* PBI Desktop offers limited and clunky options for documentation
* If the documentation is inside the report, it cannot be shared without granting access to the report
* It is harder to move, copy and reproduce documentation that is inside a report

## Background
I tried many 3rd party solutions before. None provided a simple output for documentation. Something that can be easily copied to a document and is easy to reproduce at later stages / releases of a development cycle.
* The output of this query can be copied as a table and be inserted to any documentation.

I wanted something that does not require much manual work and uses tools that a PBI dev already has.
* The script uses Power BI Desktop, DAX Studio and Excel only.

I needed something that does not require PBI premium capacity. So I had to avoid XMLA endpoints and Rest API.
* The script runs locally.

I searched for a solution that is not using loopholes and exploits
* The script is based on officially supported DAX information functions, so hopefully it is rather future proof.

## DEV notes
There was one update in the past that changed some of the names of the output values of the information functions. This also meant that I had to change the code to accomodate the new column names. This might happen in the future.

  

