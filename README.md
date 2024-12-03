# ttt-p2-cleaning

This repository contains code for centralized data cleaning for Phase II of Project TRACK to TREAT. The repo is linked to this project on the Open Science Framework (OSF): [TODO](TODO).

## Table of Contents

- [Project Overview](#project-overview)
- [Data](#data)
- [Code](#code)
- [Other Documentation](#other-documentation)
- [TODOs](#todos)

## Project Overview

Phase II of Project TRACK to TREAT (TTT) aims to TODO.

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

### Scripts

TODO

## Other Documentation

The following files in the TODO folder are relevant to data cleaning

TODO

## TODOs

- TODO