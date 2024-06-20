# MariaDB
Code concerning the MariaDB database





Recommendation: 
    1. Blake’s Recommendation for Date Format:  YYYYMMDD
    2. Recommendation to change the name of the Sample_ID column to make sure that it’s consistent across the data table. 
    3. Recommendation to change the data file name:
        a. For qPCR datafile, each file should start with “qpcr_*” and follow with what’s necessary to distinguish that file from other qpcr files. End with date (yyyymmdd) if needed.
        b. For taxonomical profile, genome coverage and metadata, if the pool number is critical, start with that and add unique labels to separate it from other files.
            i.  i.e: 
                1. p1647_genome_coverage_general_report.all_samples.100windows.mean_cov”
                2. p1647_taxonomical_profile_general_report.coverm.combined.tax
Data Definitions:

Metadata Folder:
This folder contains data from Baylor. The prefix “P-XXXX” in the file names indicate different batch numbers (pool number).

Columns: 
Folder
Column Names
Data Type
Description
­Comments
Metadata
Sample_ID
String, TEXT
These are the labels of the bottle samples from WWTP sites, BARCODE


Site
String, TEXT



City
String, TEXT



Date

Date 
Format: YYYY-MM-DD
YYYY-MM-DD


Flow
Real Number, Float, Decimal



PoolID­
String, TEXT
Group of sample libraries loaded together on a sequencer





qPCR Folder:
Folder
Column Names
Data Type
Description
Comments
qPCR
LocationAbbr
String, TEXT

Abbreviation for WW treatment plant


CMMR_Barcode
String, TEXT




Target
String, TEXT




Ct
Real Number, 
Double



copiesperml
Real Number, Float, Decimal



SampleName
String, TEXT




date_of_collection
Date 
Format: m/dd/yyyy










Genome_coverage Folder:
Folder
Column Names
Data Type
Description
Comments
Genome_coverage
Sample_ID
String, TEXT
BARCODE.POOLID


accession
String, TEXT




Start_base

Integer



End_base

Integer



Mean_depth
Real Number, Float, Decimal






Site_coding Folder:

Folder
Column Names
Data Type
Description
Comments
Site_coding
Name
String, TEXT



Code
String, TEXT






Taxonomical_profiles Folder:

Folder
Column Names
Data Type
Description
Comments
taxonomical_profiles
accession
String, TEXT



reference_length
Real Number, 
Integer





covered_base
Real Number, 
Integer




reads_aligned
Real Number, 
Integer




mean_coverage
Real Number, 
double




RPKMF
Real Number, 
double




sequence_name
String, TEXT



taxid
String, TEXT



kingdom
String, TEXT



phylum
String, TEXT



class_var
String, TEXT



order_var
String, TEXT



family
String, TEXT



genus
String, TEXT



species
String, TEXT



subspecies
String, TEXT



strain
String, TEXT



sample_ID
String, TEXT
BARCODE.POOLID
The PoolID field has been removed

total_filtered_reads_in_sample
Real Number, 
double











WWTP_Location Folder:
Folder
Column Names
Data Type
Description
Comments
Wwtp_location
State
String, TEXT



County
String, TEXT




City
String, TEXT



WWTP
String, TEXT



lat
Real Number, Float, Decimal



lon
Real Number, Float, Decimal



county_centroid_lat
Real Number, Float, Decimal



county_centroid_lon
Real Number, Float, Decimal



city_centroid_lat
Real Number, Float, Decimal



city_centroid_lon
Real Number, Float, Decimal





