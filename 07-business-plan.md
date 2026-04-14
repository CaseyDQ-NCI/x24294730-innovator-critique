# Step G — Business Plan & Marketing Campaign

---

## Executive Summary

**VineIQ SRL** is a Matera-based deeptech startup delivering AI-powered precision viticulture to Italy's 270,000 small wine producers (< 5 ha) — the backbone of the country's DOC/DOCG wine economy — who collectively lose 30–45% of annual yield to climate-driven harvest timing failures yet have zero access to affordable precision agriculture tools. VineIQ delivers its intelligence through a €280 solar IoT sensor kit, a varietal-specific AI engine trained on 40+ indigenous Italian cultivars, and a WhatsApp-native interface requiring no app, no dashboard, and no learning curve. The platform is priced at €199/month — 95% less than legacy alternatives.

**Seeking:** €2M seed round (Q3 2026) | **Use:** 18 months runway to 5,000 producers and Series A readiness

---

## 1. Company Overview

| | |
|---|---|
| Legal entity | VineIQ SRL |
| Headquarters | Via Lucana 42, Matera (MT), 75100 Italy |
| Founded | January 2026 |
| Stage | Pre-seed → Seed |
| Team | 4 co-founders + 6 engineers + 2 agronomists |
| IP | 2 provisional patents filed (sensor calibration algorithm; varietal phenology model) |

---

## 2. Problem & Market

### The Problem (quantified)
- 270,000 Italian wine producers manage estates < 5 ha
- These producers account for 61% of all DOC/DOCG Italian wines
- Average annual harvest loss: 30–45% (climate-driven ripening failures, frost events, disease outbreaks)
- Current precision ag platforms: €12,000–€40,000/year — inaccessible to small producers
- < 8% have access to any digital tool beyond a weather app
- Climate projections (CMCC, RCP 4.5): –22% yield loss by 2035 without intervention

### Market Sizing

| Market | Value | Basis |
|---|---|---|
| Italy TAM | €648M/yr | 270K producers × €2,400 ARPU |
| Mediterranean SAM (5yr) | €4.2B/yr | France, Spain, Portugal, Greece, Croatia |
| Initial SOM (Year 1) | €1.2M ARR | 500 producers × €2,400 |
| SOM (Year 3) | €49M ARR | 25,000 producers |

---

## 3. Product

### VineNode S1 (Hardware)
- 3× solar IoT nodes (soil moisture, temperature, humidity, leaf wetness, PAR, rainfall)
- LoRaWAN connected · IP67 · 3-year maintenance-free · deploys in 30 minutes
- BOM cost: €148.60 · Retail: €280

### AI Engine (SaaS)
- Gradient-boosted harvest window prediction (87% accuracy within 3 days at 14-day lead)
- CNN disease detection (AUC 0.924): Botrytis, Downy mildew, Powdery mildew, Esca
- RL irrigation scheduler (+31% water efficiency vs. manual)
- Sentinel-2 satellite imagery processed per-parcel every 5 days

### WhatsApp Interface
- Zero-download onboarding via QR code
- Daily 7AM digest in Italian
- Voice note alerts in producer's regional dialect
- Cooperative data pooling with anonymised neighbouring estate data

---

## 4. Business Model

### Revenue Streams

| Stream | Price | Contribution |
|---|---|---|
| Platform subscription (Artigiano tier) | €199/mo | 72% of ARR |
| Data co-op premium add-on | €49/mo | 16% of ARR |
| Hardware (VineNode S1 kit) | €280 one-time | 8% of revenue |
| Agronomist consulting | €500/season | 4% of ARR |

### Unit Economics

| Metric | Value |
|---|---|
| CAC | €120 |
| LTV (5-year) | €9,950 |
| LTV:CAC ratio | 83:1 |
| Gross margin (platform) | 78% |
| Gross margin (hardware) | 47% |
| Payback period | 8 months |

### Financial Projections

| Year | Producers | ARR | Revenue | EBITDA |
|---|---|---|---|---|
| 2026 (Y1) | 500 | €1.2M | €1.4M | –€1.8M |
| 2027 (Y2) | 5,000 | €11.4M | €12.8M | –€0.4M |
| 2028 (Y3) | 25,000 | €49M | €53M | €18.6M (38%) |
| 2030 (Y5) | 100,000 | €198M | €210M | €84M (40%) |

---

## 5. Go-to-Market Strategy

### Channel 1: Coldiretti Partnership (Primary)
- Distribution through Italy's largest farmers' association (1.6M members, 270,000 wine producers)
- Co-branded "Coldiretti × VineIQ" programme
- Access to Coldiretti's regional agronomy advisors as field sales force
- Integration into Coldiretti's annual harvest planning resources

### Channel 2: DOC/DOCG Consorzio Partnerships
- Work through individual consorzio boards (Aglianico del Vulture, Fiano di Avellino, Nero d'Avola, etc.)
- Collective subscription models: consorzio negotiates block pricing for members
- Data co-op positioned as a consorzio-level intelligence resource

### Channel 3: WhatsApp Referral Loop
- Every producer who receives a VineIQ morning digest naturally tells neighbours
- Referral mechanic: introduce 3 producers → 1 month free
- Viral coefficient estimated at 1.4 in pilot group

### Channel 4: EU Agri-Tech Grants
- Horizon Europe Agri-Food calls: VineIQ qualifies under Cluster 6 (Climate resilience, circular bioeconomy)
- Italy's PNRR Agri-Tech pillar: €1.2B allocated for digital agriculture tools (2025–2027)
- Coldiretti grant writing partnership to accelerate applications

---

## 6. Competitive Landscape

| Competitor | Price/year | Target customer | Cultivar specificity | UX |
|---|---|---|---|---|
| Trimble Ag | €18,000–€40,000 | 100+ ha industrial | Generic | Desktop dashboard |
| John Deere Operations Center | €12,000–€35,000 | Industrial | Generic | App |
| Sencrop | €600–€2,400 | Mid-size | Weather only | App |
| **VineIQ** | **€2,400** | **1–5 ha artisan** | **40+ Italian varietals** | **WhatsApp** |

**Moat:** Proprietary 15-year indigenous Italian varietal phenology dataset + cooperative network data effect + Coldiretti distribution partnership

---

## 7. Technology & IP

- 2 provisional patents filed (Italy, PCT)
- Training data: 15yr × 40 cultivar × 3,200 estate dataset licensed from CREA (Italy's National Research Centre for Agriculture)
- Satellite data: Copernicus Sentinel-2 (free), Planet Labs (commercial tier)
- Cloud infrastructure: AWS IoT Core + SageMaker + Lambda (EU-West-1)
- Data residency: All producer data stored in EU (GDPR compliant)

---

## 8. Team

| Name | Role | Background |
|---|---|---|
| Sofia Esposito | CEO & Co-Founder | CMCC Foundation (8yr), marine biologist, MSc Naples |
| Marco Venezia | CTO & Co-Founder | John Deere Precision Ag ML lead (Stuttgart), PhD Ag Data Science |
| Chiara Bellini | Head of Agronomy | 20yr viticulture consultant, 3 DOC consorzio advisor |
| Alessandro Ricci | CFO | Ex-CFO 2 agri-tech exits (€80M, €210M), €140M raised |

**Advisors:** Prof. Giovanni Testa (Univ. Naples, viticulture phenology) · Dr. Anna Ferretti (CMCC climate modelling) · Filippo Calabrese (Coldiretti National Board)

---

## 9. Funding

### Seed Round: €2M

**Allocation:**

| Use of funds | % | Amount |
|---|---|---|
| R&D & AI platform development | 40% | €0.80M |
| Sales & marketing (Coldiretti rollout) | 28% | €0.56M |
| Hardware supply chain & manufacturing | 20% | €0.40M |
| Operations, legal, HR | 12% | €0.24M |

**Milestones funded by this round:**
- 500 → 5,000 producers (18 months)
- VineNode S2 hardware revision
- France and Spain pilot (20 producers each, Q4 2027)
- Series A raise at €49M ARR / 25,000 producers

---

## 10. Marketing Campaign: "La Vendemmia Giusta" (The Right Harvest)

### Campaign Concept
*La Vendemmia Giusta* — The Right Harvest — is a campaign that speaks to the existential fear every small Italian wine producer carries: the fear of a bad vintage. The campaign does not sell technology. It sells certainty. It sells the confidence that comes from knowing — 14 days ahead — exactly when to harvest.

### Campaign Phases

**Phase 1 — AWARENESS (Months 1–3): "What the land already knows."**
- Format: 60-second documentary short films featuring real Basilicata and Campania producers
- Tone: Intimate, earthy, Italian. No jargon. No tech speak.
- Distribution: YouTube pre-roll targeting Italian farmers; RAI regional broadcasts; Coldiretti newsletter (1.6M subscribers)
- Key message: "The land has always known when to harvest. Now it can tell you."

**Phase 2 — CONSIDERATION (Months 3–6): "Ask VineIQ."**
- Format: WhatsApp-native campaign. QR codes on Coldiretti materials, local agronomy offices, wine co-ops
- Mechanic: Scan QR → receive a free 7-day harvest forecast for your estate, no signup required
- Goal: 20,000 free forecast requests → 5% conversion to paid trial

**Phase 3 — CONVERSION (Months 6–12): "Your best vintage yet."**
- Format: Peer video testimonials from Pilot Year producers
- Mechanic: Existing producers create 30-second WhatsApp videos → forward to 3 neighbours → unlock free sensor kit
- Goal: Referral loop driving 60% of new signups

**Phase 4 — RETENTION (Ongoing): "Harvest Report"**
- Annual personalised PDF/WhatsApp report: "Your vineyard in 2026" — soil health trajectory, harvest timing performance vs. neighbours, projected improvement for next season
- Timed for December — the reflective period after harvest
- Designed to be proudly shared on social media

### Content Pillars
1. **"La Terra Parla"** (The Land Speaks) — educational content about what soil and satellite data reveal
2. **"Piccola Vigna, Grande Vino"** (Small Vineyard, Great Wine) — producer story series
3. **"Il Modello Dice"** (The Model Says) — demystifying AI for traditional producers
4. **Data Visualisation Posts** — "What a heatwave looks like in your soil" — striking visual content

### KPIs
| Metric | 12-Month Target |
|---|---|
| Waitlist signups | 3,500 |
| Free forecast requests | 20,000 |
| Paid conversions (trial → paid) | 500 |
| Referral conversion rate | 40% |
| Monthly WhatsApp opt-in rate | 25% of trial users |
| Social reach (organic) | 500,000 impressions/month |
