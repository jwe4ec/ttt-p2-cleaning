# ttt-p2-cleaning

TODO: Document that latest centralized Phase II cleaning is now on [track-to-treat](https://github.com/isaacahuvia/track-to-treat) repo.





This repository contains code for centralized data cleaning for Phase II of Project TRACK to TREAT. The repo is linked to this project on the Open Science Framework (OSF): [https://osf.io/yjv72/](https://osf.io/yjv72/).

## Table of Contents

- [Project Overview](#project-overview)
- [Data](#data)
- [Code](#code)
- [Other Documentation](#other-documentation)
- [TODOs](#todos)

## Project Overview

Phase II of Project TRACK to TREAT (TTT) aims to use parameters from network models estimated from ecological momentary assessment (EMA) data to predict treatment response in depressed adolescents. Phase II consisted of an observational part (21 days of EMA with 5 pings per day) followed by an intervention part (i.e., random assignment to one of three single-session interventions [SSIs]: behavioral activation, growth mindset, or active control) completed within 2 weeks later. Qualtrics measures were given at baseline (pre-EMA); immediately pre- and post-SSI; and at 3, 6, 12, 18, and 24 months after post-SSI measures. Random assignment occurred immediately before pre-SSI measures.

Study registration: [https://clinicaltrials.gov/study/NCT04607902](https://clinicaltrials.gov/study/NCT04607902)

## Data Cleaning Overview

Data, initial code, and documentation relevant to centralized data cleaning for Phase II of TTT are stored in the `MSS/Schleider_Lab/jslab/TRACK to TREAT P2` folder on the [FSMResFiles](https://www.feinberg.northwestern.edu/it/services/server-storage-and-data/research-data-storage.html) server at [Northwestern University Feinberg School of Medicine](https://www.feinberg.northwestern.edu/).

The initial LifePak data cleaning code was drafted by [Yama Chang](https://github.com/yamachang), who adapted [Michael Mullarkey](https://github.com/mcmullarkey)'s LifePak data cleaning code from Phase I of TTT. The present repo houses [Jeremy Eberle](https://github.com/jwe4ec) and [Isaac Ahuvia](https://github.com/isaacahuvia)'s completion of data cleaning for Phase II. For centralized data cleaning for Phase I of TTT, see the separate repo [ttt-p1-main-analysis](https://github.com/jwe4ec/ttt-p1-main-analysis).

Lab staff who contributed to Phase II of TTT include current research coordinator [Alyssa Gorkin](https://github.com/alyssagorkin) and former research coordinators Sharon Leong (formerly Chen), Arielle Smith, Laura Jans, and Chantelle Roulston.

## Data

### Raw

#### From Qualtrics

##### Screening Survey

Screening and enrollment are complete.

The `/TRACK to TREAT P2/Data/Qualtrics/Raw` folder contains 1 CSV file copy (see below) of the Phase II screening data obtained from Qualtrics (per the Date Modified file metadata of the original file and the date in the file name, presumably this file was obtained on 8/31/23). The original file is in the `MSS/Schleider_Lab/jslab/Qualtrics Back-Ups/TRACK to TREAT P2/DP5 Phase 2 - Screener` folder.

##### Study Surveys

Qualtrics data collection through the 18-month assessment is complete; collection of 24-month assessment data is ongoing and projected to be complete in November 2025.

Raw ***<ins>interim</ins>*** data at the baseline; pre/post-SSI; and 3-, 6-, 12-, and 18-month assessments are stored in the `/TRACK to TREAT P2/Data/Qualtrics/Raw` folder, which contains (in the `2025.05.06_interim` subfolder) 22 CSV files (see below) dumped from Qualtrics by Alyssa Gorkin on 5/6/25.

#### From LifePak

EMA data collection is complete.

Raw EMA data are stored in the `/TRACK to TREAT P2/Data/LifePak/TRACK_to_T_NIS_Wide20230823_19_49_36/DataReports` folder, which contains 2 CSV files obtained from LifePak (per Date Modified file metadata, presumably on 9/6/23, although the folder and file names include the date 8/23/23). Although other files are in the `/TRACK to TREAT P2/Data/LifePak/` folder, they have earlier dates in their file names and thus do not seem to be used.

### Clean

Output (i.e., `cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) from Yama Chang's initial LifePak cleaning script is in the `/TRACK to TREAT P2/Data Cleaning/old/2024.08.01 From Yama Chang/cleaned_data` folder.

## Code

### Setup and File Relations

The scripts in the `code` folder of this repo import the raw data and clean and deidentify the data, resulting in what we refer to as "intermediately cleaned" files ("intermediate" because additional cleaning will be needed specific to any given analysis).

To run the code, create a parent directory (denoted here as `.`) with the `./data` and `./code` subfolders below. Ensure the working directory is set to this parent directory. This setup ensures the code imports/exports correctly using relative file paths.

Put the raw LifePak data in the `./data/raw/lifepak` subfolder and the raw Qualtrics data in the `./data/raw/qualtrics` subfolder. `ttt_p2_lifepak_cleaning.Rmd` will create the `./data/clean` subfolder, where the scripts will export clean data.

```
.                                # Parent folder (i.e., working directory)
├── data                         # Data subfolders
├── ├── raw
├── ├── ├── lifepak              # 2 CSV files listed below
├── ├── ├── qualtrics            # 19 CSV files listed below
├── ├── (clean)                  # Folder with clean data will be created by "ttt_p2_lifepak_cleaning.Rmd"
└── code                         # Code subfolder
```

### Scripts

#### `ttt_p2_lifepak_cleaning.Rmd`

This script, derived from Yama Chang's initial script `ttt_p2_lifepak_cleaning_07312024.Rmd`, reproduces the output (`cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) of the initial script per `identical(x, y, F, F, F, F)`. To date, the initial script has only been revised slightly to improve reproducibility; for the changes, see the present script's [history](https://github.com/jwe4ec/ttt-p2-cleaning/commits/main/code/ttt_p2_lifepak_cleaning.Rmd).

Inputs the following 2 raw CSV files
```
# "TRACK_to_T_NIS_Wide20230823_19_49_36_1.csv"
# "TRACK_to_T_NIS_Wide20230823_19_49_36_2.csv"
```

Outputs `cleaned_lifepak_ttt_phase_2_YYYY-MM-DD.csv` (where `YYYY-MM-DD` is the system date)

#### TODO: Qualtrics cleaning script

Should input `DP5 Phase 2 - Screener_August 31, 2023_12.08 (Copy).csv`

Should also input the following 22 raw CSV files
```
# "DP5+Phase+2+-+Parent+-+Baseline_May+6,+2025_09.42 _c"
# "DP5+Phase+2+-+Parent+-+Baseline_May+6,+2025_09.42_n"
# "DP5+Phase+2+-+Parent+-+FU+1+-+3M_May+6,+2025_09.44_n"
# "DP5+Phase+2+-+Parent+-+FU+1+-+3M_May+6,+2025_09.45_c"
# "DP5+Phase+2+-+Parent+-+FU+2+-+6M_May+6,+2025_09.46_n"
# "DP5+Phase+2+-+Parent+-+FU+2+-+6M_May+6,+2025_09.47_c"
# "DP5+Phase+2+-+Parent+-+FU+3+-+12M_May+6,+2025_09.48_n"
# "DP5+Phase+2+-+Parent+-+FU+3+-+12M_May+6,+2025_09.49_c"
# "DP5+Phase+2+-+Parent+-+FU+4+-+18M_May+6,+2025_09.50_n"
# "DP5+Phase+2+-+Parent+-+FU+4+-+18M_May+6,+2025_09.51_c"
# "DP5+Phase+2+-+Youth+-+Baseline_May+6,+2025_09.43_c"
# "DP5+Phase+2+-+Youth+-+Baseline_May+6,+2025_09.43_n"
# "DP5+Phase+2+-+Youth+-+FU+1+-+3M_May+6,+2025_09.45_c"
# "DP5+Phase+2+-+Youth+-+FU+1+-+3M_May+6,+2025_09.45_n"
# "DP5+Phase+2+-+Youth+-+FU+2+-+6M_May+6,+2025_09.47_n"
# "DP5+Phase+2+-+Youth+-+FU+2+-+6M_May+6,+2025_09.48_c"
# "DP5+Phase+2+-+Youth+-+FU+3+-+12M_May+6,+2025_09.49_n"
# "DP5+Phase+2+-+Youth+-+FU+3+-+12M_May+6,+2025_09.50_c"
# "DP5+Phase+2+-+Youth+-+FU+4+-+18M_May+6,+2025_09.51_n"
# "DP5+Phase+2+-+Youth+-+FU+4+-+18M_May+6,+2025_09.52_c"
# "DP5+Phase+2+-+Youth+-+Interventions_May+6,+2025_09.56_n"
# "DP5+Phase+2+-+Youth+-+Interventions_May+6,+2025_09.57_c"
```

TODO: Describe output

#### TODO: Deidentification script

TODO: Describe inputs and outputs

## Other Documentation

The following files in the `MSS/Schleider_Lab/jslab/TRACK to TREAT P2` folder are relevant to data cleaning.

### General

- `/TRACK to TREAT P2/Data/README_ttt_p2_data_collection.docx`
- `/TRACK to TREAT P2/LSMH Participant Database Backups` folder
- `/TRACK to TREAT P2/Data Cleaning/README_ttt_p2_data_cleaning.docx`
  - Points to present repo as most recent data cleaning effort

### Qualtrics

- `/TRACK to TREAT P2/Data/Qualtrics/Raw/README_ttt_p2_raw_qualtrics_data.docx`

## TODOs

- TODO: Clean and deidentify Qualtrics data
- TODO: Further clean and deidentify LifePak data if needed
- TODO: Check for data quality (see Exclusion Criteria in [study registration](https://clinicaltrials.gov/study/NCT04607902))
- TODO: Add 24-month Qualtrics data to cleaning pipeline once data collection is complete
- TODO: Put deidentified clean data in `./data/clean` folder on [OSF project](https://osf.io/yjv72/) linked to the present repo