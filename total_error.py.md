[**Script Location**](https://repositories.arlut.utexas.edu/ICESat2_PPD/PPD/-/blob/master/Pointing/pointing_src/total_error.py)

[[_TOC_]]

## Description

Write all errors from pointing `.rul` files in `/work/PPD/Pointing/bin/` to `pointing_err.txt`

## Arguments

1. `/work/PPD/Pointing/bin/`
2. `/work/PPD/Pointing/pointing_out/year_<year>/day_<yday>/`

Example:

`/work/PPD/Pointing/bin/ /work/PPD/Pointing/pointing_out/year_2023/day_044/`

## Input Files

- .rul files from Pointing Executables: `*.rul`

## Output Files

**Output File Location**

`/work/PPD/Pointing/pointing_out/year_yyyy/day_ddd`

---

### pointing_err.txt

**Description**

&nbsp; &nbsp; &nbsp; &nbsp;
Errors from pointing

**Sampling Frequency**

&nbsp; &nbsp; &nbsp; &nbsp;
N/A

**Column Description**

| script_name | error text | 
| ---        | ---     | 

---
