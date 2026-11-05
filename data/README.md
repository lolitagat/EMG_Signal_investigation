Documents where our dataset comes from
## Source

This project uses the Surface Electromyographic Signals During Walking dataset from PhysioNet.

- **Dataset:** Surface electromyographic signals collected during long-lasting ground walking of young able-bodied subjects
- **Version:** 1.0.1
- **Source:** https://physionet.org/content/semg/1.0.1/
- **DOI:** https://doi.org/10.13026/grdj-qx06

## Selected Recording

The analysis uses recording S01 from the dataset.

- **Channel:** semg LT TIB.A
- **Muscle:** Left tibialis anterior
- **Activity:** Walking
- **Segment:** First 2 seconds
- **Sampling rate:** 2,000 Hz

## Data Access

The dataset is not duplicated in this repository. The recording is accessed directly from PhysioNet using the WFDB Python library.

The notebook retrieves the selected recording using `wfdb.rdrecord()`.

An internet connection is required to access the dataset.

## Attribution

Di Nardo, F., Morbidoni, C., & Fioretti, S. (2024). *Surface electromyographic signals collected during long-lasting ground walking of young able-bodied subjects* (version 1.0.1). PhysioNet.

https://doi.org/10.13026/grdj-qx06

Dataset license: Open Data Commons Attribution License v1.0 (ODC-BY 1.0).
