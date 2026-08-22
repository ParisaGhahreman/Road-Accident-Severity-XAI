# Data sources

This project analyzes road-accident data from the United Kingdom, France, and Ethiopia. Dataset files are not distributed in this repository.

## United Kingdom
- Dataset: STATS19 Road Safety Open Data
- Analysis year: 2025
- Source URL: https://www.gov.uk/government/statistical-data-sets/road-safety-open-data
- Files used: collision, vehicle, and casualty CSV files for 2025.
- License / reuse terms: UK Open Government Licence v3.0 (OGL v3.0). See https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/

## France
- Dataset: BAAC annual road-accident database
- Analysis year: 2024
- Source URL: https://www.data.gouv.fr/datasets/bases-de-donnees-annuelles-des-accidents-corporels-de-la-circulation-routiere-annees-de-2005-a-2024
- Files used: `caract-2024.csv`, `lieux-2024.csv`, `vehicules-2024.csv`, and `usagers-2024.csv`.
- License / reuse terms: Licence Ouverte / Open Licence 2.0. See https://www.etalab.gouv.fr/licence-ouverte-open-licence

## Ethiopia
- Dataset: Addis Ababa City Road Traffic Accident Severity Dataset
- Coverage: Addis Ababa, Ethiopia; 2016–2022.
- Source URL / DOI: https://doi.org/10.6084/m9.figshare.28122899
- File used: `Addis_Ababa_city_RTA.csv`.
- License / reuse terms: CC BY 4.0. Attribute the dataset creator, Getachew Getu Enyew, and include the licence link: https://creativecommons.org/licenses/by/4.0/

## Reproducibility note
The notebooks expect the local data layout described in `data/README.md`. The repository intentionally excludes the datasets themselves. The code's MIT licence does not replace, extend, or alter these dataset licences.
