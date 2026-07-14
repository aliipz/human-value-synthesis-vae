# Data

This project uses the **European Social Survey Round 11 (ESS11)**, a cross-national survey conducted biennially across Europe. The most recent round includes responses from 50,116 individuals across 30 European countries.

## Why the data is not included

The ESS dataset is freely available but requires registration and acceptance of the ESS terms of use. It cannot be redistributed directly in this repository.

## How to download

1. Go to the ESS Data Portal: [https://ess.sikt.no/en/series/321b06ad-1b98-4b7d-93ad-ca8a24e8788a](https://ess.sikt.no/en/series/321b06ad-1b98-4b7d-93ad-ca8a24e8788a)
2. Create a free account or log in
3. Select **ESS Round 11** and download the **integrated file** in CSV format
4. Rename the file to `ESS11e04_1-subset.csv` and place it in this `data/` folder

## Columns required

The notebook uses the following columns from the integrated file. When downloading, you can select only these to reduce file size:

**Country identifier:**
- `cntry`

**Human Values Scale — PVQ-21 items:**
- `impfreea`, `ipcrtiva` — Self-Direction
- `impdiffa`, `ipadvnta` — Stimulation
- `impfuna`, `ipgdtima` — Hedonism
- `ipsucesa`, `ipshabta` — Achievement
- `impricha`, `iprspota` — Power
- `impsafea`, `ipstrgva` — Security
- `ipbhprpa`, `ipfrulea` — Conformity
- `imptrada`, `ipmodsta` — Tradition
- `iphlppla`, `iplylfra` — Benevolence
- `impenva`, `ipeqopta`, `ipudrsta` — Universalism

## Citation

If you use this data, please cite it as:

> ESS ERIC. (2024). *ESS11 – integrated file, edition 2.0* [Data set]. Sikt – Norwegian Agency for Shared Services in Education and Research. https://doi.org/10.21338/ess11e02_0
