# ttt-p2-lifepak-cleaning-old

This repo contains the old centralized LifePak data cleaning code for Phase 2 of Project Track to Treat (TTT). **For the new LifePak and Qualtrics data cleaning code for Phases 1-2 of TTT, see the [jwe4ec/track-to-treat](https://github.com/jwe4ec/track-to-treat) repo.**

The old code was drafted by [Yama Chang](https://github.com/yamachang), who adapted [Michael Mullarkey](https://github.com/mcmullarkey)'s old LifePak data cleaning code from Phase 1 of TTT (see [jwe4ec/ttt-p1-cleaning-old](https://github.com/jwe4ec/ttt-p1-cleaning-old)). The Phase 2 Qualtrics data had not been cleaned, which in part motivated the new approach to data cleaning (encompassing both LifePak and Qualtrics data).

Lab staff who contributed to Phase 2 of TTT include current research coordinator [Alyssa Gorkin](https://github.com/alyssagorkin) and former research coordinators Sharon Leong (formerly Chen), Arielle Smith, Laura Jans, and Chantelle Roulston.

The data, old code, and documentation for Phase 2 are stored in `jslab/TRACK to TREAT P2/` on the FSMResFiles server.

## Data

### Raw LifePak

Raw EMA data are stored in `/TRACK to TREAT P2/Data/LifePak/TRACK_to_T_NIS_Wide20230823_19_49_36/DataReports/`, which contains 2 CSV files obtained from LifePak (per Date Modified file metadata, presumably on 9/6/2023, although the folder and file names include the date 8/23/2023). Although other files are in `/TRACK to TREAT P2/Data/LifePak/`, they have earlier dates in their file names and thus do not seem to be used.

### Clean

Output (i.e., `cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) from Yama Chang's initial LifePak cleaning script is in `/TRACK to TREAT P2/Data Cleaning/old/2024.08.01 From Yama Chang/cleaned_data/`.

## Code

### `ttt_p2_lifepak_cleaning.Rmd`

This script, derived from Yama Chang's initial script `ttt_p2_lifepak_cleaning_07312024.Rmd`, reproduces the output (`cleaned_lifepak_ttt_phase_2_2024-08-01.csv`) of the initial script per `identical(x, y, F, F, F, F)`. To date, the initial script has only been revised slightly to improve reproducibility; for the changes, see the present script's history.

Inputs the following 2 raw CSV files
```
# "TRACK_to_T_NIS_Wide20230823_19_49_36_1.csv"
# "TRACK_to_T_NIS_Wide20230823_19_49_36_2.csv"
```

Outputs `cleaned_lifepak_ttt_phase_2_YYYY-MM-DD.csv` (where `YYYY-MM-DD` is the system date)

## Other Documentation

The following files in `/TRACK to TREAT P2/` are relevant to data cleaning.

### General

- `/TRACK to TREAT P2/Data/README_ttt_p2_data_collection.docx`
- `/TRACK to TREAT P2/LSMH Participant Database Backups/`
- `/TRACK to TREAT P2/Data Cleaning/README_ttt_p2_data_cleaning.docx`
  - Now points to [jwe4ec/track-to-treat](https://github.com/jwe4ec/track-to-treat) repo as most recent data cleaning effort

### Qualtrics

- `/TRACK to TREAT P2/Data/Qualtrics/Raw/README_ttt_p2_raw_qualtrics_data.docx`