# SST Citation Guide — Corrected

## Proxies Used in Final Model (mld_Longarma)

### 1. Seki_Int — NE Pacific / California Margin

**Correct citation:**
Seki, O., Ishiwatari, R., & Matsumoto, K. (2002). Millennial climate oscillations in NE Pacific surface waters over the last 82 kyr: New evidence from alkenones. *Geophysical Research Letters*, 29(23), 2144. doi:10.1029/2002GL015200

- **Core:** ODP Site 1017, California Margin
- **Proxy:** Alkenone unsaturation index (Uk'37) — sea surface temperature
- **Full record:** ~82,000 years
- **Subset used:** ~28,000 years (most recent portion)
- **Resolution:** ~400 years between measurements (93 raw points in the 28 kyr subset)
- **Primary data source:** Yes

**Notes for paper:**
- The full Seki et al. record extends to 82 kyr. State explicitly that only the most recent ~28 kyr were used (e.g., "we use the last 28 kyr of the 82 kyr record from Seki et al., 2002").

---

### 2. Stott_Int — Western Equatorial Pacific (REPLACED)

**STATUS: Palmer & Pearson (2003) REPLACED with Stott et al. (2007) due to wrong-column error.**

**Previous source (Palmer & Pearson, 2003):**
The values originally used as "Palmer_SST" were actually δ¹¹B (boron isotope ratios in ‰) from Table 1 of Palmer & Pearson (2003), used as a proxy for ENSO behavior but not actually SST values despite being in the plausible range. Additionally, the Palmer & Pearson record had only 18 actual Mg/Ca temperature measurements — too coarse for our model.

**Replacement citation:**
Stott, L., Cannariato, K., Thunell, R., Haug, G.H., Koutavas, A., & Lund, S. (2004). Decline of surface temperature and salinity in the western tropical Pacific Ocean in the Holocene epoch. *Nature*, 431, 56–59. doi:10.1038/nature02903

Stott, L., Timmermann, A., & Thunell, R. (2007). Southern Hemisphere and deep-sea warming led deglacial atmospheric CO2 rise and tropical warming. *Science*, 318(5849), 435–438. doi:10.1126/science.1143791

- **Core:** MD98-2176
- **Coordinates:** 5°S, 133.44°E, 2382 m depth, western tropical Pacific
- **Species:** *Globigerinoides ruber*
- **SST calibration:** Anand & Elderfield (2003) Mg/Ca-temperature relationship
- **Data points:** 271 measurements spanning ~125–20,333 years BP
- **Resolution:** ~50–100 years (Holocene), ~50–55 years (glacial) — vastly superior to Palmer's ~600 years
- **SST range:** 25.4–30.2°C
- **Data source:** NOAA Paleoclimatology archive (stott2007.txt)

---

### 3. Davis5 — Sea of Okhotsk

**Correct citation (original data producer):**
Seki, O., Kawamura, K., Ikehara, M., Nakatsuka, T., & Oba, T. (2004). Variation of alkenone sea surface temperature in the Sea of Okhotsk over the last 85 kyrs. *Organic Geochemistry*, 35(3), 347–354. doi:10.1016/j.orggeochem.2003.11.006

**Compilation accessed through:**
Davis, C.V., Myhre, S.E., Deutsch, C., Caissie, B., Praetorius, S., Borreggine, M., & Thunell, R. (2020). Sea surface temperature across the Subarctic North Pacific and marginal seas through the past 20,000 years: A paleoceanographic synthesis. *Quaternary Science Reviews*, 246, 106519. doi:10.1016/j.quascirev.2020.106519

- **Core:** XP98 PC-2
- **Coordinates:** 50.4°N, 148.32°E, 1258 m depth, Sea of Okhotsk
- **Proxy:** Alkenone unsaturation index (Uk'37) — sea surface temperature
- **Points used:** 46 measurements spanning ~24,700 years
- **Resolution:** ~300–500 years between measurements
- **Primary data source:** Seki et al. (2004); accessed via the Davis et al. (2020) synthesis compilation

---

## Diagnostic Proxies (not in final model, used for validation)

### Davis1 — Eastern Pacific / Northern California Margin

**Correct citation (original data producer):**
Barron, J.A., Heusser, L., Herbert, T., & Lyle, M. (2003). High-resolution climatic evolution of coastal northern California during the past 16,000 years. *Paleoceanography*, 18(1), 1020. doi:10.1029/2002PA000768

**Accessed through:** Davis et al. (2020), as above.

- **Core:** ODP Hole 1019C
- **Coordinates:** 41.68°N, 124.93°W, Eastern Pacific off northern California
- **Proxy:** Alkenone unsaturation index (Uk'37) — sea surface temperature
- **Timespan:** ~15,000 years
- **Resolution:** ~100 years
- **Used in:** mld_Short and mld_Cal diagnostic models only (not the final 20 kyr hindcast)

---

### PDO and ENSO (annual-resolution, limited coverage)

**PDO:**
MacDonald, G.M. & Case, R.A. (2005). Variations in the Pacific Decadal Oscillation over the past millennium. *Geophysical Research Letters*, 32(8). doi:10.1029/2005GL022478

**ENSO:**
Li, J., Xie, S.-P., Cook, E.R., Huang, G., D'Arrigo, R.D., Liu, F., Ma, J., & Zheng, X.-T. (2011). Interdecadal modulation of El Nino amplitude during the past millennium. *Nature Climate Change*, 1, 114–118. doi:10.25921/c8ez-6f86