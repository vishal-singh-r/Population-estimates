# Population estimates

Create population estimates for age and sex combinations from 1995 to 2000 at SA2-level (Australia | 2021 boundaries) and 1995 to 2023 at suburb-level (Queensland, Australia | 2016 and 2021 boundaries). The data is available at 5-year age groups and age groups better suited for research on cardiovascular diseases.

## Authors
Vishal Singh<sup>1,2</sup><br>
Susanna Cramb<sup>1</sup><br>
Javier Cortes-Ramirez<sup>1,2</sup>

<sup>1</sup>School of Public Health and Social Work, Queensland University of Technology <br>
<sup>2</sup>Centre for Data Science, Queensland University of Technology

## Methodology

<img width="1536" alt="Population estimates strategy" src="https://github.com/user-attachments/assets/c30ef6ec-687a-4dba-b0a0-0ac935b52b2f" />

### Step 1: Starting point: Estimated resident population ASGS 2021

### Step 2: Extrapolating data to 1995:2000
Extrapolation was done through calculation of growth rate with 2001 as starting point. After testing all variations, including  constant growth rate from 1 to 22 years in future and growth rates considering earlier years having higher influence over past predictions than later years, 1-year backcasting provided results closest to state-level estimates.
### Step 3: Correct SA2-level estimates using state-level estimates
There were deviations between SA2-level extrapolation results and state-level ABS estimates across age-group, sex and state combinations. The SA2-level estimates were adjusted by the ratio of deviations in each strate to get numbers closer to ABS estimates.
Even ABS estimates did not match with each other for 2001 to 2023 years, but they were not adjusted to match with state-level totals as SA2-level data provides more richness and adjustments would have created non-integers, which would require rounding. Thus, SA2 ABS estimates were kept as is for years 2001:2023.
### Step 4: Creating ASGS 2021 SA1 level population using ratio of population changes at SA2-level using 2011 as start point
Australian statistical area boundaries are structured in a way that everything at lower levels work as building blocks for higher level structures. That is, mesh blocks make up SA1s, SA1s make up SA2, and so on. Thus, we can distribute people amoung lower-level boundaries contained in a higher-level boundary based on population distributions without the risk of population transfer to external boundaries.
If we assume that the trend of population changes happening at SA2-level are also happening at SA1-level, we can use proportional changes in population to retrodict population in past years.
SA1 level data was only available for Queensland.
### Step 5: Converting to 2021 suburb using correspondence data
Now that we have population estimates at SA1-level, we can use ABS correspondece information to get sububr-level estimates. This correspondence is a much higher quality than conversion from SA2-level to suburb-level as SA1s are smaller in size and a suburb usually contains an SA1 wholly, so the number of people do not get transferred as much, which could cause significant changes in age and sex structures, especially in low-population areas.
### Step 6: Converting 2021 suburb to 2016 suburb using correspondence data
Minor changes were made between 2016 and 2021 suburb boundaries, which resulted in good quality correspondence between them.

## Corrections
If you see mistakes or want to suggest changes, please create an issue on the source repository.

## Reuse
Text and figures are licensed under Creative Commons Attribution CC BY-SA 4.0. Source code is available at https://github.com/ctrl-shift-vs/Population-estimates, unless otherwise noted. The figures that have been reused from other sources don't fall under this license and can be recognized by a note in their caption: "Figure from ...".

## Citation
### For attribution, please cite this work as:
Singh, et al. (2025, March 8). Population estimates. Retrieved from https://github.com/ctrl-shift-vs/Population-estimates

### BibTeX citation:
@misc{singh2025population,
  author = {Singh, Vishal and Cramb, Susanna and Cortes-Ramirez, Javier},
  title = {Population estimates},
  url = {https://github.com/ctrl-shift-vs/Population-estimates},
  year = {2025}
}
