## Nowcast analysis development

### Folder Structure
```
.
├ README.md                 - this readme file.
├── /data/                  - all data files put here
│   ├── proc/                   - processed files (e.g. CDO/NCO output, ROMS subsets)
│   └── raw/                    - raw data
├── /docs/                  - PDFs, manuals, etc
├── /notebooks/             - exploratory science in notebooks
│   
│   
└── /src                    - source code
    ├── ckerry_autoplot_test_v1.py               - testing a script to load data and make plot
    ├── analyses/               - repeatable analyses
    ├── ext/                    - source code from other people
    ├── functions/              - functions
    └── project/                - project code, final toolkit code, etc.
```
---
### Progress:
ckerry_autoplot_test_v1.py <-- this script will load a date from a datefile at the given location then make plots from the ROMS and OMAPS files.
