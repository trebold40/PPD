[**Script Location**](https://repositories.arlut.utexas.edu/ICESat2_PPD/PPD/-/blob/master/PreProc/ATL02/codes/pre_proc_src/ttg_align_lrshydgyr.c)

[[_TOC_]]

## Description


## Arguments

1. `/work/PPD/PreProc/ATL02/output/year_<year>/day_<yday>/`
2. `/atti_hyd1_tcorr.dat`
3. `/atti_hyd2_tcorr.dat`

Example:

`/work/PPD/PreProc/ATL02/output/year_2023/day_044/ /atti_hyd1_tcorr.dat /atti_hyd2_tcorr.dat`

## Input Files

- Aligned Stellar Side Centroid Data File: `FOV_pxl_coi_align.dat`
- Continuous Star Tracker Quaternions with Shifted Time Tags: `atti_hyd*_tcorr.dat`
- Interpolated 3-axis LRS gyro rate data: `g_rate_all_intp.dat`

## Output Files 

**Output File Location**

`/work/PPD/PreProc/ATL02/output/year_yyyy/day_ddd/`

---

### atti_lrshydgyr.dat

**Description**

&nbsp; &nbsp; &nbsp; &nbsp;
Stellar Side centroid data, HYD1 and HYD2 star tracker data, and 10 hz LRS frame gyro rate data, in chronological order and appropriate file flags.

**Sampling Frequency**

&nbsp; &nbsp; &nbsp; &nbsp;
N/A

**Column Descriptions**
&nbsp; &nbsp; &nbsp; &nbsp;
The column `data` refers to the data in the file corresponding to the time tag under `delta_time` and the flag under `file_flag`. The flags are as follows:

- 0 --> `FOV_pxl_coi_align.dat`
- 1 --> `atti_hyd1_tcorr.dat`
- 2 --> `atti_hyd2_tcorr.dat`
- 3 --> `g_rate_all_intp.dat`

| delta_time | file_flag  | data       | 
| ---        | ---        | ---        |