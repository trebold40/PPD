[**Script Location**](https://repositories.arlut.utexas.edu/ICESat2_PPD/PPD/-/blob/master/PreProc/ATL02/codes/pre_proc_src/ttg_align_lrshyd.c)

[[_TOC_]]

## Description

Write time tags from stellar centroids and time corrected star tracker quaternions to a file. There are no flags to determine what file the time tag came from. 

## Arguments

1. `/work/PPD/PreProc/ATL02/output/year_<year>/day_<yday>/`
2. `atti_hyd1_tcorr.dat`
3. `atti_hyd2_tcorr.dat`

Example:

`/work/PPD/PreProc/ATL02/output/year_2023/day_044/ atti_hyd1_tcorr.dat atti_hyd2_tcorr.dat`

## Input Files

- Continuous Star Tracker Quaternions with Shifted Time Tags: `atti_hyd*_tcorr.dat`
- Stellar Centroid File: `FOV_pxl_coi.dat`

## Output Files

**Output File Location**

`/work/PPD/PreProc/ATL02/output/year_yyyy/day_ddd/`

---

### ttg_of_lrshyd.dat

**Description**

&nbsp; &nbsp; &nbsp; &nbsp;
Time tags from the stellar side centroids and the star tracker quaternion files in chronological order. 

**Sampling Frequency**

&nbsp; &nbsp; &nbsp; &nbsp;
N/A

**Column Descriptions**

| delta_time |
| ---        |


