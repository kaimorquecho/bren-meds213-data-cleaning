DATA & FILE OVERVIEW

FILES

``` text
bren-meds213-data-cleaning/
├── bren-meds213-data-cleaning.Rproj
├── README.md
├── fixed_snow_cover_README.md
├── eds213_data_cleaning_assignment.qmd
├── data/
│   ├── raw/
│   │   ├── 01_ASDN_readme.txt
│   │   ├── ASDN_Daily_species.csv
│   │   └── ASDN_Snow_survey.csv
│   └── processed/
│       ├── all_cover_fixed_KaijuMorquecho.csv
│       └── species_presence.csv
```

-   eds_213_data_cleaning_assignment.qmd — Contains code to clean the ASDN_Snow_survey dataset

-   `data` folder contains two subfolders

    -   `raw` — Contains original datasets that haven't been cleaned.
    -   `processed` — Contains clean files, including cleaned ASDN_Snow_survey.csv as 'all_cover_fixed_KaijuMorquecho.csv'

-   Refer to link provided under 'SHARING/ ACCESS INFORMATION' for information on access to the rest of the data collected for the ASDN project and its metadata

DATA-SPECIFIC INFORMATION FOR:

`data/processed/all_cover_fixed_KaijuMorquecho.csv`

1.  Number of variables: 11

2.  Number of cases/rows: 42830

3.  Variable list:

    | Variable | Description | Unit / Format |
    |----|----|----|
    | Site | Four-letter code of site where data were collected | Character |
    | Year | Year of observation | Integer (YYYY) |
    | Date | Date of observation | Date (YYYY-MM-DD) |
    | Plot | Name of the study plot | Character |
    | Location | Name of dedicated snow-survey location (if applicable) | Character |
    | Snow_cover | Percent of plot covered in snow (including slush) | Numeric (0–100), inferred if needed |
    | Water_cover | Percent of plot covered in water | Numeric (0–100), inferred if needed |
    | Land_cover | Percent of plot with exposed land | Numeric (0–100), inferred if needed |
    | Total_cover | Total of all cover percentages | Numeric (0–100), recomputed |
    | Observer | Name of surveyor | Character |
    | Notes | Additional comments or context | Character |

4.  Missing data codes:

    | Code  | Meaning                             |
    |-------|-------------------------------------|
    | NA    | Value not available or inferred     |
    | "."   | Originally used for missing; now NA |
    | "-"   | Originally used for missing; now NA |
    | "n/a" | Originally used for missing; now NA |
    | "unk" | Originally used for missing; now NA |

5.  Specialized formats or other abbreviations used:

    -   `Date` is stored in `YYYY-MM-DD` format
    -   All `*_cover` columns are numeric percentages between 0 - 100. Values \> 100 or \< 0 were flagged and removed (set to NA)
        -   `Snow_cover`, `Water_cover`, and `Land_cover` were inferred if missing whenever three of the four cover variables were available for estimation.

SHARING/ACCESS INFORMATION

Snow_cover data was obtained from the EDS 213 course's repository, which utilized ASDN project data.

[Bren EDS 213 Class Github Repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning.git)

Complete, original datasets for the Artic Shorebird Demographics Network project are hosted by the NFS Artic Data Center

[Arctic Data Center](https://arcticdata.io/catalog/view/doi%3A10.18739%2FA2CD5M)

The ASDN authors request that potential users of the data first contact the relevant data author(s) or send general inquiries to Emily Weiser ([Emily.L.Weiser\@gmail.com](mailto:Emily.L.Weiser@gmail.com){.email}).
