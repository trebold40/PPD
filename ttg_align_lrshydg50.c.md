[**Script Location**](https://repositories.arlut.utexas.edu/ICESat2_PPD/PPD/-/blob/master/PreProc/ATL02/codes/pre_proc_src/smooth/ttg_align_lrshydg50.c)


[[_TOC_]]

# Caveat

We used to use this in the early mission days for the EKF, but now we don't use the stellar side attitude solution anymore because it's not great. We are commenting this script out of the main processing as of 06/12/2023. 


## Description

Create a file that orders the the star tracker quaternions, the stellar side centroids, and the gyro rate data in chronological order. If there are similar time tags the priority order is:

- Centroids
- HYD1 quats
- HYD2 quats
- gyro rates

## Arguments

1. `/work/PPD/PreProc/ATL02/output/year_<year>/day_<yday>/`
2. `atti_hyd1_tcorr.dat`
3. `atti_hyd2_tcorr.dat`

Example:

`/work/PPD/PreProc/ATL02/output/year_2023/day_044/ /atti_hyd1_tcorr.dat /atti_hyd2_tcorr.dat` 

## Input Files

- Aligned Stellar Side Centroid Data File: `FOV_pxl_coi_align.dat`
- Continuous Star Tracker Quaternions with Shifted Time Tags: `atti_hyd*_tcorr.dat`
- 3-axis LRS Frame Gryo Rate File: `g_rate_50_intp.dat`

## Output Files

**Output File Location**

`/work/PPD/PreProc/ATL02/output/year_yyyy/day_ddd/`

---

### atti_lrshydg50.dat

**Description**

&nbsp; &nbsp; &nbsp; &nbsp;
Stellar Side centroid data, HYD1 and HYD2 star tracker data, and 50 hz LRS frame gyro rate data, in chronological order and appropriate file flags. 

**Sampling Frequency**

&nbsp; &nbsp; &nbsp; &nbsp;
N/A

**Column Descriptions**

&nbsp; &nbsp; &nbsp; &nbsp;
The column `data` refers to the data in the file corresponding to the time tag under `delta_time` and the flag under `file_flag`. The flags are as follows:

- 0 --> `FOV_pxl_coi_align.dat`
- 1 --> `atti_hyd1_tcorr.dat`
- 2 --> `atti_hyd2_tcorr.dat`
- 3 --> `g_rate_50_intp.dat`

| delta_time | file_flag | data | 
| ---        | ---       | ---  |
