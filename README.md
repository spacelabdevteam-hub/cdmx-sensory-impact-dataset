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
[![🤗 Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-Datasets-yellow.svg)](https://huggingface.co/datasets/spacejourney/cdmx-sensory-impact-dataset)
[![Mirror: GitHub](https://img.shields.io/badge/GitHub-Repository-blue.svg)](https://github.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/spacelabdevteam-hub/cdmx-sensory-impact-dataset/blob/main/explore_cdmx_sensory_impact.ipynb)

**Principal Investigator & Author:** [Daniel Adolfo Duque Romero](https://spacejourney.app/)  
**Curated & Maintained by:** [Space Journey Studio](https://spacejourney.app/)  
**Hugging Face Hub Dataset:** [spacejourney/cdmx-sensory-impact-dataset](https://huggingface.co/datasets/spacejourney/cdmx-sensory-impact-dataset)  
**City Exploration Hub:** [Guía Solarpunk de Ciudad de México (CDMX)](https://spacejourney.app/ciudad/cdmx/)  
**Global Project Homepage:** [https://spacejourney.app/](https://spacejourney.app/)  
**Sensory Itinerary Planner:** [https://spacejourney.app/en/itinerary-planner/](https://spacejourney.app/en/itinerary-planner/)  
**Sensory Copilot:** [https://spacejourney.app/en/ai-journey-assistant/](https://spacejourney.app/en/ai-journey-assistant/)  

---

## 📌 Dataset Summary

The **Mexico City Sensory Impact Dataset (SIS)** is an empirical, open-access sensory and acoustic benchmark recording quantitative environmental, acoustic, and luminous telemetry across **15 verified contemplative experiences, quiet cloisters, and urban nature sanctuaries** in Mexico City (CDMX).

Reverse-engineered directly from the production telemetry of **Space Journey Studio** and aligned with the Rome V2 and Paris open benchmarks, this catalog maps the restorative topography of a high-density megalopolis: from the pre-Hispanic silence of Xochimilco's sunrise chinampa canals (15 dB) and high-altitude oyamel cloud forests in Desierto de los Leones (30 dB), to architectural sound refuges like Audiorama Chapultepec (20 dB) and Alberto Kalach's Biblioteca Vasconcelos (40 dB).

Each record provides calibrated metrics evaluating ambient acoustic sound pressure (dB), pedestrian congestion, optimal atmospheric lighting windows, and physical energy expenditure.

---

## 📊 Dataset Structure & Features

The dataset is published in structured JSON (`data/cdmx_sensory_impact_sis_v1.json`) and tabular CSV (`data/cdmx_sensory_impact_sis_v1.csv`).

| Feature | Type | Description | Example |
| :--- | :---: | :--- | :--- |
| `id` | string | Unique node identifier (`L` = Free Restorative, `S` = Secret Sanctuary, `P` = Curated Premium) | `"L-01"` |
| `name` | string | Official experience name (English) | `"Audiorama Chapultepec: Sound Refuge of Ahuehuetes"` |
| `name_es` | string | Official experience name (Spanish) | `"Audiorama Chapultepec: El refugio del silencio"` |
| `category` | string | Curation tier (`Free Restorative`, `Secret Sanctuary`, `Curated Premium`) | `"Free Restorative"` |
| `neighborhood` | string | Urban district / borough | `"Bosque de Chapultepec (1ª Sección)"` |
| `latitude` | float | Decimal coordinate WGS84 | `19.41943` |
| `longitude` | float | Decimal coordinate WGS84 | `-99.18129` |
| `sis_score` | int | Sensory Impact Score (0 to 100 continuous restorative scale) | `97` |
| `acoustic_noise_db` | int | Ambient sound pressure level (A-weighted decibels, dBA) | `20` |
| `golden_hour_window` | string | Recommended contemplative lighting window | `"09:00 - 12:30 CST"` |
| `light_level_lux` | int | Ambient luminous flux under optimal window (Lux) | `1900` |
| `energy_cost_score` | int | Physical exertion index (1 = Minimal / Flat, 5 = High fatigue) | `1` |
| `crowd_density_index` | float | Congestion index (0.00 = Solitary sanctuary, 1.00 = Acute mass crowding) | `0.05` |
| `canonical_url` | string | Verified endpoint on Space Journey | `"https://spacejourney.app/experiencia/audiorama-chapultepec-el-refugio-del-silencio/"` |
| `description` | string | Architectural and contemplative qualitative narrative | `"Botanical sound sanctuary shaded by century-old ahuehuetes..."` |
| `golden_spot_tips` | string | Micro-location vantage point for optimal sensory resonance | `"Blue armchair facing the volcanic grotto..."` |

---

## 🏛️ Master Catalog: 15 Verified Experiences

### 🌿 Free Restorative (5 Nodes)
* **L-01 | Audiorama Chapultepec (20 dB · SIS 97):** Shaded by century-old ahuehuetes with strict community silence and classical audio diffusion.
* **L-02 | Huerto Roma Verde (40 dB · SIS 93):** Agroecological community permaculture with bamboo geodesic domes and melipona bee sanctuaries.
* **L-03 | Kiosko Morisco (45 dB · SIS 89):** Intricate 1884 cast-iron neo-Mudejar pavilion in Santa María la Ribera.
* **L-04 | Parque México (50 dB · SIS 87):** Art Deco elliptical 9-hectare canopy with Lindbergh Forum and dense bamboo sound buffers.
* **L-05 | Las Islas UNAM (55 dB · SIS 85):** Modernist campus esplanade on volcanic pedregal facing Juan O'Gorman mineral stone murals.

### 🗝️ Secret Sanctuary (5 Nodes)
* **S-01 | Desierto de los Leones (30 dB · SIS 95):** 17th-century Discalced Carmelite cloister enveloped in high-mountain oyamel cloud forests.
* **S-02 | Biblioteca Vasconcelos (40 dB · SIS 92):** Alberto Kalach's matrix of suspended glass bookshelves inside a 26,000 sqm endemic garden.
* **S-03 | Coyoacán Francisco Sosa (45 dB · SIS 90):** River-stone avenue with bougainvillea volcanic walls and quiet Plaza de la Conchita.
* **S-04 | Plaza San Jacinto (50 dB · SIS 88):** Shaded San Ángel colonial courtyards, fountain whispers, and open-air artists' studios.
* **S-05 | Plaza Santo Domingo (55 dB · SIS 84):** Historic viceregal arcades preserving centuries-old analog letterpress typing rituals.

### ✨ Curated Premium (5 Nodes)
* **P-01 | Xochimilco Sunrise Cuemanco (15 dB · SIS 98):** Zero-emission electric/poled trajinera navigation through pre-Hispanic mist-veiled chinampas.
* **P-02 | Teotihuacán Hot Air Flight (25 dB · SIS 96):** Silent aerostatic thermal ascension above the Pyramids of the Sun and Moon at dawn.
* **P-03 | Pujol & Quintonil High Gastronomy (40 dB · SIS 92):** Ancestral corn, wild quelites, and intimate acoustic architecture in Polanco.
* **P-04 | Museo Nacional de Antropología (35 dB · SIS 91):** Pedro Ramírez Vázquez waterfall canopy ('El Paraguas') providing acoustic protection.
* **P-05 | Templo Mayor Sacred Axis (45 dB · SIS 88):** Suspended catwalks over superimposed Mexica cosmic strata and Coyolxauhqui monolith.

---

## 🔬 Methodology: The Sensory Impact Score (SIS)

The **Sensory Impact Score (SIS)** is calculated as a multi-factor restorative index evaluated on a continuous scale from 0 to 100:

$$\text{SIS} = 100 - \left( 0.35 \times \text{NoisePenalty} + 0.30 \times \text{CrowdPenalty} + 0.20 \times \text{ExertionPenalty} - 0.15 \times \text{LightBonus} \right)$$

### Algorithmic Parameters:
* **NoisePenalty (Weight: 35%):** Sound pressure level normalized against the World Health Organization (WHO) 53 dB $L_{den}$ environmental guideline. Baseline quietude (< 40 dB) incurs 0 penalty.
* **CrowdPenalty (Weight: 30%):** Pedestrian congestion index (0.00 = solitary contemplation, 1.00 = acute mass tourism density).
* **ExertionPenalty (Weight: 20%):** Physical exertion metric (1 to 5 scale accounting for elevation gradient, steps, and urban surface friction).
* **LightBonus (Weight: 15%):** Solar quality coefficient rewarding warm, glare-free golden hour irradiance (2,000 to 3,500 Lux).

---

## 💻 Quickstart & Reproducibility

### 0. 🚀 Interactive Google Colab (One-Click Live Execution)
Run live sensory telemetry queries and Solarpunk data visualizations directly in Google's cloud with zero local setup:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/spacelabdevteam-hub/cdmx-sensory-impact-dataset/blob/main/explore_cdmx_sensory_impact.ipynb)

### 1. Hugging Face (`datasets` library)
```python
from datasets import load_dataset

# Official Hugging Face Hub Dataset loader
dataset = load_dataset("spacejourney/cdmx-sensory-impact-dataset")

# Print first sanctuary record
print(dataset["train"][0])

# Direct conversion to pandas DataFrame
df = dataset["train"].to_pandas()
print(df[["id", "name", "acoustic_noise_db", "sis_score"]].head())
```

### 2. Python (Pandas)
```python
import pandas as pd

# Load from Hugging Face Hub mirror or raw telemetry
url = "https://raw.githubusercontent.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset/main/data/cdmx_sensory_impact_sis_v1.csv"
df = pd.read_csv(url)

# Filter Deep Restorative Sanctuaries (Noise <= 30 dB)
quiet_sanctuaries = df[df["acoustic_noise_db"] <= 30]
print(quiet_sanctuaries[["id", "name", "acoustic_noise_db", "sis_score"]])
```

### 3. DuckDB (Serverless SQL via Hugging Face Hub)
```sql
SELECT id, name, category, sis_score, acoustic_noise_db, golden_hour_window
FROM 'hf://datasets/spacejourney/cdmx-sensory-impact-dataset/data/cdmx_sensory_impact_sis_v1.csv'
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
  publisher    = {Space Journey Studio / GitHub / Hugging Face},
  version      = {v1.0.0},
  url          = {https://github.com/spacelabdevteam-hub/cdmx-sensory-impact-dataset}
}
```
