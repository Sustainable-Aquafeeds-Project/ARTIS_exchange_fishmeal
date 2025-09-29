# README

Repository for analysing the use of fish processing by-products (trimmings) in global fishmeal production and trade, 1996-2020. This work is associated with a pending manuscript assessing the taxonomic composition, geographic origins, and trade flows of fishmeal. 

Please read this file befor trying to reproduce the output from this reserach project. Below you will find information on the potential publication associated with the repository, contact information for the lead author, and a description of the repository structure with each section explained. 

## Approach

Fishmeal has traditionally been produced from whole forage fish. However, an increasing portion now derives from trimmings (by-products of fish and crustacean processing). Despite this trend, comprehensive, open-source data on trimmings based fishmeal have been lacking. 

In this repo we:

1. Integrate multiple data sources - combining Aquatic Resource Trade in Species (ARTIS) database with a literature review and additional data sets from industry and scientific literature. 

2. Estimate the share of fishmeal from trimmings vs. whole fish - for each species and source country. 

3. Quantify trade patterns - tracing origins, processors, and importers of fishmeal.

4. Compare with industry statistics - to validate and highlight where our analysis expands existing coverage (e.g., inclusion of shrimp aquaculutre trimmings)

Our findings show that trimmings-derived fishmeal is not only a Western niche, but also a major component of fishmeal production in Asias, with significant untapped potential for expaning trimmings utilisation globally. 

## Analytical Framework

 - Species level data assignment and trimmings estimation: We conducted a literature review and found research and reports that reported what species were used in fishmeal, and whether they were rendered whole fish or with trimmings. From this, we created a metric describing the average proportion of fishmeal created from each species derived from trimmings or whole fish. 
 - Trade linkage: We matched to the ARTIS database, on species and origin (country), and for what observations did not match we gapfilled the trimmings proportions. We then estimated the amount of fishmeal reported as either trimmings or whole fish derived. 
 - Validation: Compared results against IFFO statistics for finfish- and crustacean-derived fishmeal.
 
### Key assumptions

1. Reported trimings proportions are representative for the time period and source country. 
2. Taxonomic assignments exclude implausible contributors (e.g., bivalve molluscs reported as being used for fishmeal)
 
### Limitations
 - Our literature review is likely incomplete for some species and countries.
 - ARTIS has inherent limitations, especially for product codes with multiple contribution species and co-products. 
 - Estimates should be interpreted as approximations rather than exact figures. 
 
## File structure

### `prep` folder
 
Contains scripts for cleaning, integrating, and processing raw data into usuable inputs for analysis. Scripts are numbered in the order they should be run. 

### `R` folder

Reference scripts that store directory paths, helper functions, and repeated lookups. 

### `data` folder

Contains raw data from literature and industry sustainability reports on species used in fishmeal production, FAO data on trade, and some ARTIS data used for analysis.

### `int` folder

Contains intermediate processed files used by downstream prep and analysis.

### `outputs` folder

Cleaned and aggregated outputs including country/species-level estimates of trimmings and whole fish fishmeal, and figures used in the manuscript. 

## Contact

Please direct any correspondence to Gage Clawson at gage.clawson@utas.edu.au

## Reproducibility 

We strongly advocate for open and reproducible science. The code in this repository enables a user to recreate the results outlined in the associated publication. A few notes: 

 - Run the code as an R project - scripts use relative paths from the home directory.
 - Large datasets (such as the raw data of the ARTIS database) are not stored on github due to file size limits. Scripts in the `prep` folder contain instructions for downloading and linking to all required data.
 - All external data used are freely accessible online.
 
## Quickstart  
 
To reproduce the analysis:  

1. **Clone the repository**

This can either be done directly from github or in the terminal: https://github.com/Sustainable-Aquafeeds-Project/ARTIS_exchange_fishmeal

   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
   
2. **Open the project in R**

 - Start an R session and open the `.Rproj` file in the repository root. 
 - All scripts rely on relative paths, so working inside the R project is recommended.
 
3. **Download required data**

 - Large external datasets (e.g., ARTIS, FAO) are not stored on github. Follow instructions inside the scripts in the `prep` folder to download and prepare these data. 
 
4. **Run preprocessing scripts**

 - Scripts in the prep folder are numbered in order of execution.
 - Running them sequentially will clean raw data, create intermediate datasets, and generate outputs. 
 
5. **Inspect outputs**
 
  - Results (e.g., country/species level estimates, figures, etc.) are written to the `outputs` folder. 
 
## Data sources and references used in repository

Bachis E 2024 Update on by-product marine ingredients IFFO: The marine ingredients organization Online: https://www.iffo.com/update-product-marine-ingredients#:~:text=IFFO%20has%20calculated%20that%20currently,%2Dproduct%20(Figure%201).&text=To%20better%20understand%20the%20origin,direct%20human%20consumption%20in%202020.

BioMar 2023 BioMar Group Integrated Sustainability Report (BioMar Group) Online: https://www.biomar.com/our-promise/sustainability-report

Cao L, Naylor R, Henriksson P, Leadbitter D, Metian M, Troell M and Zhang W 2015 China’s aquaculture and the world’s wild fisheries Science 347 133–5

Cargill 2023 Cargill Aqua Nutrition Sustainability Report (Cargill, Incorporated, P.O. Box 9300 Minneapolis, MN 55440: Cargill) Online: https://www.cargill.com/doc/1432261381843/cargill-aqua-nutrition-sustainability-report-2023.pdf

Chiu A, Li L, Guo S, Bai J, Fedor C and Naylor R L 2013 Feed and fishmeal use in the production of carp and tilapia in China Aquaculture 414–415 127–34

Edwards P, Tuan L A and Allan G L 2004 A survey of marine trash fish and fish meal as aquaculture feed ingredients in Vietnam (Australian Centre for International Agricultural Research) Online: https://www.aciar.gov.au/sites/default/files/legacy/node/554/wp57.pdf

FAO 2022 Fishery and Aquaculture Statistics. Global production by production source 1950-2020 (FishstatJ).

FAO 2024 Global Aquatic Processed Production Statistics Quantity (1976-2022) Online: https://www.fao.org/fishery/statistics-query/en/trade_pp/trade_pp_quantity

Gephart J A, Agrawal Bejarano R, Gorospe K, Godwin A, Golden C D, Naylor R L, Nash K L, Pace M L and Troell M 2024a Globalization of wild capture and farmed aquatic foods Nat Commun 15 8026

Gephart J, Agrawal Bejarano R, Marks A and Gorospe K 2024b Aquatic Resource Trade in Species (ARTIS) Online: https://knb.ecoinformatics.org/view/doi:10.5063/F1CZ35N7

Greenpeace 2017 Current status of juvenile trash fish fishing in China and its implications for the development of sustainable fisheries in China (Greenpeace East Asia) Online: https://www.greenpeace.org.cn/wp-content/uploads/2017/07/%E6%B5%B7%E6%B4%8B%E6%8A%A5%E5%91%8A_0730%EF%BC%88300ppi%EF%BC%89.pdf

Havfisk 2024 Our products Online: https://www.havfisk.no/en/productsd

Leadbitter D 2019 Driving change in South East Asian trawl fisheries, fishmeal supply, and aquafeed (Fish Matter Pty Ltd) Online: https://www.iffo.com/system/files/downloads/Full%20Report%20on%20South%20East%20Asia.pdf

Melnychuk M C, Clavelle T, Owashi B and Strauss K 2017 Reconstruction of global ex-vessel prices of fished species ed R Prellezo ICES Journal of Marine Science 74 121–33

Newton R and Jackson A 2016 A Project to model the use of fisheries by-products in the production of marine ingredients with special reference to omega- 3 fatty acids EPA and DHA Online: http://rgdoi.net/10.13140/RG.2.2.21237.19687

Péron G, François Mittaine J and Le Gallic B 2010 Where do fishmeal and fish oil products come from? An analysis of the conversion ratios in the global fishmeal industry Marine Policy 34 815–20

Sandström V, Chrysafi A, Lamminen M, Troell M, Jalava M, Piipponen J, Siebert S, Van Hal O, Virkki V and Kummu M 2022 Food system by-products upcycled in livestock and aquaculture feeds can increase global food supply Nat Food 3 729–40

Shea L A, Wabnitz C C C, Cheung W W L, Pauly D and Sumaila U R 2025 Spatial distribution of fishmeal and fish oil factories around the globe Sci. Adv. 11 Online: https://www.science.org/doi/10.1126/sciadv.adr6921

Skretting 2022 Skretting Sustainability Report (Skretting) Online: https://www.skretting.com/en-us/sustainability/sustainability-reporting/sustainability-report-2022/



 
