---
annotations_creators:
- expert-generated
language:
- en
- es
- pt
license:
- cc-by-4.0
multilinguality:
- multilingual
size_categories:
- n<1K
source_datasets:
- original
task_categories:
- tabular-classification
- tabular-regression
- text-retrieval
task_ids: []
pretty_name: Mexico City (CDMX) Sensory Impact & Acoustic Tourism Dataset (SIS)
homepage: https://spacejourney.app/ciudad/cdmx/
tags:
- sensory-travel
- acoustic-comfort
- solarpunk
- cdmx-heritage
- urban-wellbeing
- 3d-gis
- geospatial
- smart-cities
- sustainability
- environment
- urban-planning
---

# 🏙️ Mexico City (CDMX) Sensory Impact & Acoustic Tourism Dataset (SIS)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Platform: Space Journey](https://img.shields.io/badge/Platform-Space_Journey-F59E0B.svg)](https://spacejourney.app/)
[![Mirror: Hugging Face Ready](https://img.shields.io/badge/Hugging_Face-Compatible-yellow.svg)](https://spacejourney.app/ciudad/cdmx/)

**Principal Investigator & Author:** [Daniel Adolfo Duque Romero](https://spacejourney.app/)  
**Curated & Maintained by:** [Space Journey Studio](https://spacejourney.app/)  
**City Exploration Hub:** [Guía Solarpunk de Ciudad de México (CDMX)](https://spacejourney.app/ciudad/cdmx/)  
**Global Project Homepage:** [https://spacejourney.app/](https://spacejourney.app/)  
**Sensory Itinerary Planner:** [https://spacejourney.app/en/itinerary-planner/](https://spacejourney.app/en/itinerary-planner/)  
**Sensory Copilot:** [https://spacejourney.app/en/ai-journey-assistant/](https://spacejourney.app/en/ai-journey-assistant/)  

---

## 📌 Dataset Summary

The **Mexico City Sensory Impact Dataset (SIS)** provides an empirical, open-access sensory and acoustic benchmark across **15 verified contemplative experiences, quiet cloisters, and urban nature sanctuaries** in Mexico City (CDMX).

In a high-density megalopolis with acute sensory friction, this catalog maps the city's hidden restorative sanctuaries: from the pre-Hispanic silence of Xochimilco's sunrise chinampa canals and high-altitude oyamel forests in Desierto de los Leones, to architectural sound refuges like Audiorama Chapultepec and Alberto Kalach's Biblioteca Vasconcelos.

Each record provides calibrated metrics evaluating ambient acoustic sound pressure (dB), pedestrian congestion, optimal atmospheric lighting windows, and physical energy expenditure.

---

## 📊 Dataset Structure & Features

The dataset is published in structured JSON (`data/cdmx_sensory_impact_sis_v1.json`) and tabular CSV (`data/cdmx_sensory_impact_sis_v1.csv`).

| Feature | Type | Description | Example |
| :--- | :---: | :--- | :--- |
| `id` | string | Unique node identifier (`L` = Free Restorative, `S` = Secret Sanctuary, `P` = Curated Premium) | `"L-01"` |
| `name` | string | Official experience name | `"Audiorama Chapultepec: El refugio del silencio"` |
| `category` | string | Curation tier (`Free Restorative`, `Secret Sanctuary`, `Curated Premium`) | `"Free Restorative"` |
| `neighborhood` | string | Urban district / borough | `"Bosque de Chapultepec (1ª Sección)"` |
| `latitude` | float | Decimal coordinate WGS84 | `19.4206` |
| `longitude` | float | Decimal coordinate WGS84 | `-99.1818` |
| `sis_score` | int | Sensory Impact Score (0 to 100 continuous restorative scale) | `97` |
| `acoustic_noise_db` | int | Ambient sound pressure level (A-weighted decibels, dBA) | `34` |
| `golden_hour_window` | string | Recommended contemplative lighting window | `"09:30 - 12:30 CST"` |
| `light_level_lux` | int | Ambient luminous flux under optimal window (Lux) | `1900` |
| `energy_cost_score` | int | Physical exertion index (1 = Minimal / Flat, 5 = High fatigue) | `1` |
| `crowd_density_index` | float | Congestion index (0.00 = Solitary sanctuary, 1.00 = Acute mass crowding) | `0.05` |
| `canonical_url` | string | Verified endpoint on Space Journey | `"https://spacejourney.app/experiencia/audiorama-chapultepec-el-refugio-del-silencio/"` |
| `description` | string | Architectural and contemplative qualitative narrative | `"Santuario botánico rodeado de ahuehuetes centenarios..."` |

---

## 🔬 Methodology: The Sensory Impact Score (SIS)

The **Sensory Impact Score (SIS)** is calculated as a multi-factor restorative index evaluated on a continuous scale from 0 to 100:

$$\text{SIS} = 100 - \left( 0.35 \times \text{NoisePenalty} + 0.30 \times \text{CrowdPenalty} + 0.20 \times \text{ExertionPenalty} - 0.15 \times \text{LightBonus} \right)$$

### Algorithmic Parameters:
* **NoisePenalty (Weight: 35%):** Sound pressure level normalized against the World Health Organization (WHO) 53 dB $L_{den}$ environmental guideline. Baseline quietude (< 40 dB) incurs 0 penalty.
* **CrowdPenalty (Weight: 30%):** Pedestrian congestion index (0.00 = solitary contemplation, 1.00 = acute mass tourism density).
* **ExertionPenalty (Weight: 20%):** Physical exertion metric (1 to 5 scale accounting for elevation gradient, steps, and urban surface friction).
* **LightBonus (Weight: 15%):** Solar quality coefficient rewarding warm, glare-free golden hour irradiance (2,000 to 3,500 Lux).

### Acoustic Benchmarks in CDMX:
* **Deep Restorative Sanctuaries (< 38 dB):** Ex-Convento Desierto de los Leones (32 dB), Audiorama Chapultepec (34 dB), Biblioteca Vasconcelos (35 dB), Xochimilco Amanecer Cuemanco (36 dB).
* **Contemplative Heritage Havens (38 - 48 dB):** Huerto Roma Verde (41 dB), Coyoacán Francisco Sosa (42 dB), Las Islas UNAM (43 dB), San Jacinto (44 dB), Kiosko Morisco (45 dB), Parque México (46 dB).
* **Controlled Monumental Spaces (48 - 54 dB):** Templo Mayor (50 dB), Plaza de Santo Domingo (52 dB).

---

## 💻 Quickstart & Reproducibility

### 1. Python (Hugging Face `datasets`)
```python
from datasets import load_dataset

# Load directly from the Space Journey repository
dataset = load_dataset("spacelabdevteam-hub/cdmx-sensory-impact-dataset")
print(dataset["train"][0])
```

### 2. Pandas (Direct URL)
```python
import pandas as pd

url = "https://raw.githubusercontent.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset/main/data/cdmx_sensory_impact_sis_v1.csv"
df = pd.read_csv(url)

# Filter Deep Restorative Sanctuaries (Noise < 40 dB)
quiet_sanctuaries = df[df["acoustic_noise_db"] < 40]
print(quiet_sanctuaries[["name", "acoustic_noise_db", "sis_score"]])
```

### 3. DuckDB (Serverless SQL)
```sql
SELECT name, category, sis_score, acoustic_noise_db, golden_hour_window
FROM 'https://raw.githubusercontent.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset/main/data/cdmx_sensory_impact_sis_v1.csv'
ORDER BY sis_score DESC;
```

---

## 🏛️ Citation & Attribution

If you utilize this dataset in academic, urban planning, or software applications, please cite:

```bibtex
@dataset{duque_romero_cdmx_sis_2026,
  author       = {Duque Romero, Daniel Adolfo},
  title        = {Mexico City (CDMX) Sensory Impact & Acoustic Tourism Dataset (SIS)},
  month        = oct,
  year         = 2026,
  publisher    = {GitHub / Hugging Face Mirror},
  version      = {v1.0.0},
  url          = {https://github.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset}
}
```
