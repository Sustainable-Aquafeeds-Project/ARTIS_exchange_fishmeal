# README

These scripts prepare and analyse data on trimmings use in fishmeal production.

`01_pull_artis_data.Rmd`: Reads in raw ARTIS data and filters for fishmeal and fillet data.

`02_compile_fm_origins`: Parses through reports from literature review to create datasets describing species used in fishmeal production.

`03_combine_trimmings_origins.Rmd`: Combines all data from the previous step so that we can match to ARTIS data.

`04_gapfilling_part_1.Rmd`: Matches data from previous script to the ARTIS database and gapfills any remaining fishmeal not covered from our literature review.

`05_gapfilling_part_2.Rmd`: Matches data from previous script to the ARTIS database and gapfills any remaining fishmeal not covered from our literature review.

`06_save_analysis_data.Rmd`: Saves data that we can use for analysis and will ultimately be published online.

`07_figs.Rmd`: Creates the figures in the manuscript.

`08_MS_stats.Rmd`: Reads in fishmeal data and finds interesting stats for the manuscript.

`09_scenarios.Rmd`: Runs high level scenarios of by-product utilisation and replacements for fishmeal. 

`10_SI_tables.Rmd`: Creates tables that will be published as supplementary information. 

`test_GAM_modeling`: This folder contains archived scripts where we explored modeling what species are used for trimmings vs whole fish fishmeal, instead of our other gapfilling approaches. 

 