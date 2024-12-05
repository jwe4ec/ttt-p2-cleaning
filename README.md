# ttt-p2-cleaning

This repository contains code for centralized data cleaning for Phase II of Project TRACK to TREAT. The repo is linked to this project on the Open Science Framework (OSF): [https://osf.io/yjv72/](https://osf.io/yjv72/).

## Table of Contents

- [Project Overview](#project-overview)
- [Data](#data)
- [Code](#code)
- [Other Documentation](#other-documentation)
- [TODOs](#todos)

## Project Overview

Phase II of Project TRACK to TREAT (TTT) aims to use parameters from network models estimated from ecological momentary assessment (EMA) data to predict treatment response in depressed adolescents. Phase II consisted of an observational part (21 days of EMA with 5 pings per day) followed by an intervention part (i.e., random assignment to one of three single-session interventions [SSIs]: behavioral activation, growth mindset, or active control) completed within 2 weeks later. Qualtrics measures were given at baseline (pre-EMA); immediately pre- and post-SSI; and at 3, 6, 12, 18, and 24 months after post-SSI measures. Random assignment occurred immediately before pre-SSI measures.

Data, initial code, and documentation relevant to centralized data cleaning for Phase II of TTT are stored in the `MSS/Schleider_Lab/jslab/TRACK to TREAT P2 Data Cleaning` folder on the [FSMResFiles](https://www.feinberg.northwestern.edu/it/services/server-storage-and-data/research-data-storage.html) server at [Northwestern University Feinberg School of Medicine](https://www.feinberg.northwestern.edu/).

The initial LifePak data cleaning code was drafted by [Yama Chang](https://github.com/yamachang), who adapted [Michael Mullarkey](https://github.com/mcmullarkey)'s LifePak data cleaning code from Phase I of TTT. The present repo houses [Jeremy Eberle](https://github.com/jwe4ec) and [Isaac Ahuvia](https://github.com/isaacahuvia)'s completion of data cleaning for Phase II. For centralized data cleaning for Phase I of TTT, see the separate repo [ttt-p1-main-analysis](https://github.com/jwe4ec/ttt-p1-main-analysis).

Lab staff who contributed to Phase II of TTT include current research coordinator [Alyssa Gorkin](https://github.com/alyssagorkin) and former research coordinators Sharon Chen, Arielle Smith, Laura Jans, and Chantelle Roulston.

## Data

### Raw

#### From Qualtrics

TODO

#### From LifePak

TODO

### Clean

TODO

## Code

### Setup and File Relations

The scripts in the `code` folder of this repo import the raw data, deidentify the data, and clean the deidentified data, resulting in what we refer to as "intermediately cleaned" files ("intermediate" because additional cleaning will be needed specific to any given analysis).

To run the code, create a parent directory (name it as you wish, denoted here as `.`) with two subfolders: `data` and `code`. Ensure the working directory is set to this parent directory. This setup ensures the code imports/exports correctly using relative file paths.

```
.                                # Parent folder (i.e., working directory)
├── data                         # Data subfolder
└── code                         # Code subfolder
```

TODO: Update this section (e.g., re "cleaned_data" directory created by cleaning script)

### Scripts

TODO: Present script on repo reproduces output of Yama's `ttt_p2_lifepak_cleaning_07312024` sent on 8/1/24
- That is, reproduces `cleaned_lifepak_ttt_phase_2_2024-08-01.csv` via `identical(x, y, FALSE, FALSE, FALSE, FALSE)`
- Finish processing contents of `R:\MSS\Schleider_Lab\jslab\TRACK to TREAT P2 Data Cleaning\2024.08.01 From Yama Chang` 

## Other Documentation

The following files in the TODO folder are relevant to data cleaning

TODO

## TODOs

- TODO