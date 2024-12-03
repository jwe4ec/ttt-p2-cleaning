# ttt-p2-cleaning

This README describes the centralized data cleaning for Phase II of Project TRACK to TREAT, an NIH-funded ([DP5OD028123](https://reporter.nih.gov/project-details/9513058)) sequential multiple assignment randomized controlled trial aimed at harnessing network science to personalize scalable interventions for adolescent depression (ClinicalTrials.gov [NCT04607902](https://classic.clinicaltrials.gov/ct2/show/NCT04607902)).

For questions, please contact [Yama Chang](https://github.com/yamachang) or [Jeremy W. Eberle](https://github.com/jwe4ec) or file an [issue](https://github.com/yamachang/ttt-p2-cleaning/issues).

## Table of Contents

## Citation

### Versioning

### GitHub Releases

### Zenodo DOIs

### Acknowledgments

## Data on Open Science Framework

Raw and centrally cleaned data from the Qualdrics database are stored in [Project TRACK to TREAT](https://osf.io/35w8r) on the Open Science Framework (OSF). The project has two components, with different permissions: a Private Component and a Public Component.

### Private Component

### Public Component

## Cleaning Scripts: Setup and File Relations

The scripts housed in the 'code' folder of this repository are designed to process raw data files. They import the complete raw datasets, redact specific files, and subsequently cleanse the redacted and other raw files, resulting in what we refer to as 'intermediately cleaned' files. It's essential to note that these files are labeled 'intermediate' because further cleaning tailored to specific analyses will be necessary later on.

To execute these cleaning scripts, set up a primary directory (you can name it as you wish, denoted here as '.'). This directory should contain two subfolders: 'data' and 'code'. Ensure the working directory is set to this primary directory. This configuration ensures the scripts manage data importation and exportation correctly using relative file paths.

```
.                                # Parent folder (i.e., working directory)
├── data                         # Data subfolder
└── code                         # Code subfolder
```

## Cleaning Scripts: Functionality



