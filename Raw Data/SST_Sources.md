# SST and Climate Proxy Sources

Documentation of all climate proxy datasets used in or considered for the Paashi Paleo lake elevation model.

## Column Naming Conventions

- `_SST` suffix: raw measurement points at original sampling resolution
- `_Int` suffix: interpolated to annual resolution (linear interpolation between raw points)
- `Davis1`–`Davis8`: eight SST records from Davis et al. (2020), already at annual resolution

## Proxies Used in Final Model (mld_Longarma)

| Column | Author | Year | Region | Timespan | Resolution | Proxy Type |
|--------|--------|------|--------|----------|------------|------------|
| Seki_Int | Seki et al. | 2002 | NE Pacific / California Margin | 28 kya | ~400 yr | Alkenone SST |
| Palmer_Int | Palmer & Pearson | 2003 | Western Equatorial Pacific | 23 kya | ~600 yr | Mg/Ca SST |
| Davis5 | Davis et al. | 2020 | Sea of Okhotsk | 25 kya | ~300 yr | Diatom transfer function SST |

Full citations (confirm/update):
- Seki, O., et al. (2002). [title needed]. [journal needed].
- Palmer, M.R. & Pearson, P.N. (2003). [title needed]. [journal needed].
- Davis, C.V., et al. (2020). [title needed]. [journal needed].

## Diagnostic Proxies (PDO/ENSO — annual resolution, limited time coverage)

These are used for diagnostic testing only. They cannot be used in the 20,000-year hindcast because they only cover ~1,000 years.

| Column | Author | Year | Region | Coverage | Resolution | Proxy Type |
|--------|--------|------|--------|----------|------------|------------|
| PDO | MacDonald & Case | 2005 | North Pacific (dimensionless index) | 993–1996 CE | Annual | Tree-ring reconstruction |
| ENSO | Li et al. | 2011 | Tropical Pacific (dimensionless index) | 900–2002 CE | Annual | Tree-ring reconstruction |

Full citations:
- MacDonald, G.M. & Case, R.A. (2005). Variations in the Pacific Decadal Oscillation over the past millennium. *Geophysical Research Letters*, 32(8). doi:10.1029/2005GL022478
- Li, J., Xie, S.-P., Cook, E.R., Huang, G., D'Arrigo, R.D., Liu, F., Ma, J. & Zheng, X.-T. (2011). Interdecadal modulation of El Nino amplitude during the past millennium. *Nature Climate Change*, 1, 114–118. doi:10.25921/c8ez-6f86

Download URLs:
- PDO: https://www.ncei.noaa.gov/pub/data/paleo/treering/reconstructions/pdo-macdonald2005-noaa.txt
- ENSO: https://www.ncei.noaa.gov/pub/data/paleo/treering/reconstructions/enso-li2011-noaa.txt

## Relationship Between Proxies

- **Palmer_Int** captures the long-term mean SST of the western equatorial Pacific — the region where ENSO (El Nino-Southern Oscillation) operates on 2-7 year cycles. Palmer's ~600-year resolution averages over these annual fluctuations.
- **Seki_Int** captures the long-term mean SST of the NE Pacific / California margin — the region where the PDO (Pacific Decadal Oscillation) operates on 20-30 year phases. Seki's ~400-year resolution averages over these decadal shifts.
- **PDO** and **ENSO** are the annually resolved versions of the same Pacific climate signals that Seki and Palmer capture in the multi-century mean.

## Other Proxies Considered but Not Used in Final Model

| Column | Author | Year | Region | Timespan | Resolution | Notes |
|--------|--------|------|--------|----------|------------|-------|
| Isono_Int | Isono et al. | 2009 | Japan | 15 kya | ~20 yr | Stalagmite d18O. High resolution but short and not predictive. Excluded. |
| Barron_Int / Davis1 | Barron et al. / Davis et al. | 2003 / 2020 | NE Pacific / California Margin | 15 kya | ~100 yr | Highest resolution among marine records, but short timespan limits hindcast. Used in mld_Short and mld_Cal only. |
| Davis2 | Davis et al. | 2020 | Eastern Pacific | 16 kya | — | Short timespan |
| Davis3 | Davis et al. | 2020 | Sea of Okhotsk | 9 kya | — | Short timespan |
| Davis4 | Davis et al. | 2020 | Sea of Okhotsk | 15 kya | — | Short timespan |
| Davis6 | Davis et al. | 2020 | Sea of Okhotsk | 27 kya | — | Large measurement errors, low resolution |
| Davis7 | Davis et al. | 2020 | Western Pacific | 16 kya | — | Short timespan |
| Davis8 | Davis et al. | 2020 | Eastern Pacific | 15 kya | — | Short timespan |
| Leduc et al. | Leduc et al. | — | Unknown | — | — | Added in error. Excluded. |
