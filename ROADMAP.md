# green-lab Roadmap

AI + Agriculture for India — phased plan from research to commercialization.

## Phase 0: Scoping and Research (Current)

Goal: Define the MVP wedge and the first pilot geography before writing a single line of product code.

Milestones:
- Map all five verticals against four criteria: problem specificity, data availability, deployment path, and willingness to pay in India
- Shortlist one primary vertical and one backup vertical
- Identify the first pilot geography (state + crop + farming community)
- Establish relationships with at least two Farmer Producer Organizations (FPOs)
- Survey existing open datasets: PlantVillage, iSDA soil maps, IMD weather API, ISRO Bhuvan satellite data, ICAR datasets
- Define the success metric for Phase 1 (what number proves the MVP works)

Deliverables in this repo:
- research/vertical-comparison.md
- research/india-datasets.md
- business-model/lean-canvas.md
- docs/pilot-geography.md

Timeline: 6-8 weeks

---

## Phase 1: MVP Build

Goal: A working prototype that produces a measurable result on a real farm.

Assumed vertical (to be confirmed in Phase 0): Smartphone-based crop disease detection.

Milestones:
- Collect or source 5,000+ labelled images of the target crop diseases in Indian field conditions
- Fine-tune a lightweight model (MobileNetV3 or EfficientNet-Lite) on the dataset
- Build a minimal Android app: photograph a leaf, get a prediction and treatment in under 5 seconds
- Deploy to 5 farmers in the pilot geography for a full growing season
- Collect outcome data: was the diagnosis correct, was the treatment followed, what was the yield impact

Deliverables:
- prototypes/disease-detection/ — model training notebooks
- prototypes/android-app/ — Android client code
- datasets/disease-images/ — dataset documentation and sources
- docs/mvp-spec.md — functional specification

Timeline: 3-4 months

---

## Phase 2: Pilot Expansion

Goal: Move from 5 farmers to 100 farmers. Start generating revenue.

Milestones:
- Partner with 2-3 FPOs to deploy at scale within their membership
- Introduce a paid tier: free for 10 diagnoses/month, Rs. 99/month for unlimited
- Add a second disease class (extend from one crop to two crops)
- Integrate with the government's AgriStack / Farmers' Registry where possible
- Begin data collection for a proprietary Indian field conditions dataset
- Measure: diagnosis accuracy, user retention, net promoter score

Deliverables:
- business-model/unit-economics.md — CAC, LTV, payback period
- business-model/gtm-india.md — go-to-market plan
- prototypes/disease-detection/v2/ — improved model

Timeline: 6 months post-MVP

---

## Phase 3: Second Vertical

Goal: Layer a second AI product on the existing distribution and trust built in Phase 2.

Candidate verticals (order TBD based on Phase 0 analysis):
- AI-driven irrigation scheduling (highest impact in water-stressed belts)
- Yield prediction for FPO aggregation and agri-lending

Milestones:
- Decide second vertical based on Phase 0 findings and Phase 2 farmer feedback
- Build and pilot with 20 farms before broad rollout
- Evaluate hardware requirements (soil sensors, weather stations) and whether to partner or build

Timeline: 6-12 months post Phase 2

---

## Phase 4: Platform and Scale

Goal: green-lab becomes the operating system for the Indian smallholder farm.

Vision:
- A single app through which a farmer can: diagnose disease, schedule irrigation, predict yield, and access credit/insurance products that use green-lab data as underwriting input
- A B2B2F (business-to-business-to-farmer) model where FPOs, input companies, and agri-lenders pay for API access to our crop intelligence data
- Expand to 3 states, 10 crops, 10,000+ active farmer users

Timeline: 18-36 months post Phase 1 MVP

---

## Key Risks and Mitigations

- Low smartphone data connectivity in rural areas: build offline-first, sync when connected
- Distrust of AI among older farmers: deploy via trusted FPO extension workers first
- Labelled Indian field image scarcity: partner with agricultural universities (IARI, ICAR) for data collection
- Competition from government apps (like the existing Pusa Krishi app): differentiate on accuracy, speed, and UX
- Willingness to pay: validate in Phase 1 before building a paywall; use the freemium model with value-added paid features
