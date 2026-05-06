# ttt-p2-cleaning

The repo is linked to this project on the Open Science Framework (OSF): [https://osf.io/yjv72/](https://osf.io/yjv72/).

## Data Cleaning Overview

The initial LifePak data cleaning code was drafted by [Yama Chang](https://github.com/yamachang), who adapted [Michael Mullarkey](https://github.com/mcmullarkey)'s LifePak data cleaning code from Phase I of TTT.

Lab staff who contributed to Phase II of TTT include current research coordinator [Alyssa Gorkin](https://github.com/alyssagorkin) and former research coordinators Sharon Leong (formerly Chen), Arielle Smith, Laura Jans, and Chantelle Roulston.

## Data

### Raw

#### From LifePak

EMA data collection is complete.

Raw EMA data are stored in the `/TRACK to TREAT P2/Data/LifePak/TRACK_to_T_NIS_Wide20230823_19_49_36/DataReports` folder, which contains 2 CSV files obtained from LifePak (per Date Modified file metadata, presumably on 9/6/23, although the folder and file names include the date 8/23/23). Although other files are in the `/TRACK to TREAT P2/Data/LifePak/` folder, they have earlier dates in their file names and thus do not seem to be used.

### Clean

Output (i.e., `cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) from Yama Chang's initial LifePak cleaning script is in the `/TRACK to TREAT P2/Data Cleaning/old/2024.08.01 From Yama Chang/cleaned_data` folder.

## Code

### Scripts

#### `ttt_p2_lifepak_cleaning.Rmd`

This script, derived from Yama Chang's initial script `ttt_p2_lifepak_cleaning_07312024.Rmd`, reproduces the output (`cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) of the initial script per `identical(x, y, F, F, F, F)`. To date, the initial script has only been revised slightly to improve reproducibility; for the changes, see the present script's [history](https://github.com/jwe4ec/ttt-p2-cleaning/commits/main/code/ttt_p2_lifepak_cleaning.Rmd).

Inputs the following 2 raw CSV files
```
# "TRACK_to_T_NIS_Wide20230823_19_49_36_1.csv"
# "TRACK_to_T_NIS_Wide20230823_19_49_36_2.csv"
```

Outputs `cleaned_lifepak_ttt_phase_2_YYYY-MM-DD.csv` (where `YYYY-MM-DD` is the system date)

## Other Documentation

The following files in the `MSS/Schleider_Lab/jslab/TRACK to TREAT P2` folder are relevant to data cleaning.

### General

- `/TRACK to TREAT P2/Data/README_ttt_p2_data_collection.docx`
- `/TRACK to TREAT P2/LSMH Participant Database Backups` folder
- `/TRACK to TREAT P2/Data Cleaning/README_ttt_p2_data_cleaning.docx`
  - Points to present repo as most recent data cleaning effort

### Qualtrics

- `/TRACK to TREAT P2/Data/Qualtrics/Raw/README_ttt_p2_raw_qualtrics_data.docx`