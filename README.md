# Paashi (Tulare Lake) Paleo Lake-Elevation Models

Code and data for a Bayesian hindcast of Paashi / Tulare Lake (San Joaquin
Valley, California) surface elevation over roughly the last 20,000 years,
reconstructed from Pacific sea-surface-temperature (SST) proxies and compared
against an independent geological/paleoenvironmental reconstruction.

This repository accompanies:

> Meyer-Lorey and Pratt, "Bayesian Modeling Validates Paleoenvironmental Evidence for Pleistocene-Holocene Water Levels, Pa'ashi/Tulare Lake, California", in Journal of Archaeological Science Reports [in review]. Preprint of the original submission at: https://dx.doi.org/10.2139/ssrn.7021128

---

## What you need

- **R** (4.2 or newer recommended) and **RStudio**.
- A working **C++ toolchain** for Stan, which `brms` depends on:
  - Windows: install [Rtools](https://cran.r-project.org/bin/windows/Rtools/).
  - macOS: install the Xcode Command Line Tools (`xcode-select --install`).
- The following R packages:

```r
install.packages(c(
  "tidyverse", "brms", "tidybayes", "bayesplot", "loo",
  "bridgesampling", "patchwork", "scales", "ggrepel", "ggthemes", "maps",
  "ggnewscale"
))
```

## How to run

1. **Download the whole repository**, not individual files — use the DOI
   archive's ZIP (or `Code ▸ Download ZIP` on GitHub), then unzip it. Keep the
   folder structure intact: the code reads and writes using relative paths
   (e.g. `Raw Data/...`, `Models/...`), so loose files will not run on their own.
2. **Open `PaashiPaleo.Rproj` in RStudio.** Opening the project sets the working
   directory to the repository root, which is what makes all of those relative
   paths work. (Do not open the `.Rmd` on its own.)
3. Install the packages above if you don't already have them.
4. **Open `Paashi_Paleo_Models_Pub.Rmd`** and run the chunks from top to bottom. This is the main analysis: it loads the data,
   fits/loads the models, and produces every figure. The inline comments walk
   through each step and the reasoning behind it.

## Repository

- `PaashiPaleo.Rproj` - RStudio project file
- `Paashi_Paleo_Models_Pub.Rmd` - Main analysis: data prep, models, and all figures
- `Raw Data/` - Input proxy and observation data (CSV) plus source citations
- `Processed Data/` - output tables used to build the figures
- `Models/` - Pre-fitted `brms` model objects (`.rds`)
- `Figures/` - Created automatically when you run the `.Rmd` (Figure 1, the regional map, was made separately in ArcGIS Pro)

## Reproducibility notes

- Pre-fitted models are included in `Models/`. Re-fitting the `brms` models
  from scratch is computationally intensive (minutes to hours); the saved `.rds`
  objects let you reproduce the published figures without refitting.
- The uncertainty propagation is the slowest step. Its 50 model fits
  (`Models/prop_fits_*.rds`), their bridge-sampling scores
  (`Models/prop_logml_*.rds`) and the SST interpolation draws
  (`Processed Data/SST_draws_*.rds`) are included, and the `.Rmd` reuses them
  when present. Delete them only if you want to regenerate them from scratch.
- Model-fitting chunks use `seed = 2025`; the SST interpolation draws use
  `set.seed(2025)`.

## Data sources

Proxy SST records (final model: Seki et al. 2002; Stott et al. 2004, 2007;
Pahnke et al. 2007; Seki et al. 2004 via Davis et al. 2020; plus the other
screened candidates), the PDO (MacDonald & Case 2005) and ENSO (Li et al. 2011)
reconstructions, the Adams (2015) water-balance model, and the Negrini et al.
(2006) lake-level reconstruction. Full citations and DOIs are in
`Raw Data/Data_Sources.csv`; details of how each is used are in the comments
of the `.Rmd`.

## License

Code in this dataset is released under the MIT License (see LICENSE.txt).
Input data files are derived from previously published sources; rights remain with the original authors and publishers.
See the dataset documentation and the associated article for full citations.