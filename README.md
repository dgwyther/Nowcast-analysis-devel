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
    ├── autoplot_sshsst.py               - running this script `python autoplot_sshsst.py` will generate a plot. Settings are inside script
    ├── autoplot_sshsst_zoom.py          - run this script (see below) from cmd line to plot a zoomed region
    ├── analyses/               - repeatable analyses
    ├── ext/                    - source code from other people
    ├── functions/              - functions
    └── project/                - project code, final toolkit code, etc.
```
---
### Files:
`autoplot_sshsst.py`        
- This script will plot the 12:00 snapshot fields of SSH and SST for OMAPS and ROMS. Settings are set in the script. 
- Key values to change are:
    -  `date_file_path = '/g/data/fu5/deg581/Nowcast-analysis-devel/data/raw/datefile.txt'`
    -  `base_dir = '/g/data/fu5/eac/NOWCAST/output/'`
    -  `out_dir = '/g/data/fu5/deg581/Nowcast-analysis-devel/out/'`
- file is saved to the `out_dir` with the name of `date_SSHSST.png`

`autoplot_sshsst_zoom.py`        
- This script is meant to be run from the command line and will plot the 12:00 snapshot fields of SSH and SST for OMAPS and ROMS but with zoomed extents. 
- It should be run as:
    -  Use it like `python autoplot_sshsst_zoom.py -i '/path/to/modelcode' -o '/path/to/output/image/' -d '/path/to/datefile.txt' -z lonmin,lonmax,latmin,latmax`
    -  For example `python autoplot_sshsst_zoom.py -i '/g/data/fu5/eac/NOWCAST/output/' -o '/g/data/fu5/deg581/Nowcast-analysis-devel/out/' -d '/g/data/fu5/deg581/Nowcast-analysis-devel/data/raw/datefile.txt' -z 150,155,-36,-31.5`
- file is saved to the `out_dir` with the name of `date_lonmin,lonmax,latmin,latmax_SSHSST.png`
