# Step E — Prototype & Design Specifications

---

## Prototype Overview

VineIQ Version 0.1 — "Arancio Build" (named after the clownfish in the founding story)

This prototype covers three integrated components:
1. IoT Sensor Node (hardware)
2. AI Prediction Engine (software)
3. WhatsApp Interface (UX)

---

## Component 1: IoT Sensor Node — "VineNode S1"

### Physical Specs
| Attribute | Specification |
|---|---|
| Dimensions | 14cm × 9cm × 6cm |
| Weight | 340g (with stake) |
| Enclosure | UV-stabilised ABS, IP67 rated |
| Power | 5W monocrystalline solar panel + 3.7V 6000mAh LiPo |
| Battery life (no sun) | 12 days |
| Connectivity | LoRaWAN Class A (EU868 band) + Bluetooth 5.0 (setup) |
| Data transmission | Every 15 minutes (configurable) |
| Operating temperature | –10°C to +65°C |
| Colour | Terracotta glaze (RAL 8023) with matte black panel |

### Sensors Integrated
| Sensor | Model | Accuracy |
|---|---|---|
| Soil moisture (capacitive) | Sentek Drill & Drop | ±2% VWC |
| Soil temperature | DS18B20 | ±0.5°C |
| Ambient temperature/humidity | SHT40 | ±0.2°C / ±1.8% RH |
| Leaf wetness | Decagon LWS | Qualitative 0–100 |
| Light intensity (PAR) | Apogee SQ-420 | ±5% |
| Rainfall (optional clip-on) | TE Connectivity 525 | 0.2mm resolution |

### Microcontroller
- **MCU:** ESP32-S3 (dual-core Xtensa LX7, 240MHz)
- **LoRa module:** RAK4631 (Nordic nRF52840 + SX1262)
- **Storage:** 16MB flash (local buffering during connectivity loss)
- **Firmware OTA:** Enabled via LoRaWAN fPort 200

### Installation
- Single ground stake (30cm depth) + solar panel arm
- Setup time: < 8 minutes per node
- Pairing: QR code scan via WhatsApp bot — no app required
- Coverage: 1 node per 0.8–1.2 ha (recommended)

---

## Component 2: AI Prediction Engine

### Architecture
```
Data Ingestion Layer
  └── LoRaWAN Gateway → AWS IoT Core → Kinesis Data Streams

Feature Engineering Pipeline
  └── Sensor time-series (15-min) + Sentinel-2 NDVI (5-day) 
      + ECMWF ERA5 reanalysis weather + Copernicus seasonal forecast

Model Stack
  ├── Phenology Predictor: Gradient-boosted ensemble (XGBoost + LightGBM)
  │     └── Trained on: 15yr × 40 cultivar × 3,200 estate dataset (CREA Italy)
  ├── Disease Risk Classifier: CNN on multispectral imagery (ResNet-50 backbone)
  │     └── Classes: Downy mildew, Botrytis, Powdery mildew, Esca, Healthy
  └── Irrigation Scheduler: Reinforcement learning agent (PPO)
        └── Reward: Water use efficiency × predicted Brix at harvest

Output
  └── Natural language generation (NLG) → Italian WhatsApp messages
```

### Prediction Outputs (v0.1)
| Alert Type | Trigger | Lead Time |
|---|---|---|
| Optimal harvest window | Brix model ≥ target threshold | 14 days |
| Frost risk | Min temp forecast < 0°C within 72h | 72 hours |
| Disease pressure alert | CNN confidence > 0.78 on imagery | 5 days |
| Irrigation recommendation | Soil VWC < cultivar-specific threshold | 24 hours |
| Canopy stress detected | NDVI anomaly > 1.5σ from baseline | Immediate |

### Model Performance (Validation Set — 180 estates, 2021–2024)
| Metric | Score |
|---|---|
| Harvest window prediction (within 3 days) | 87.3% accuracy |
| Disease detection (AUC-ROC) | 0.924 |
| Irrigation efficiency improvement vs. manual | +31% |
| Yield improvement vs. control group | +22% average |

---

## Component 3: WhatsApp UX

### Interaction Design

**Onboarding flow (< 5 minutes):**
1. Producer scans QR on VineNode → opens WhatsApp chat with +39 02 VineIQ number
2. Bot confirms location, auto-detects cultivar from cadastral parcel data
3. Producer confirms cultivar + target Brix + harvest style preference (early/classic/late)
4. System activated — first readings arrive within 15 minutes

**Daily digest (7:00 AM local time):**
```
🍇 *VineIQ · Tenuta Ferrara · Lunedì 14 aprile*

🌡️ Stanotte min –0.2°C → ⚠️ RISCHIO GELO MODERATO
   Consiglio: attiva protezione antigelo sulle zone A2 e B1

💧 Umidità suolo: 34% VWC (ottimale per Aglianico)
   Nessuna irrigazione necessaria oggi.

🔭 Previsione vendemmia: 18–22 settembre (aggiornata ieri)
   Confidenza modello: 84%

📸 Immagine Sentinel-2 di giovedì → 
   [thumbnail: stress canopy detected parcella C3]
   
Vuoi il report completo? Rispondi *report*
```

**Voice note alerts** for urgent events (frost, severe disease pressure) — 30-second audio in producer's regional dialect (Barese, Napoletano, Siciliano options).

---

## Design Language

| Element | Specification |
|---|---|
| Primary colour | Burgundy #6B1A2A |
| Accent | Harvest gold #C9A84C |
| Background | Parchment #F5F0E8 |
| Dark UI | Slate #1A1A2E |
| Primary typeface | Playfair Display (headings) |
| Body typeface | Inter (UI, data) |
| Illustration style | Botanical line drawing + topographic contour overlay |
| Photography style | Golden-hour vineyards, hands on vines, terracotta detail |
| Icon set | Custom — terra cotta coloured, single-weight stroke |

---

## Bill of Materials (per VineNode S1, target unit cost at 1,000+ units)

| Component | Cost (€) |
|---|---|
| ESP32-S3 + RAK4631 module | 18.40 |
| SHT40 sensor | 3.20 |
| DS18B20 sensor | 1.10 |
| Sentek soil moisture probe | 28.00 |
| LWS leaf wetness sensor | 12.50 |
| Apogee PAR sensor | 44.00 |
| 5W solar panel | 9.80 |
| 6000mAh LiPo + BMS | 7.20 |
| ABS enclosure (custom mould) | 6.40 |
| PCB + assembly | 11.00 |
| Ground stake + hardware | 4.20 |
| Packaging + QR insert | 2.80 |
| **Total BOM** | **€148.60** |
| Target retail (sensor kit 3× nodes) | **€280** |
