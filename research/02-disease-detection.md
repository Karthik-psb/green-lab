# Vertical 2: Smartphone-Based Crop Disease Detection

## What It Is

A farmer photographs a diseased plant leaf with a smartphone. An AI model — running locally on-device or via a lightweight API — identifies the disease and its severity within seconds and returns a treatment recommendation in the farmer's local language.

## Why This Vertical Scores Highest for India MVP

The problem is extremely well-defined (what disease is this leaf showing?), the feedback loop is fast (treatment works or it doesn't within days to weeks), the data is more abundant than any other vertical (PlantVillage alone has 87,000+ images), and the deployment infrastructure already exists (a smartphone app). No hardware beyond the phone the farmer already owns.

## Technology Landscape

Key papers and models:
- Using Deep Learning for Image-Based Plant Disease Detection (Mohanty et al., 2016) — the foundational paper, 99.35% accuracy on PlantVillage
- EfficientNet and MobileNetV3: lightweight architectures suitable for on-device inference
- TensorFlow Lite and ONNX: frameworks for on-device model deployment on Android

Existing apps:
- Plantix (Peat GmbH, Germany): largest crop disease detection app globally, active in India, free to use
- Cropin: Indian agri-tech platform with some disease advisory
- Government apps: IFFCO Kisan, Kisan Suvidha, mKisan

The market is not empty — Plantix has millions of users in India. Our differentiation must be genuine.

## India-Specific Data Problems

PlantVillage images were taken in lab/controlled conditions in the US. Field conditions in India differ substantially:
- Different lighting (harsh direct sun, low contrast)
- Different leaf backgrounds (mixed-crop, soil, thatch)
- Different disease prevalence by geography (blast is dominant in eastern India paddy, smut in Punjab wheat)
- Different crop varieties (desi varieties look different from US hybrid counterparts)

A model fine-tuned on PlantVillage without India field images will underperform in real conditions.

## What We Would Build Differently

- Train on India field images from the start, not just PlantVillage
- Partner with ICAR, Krishi Vigyan Kendras (KVKs), and agricultural universities (TNAU, PAU, IARI) to collect labelled images
- Build an offline-first Android app (inference on device, no data connection required)
- Output in local language (Hindi, Tamil, Telugu, Kannada, Marathi) with a voice option for low-literacy farmers
- Focus on the top 3 disease-crop pairs in the pilot geography first, not trying to cover everything

## Differentiation vs Plantix

Plantix is very good. We should not try to out-feature it on day one. Our differentiation:
- Genuinely offline-first (Plantix requires connectivity for some features)
- Language and voice-first UX for low-literacy smallholders
- Direct FPO integration (diagnoses aggregated at FPO level for bulk advisory)
- Eventually: disease outbreak prediction (if 20% of FPO members report blast in the same week, alert the whole FPO)

## Business Model

Freemium direct-to-farmer: free tier (10 diagnoses/month), paid tier (Rs. 99/month unlimited)
B2B to FPOs: FPO pays Rs. 5-10 per farmer per month for bulk license, provides to members as a service
B2B to input companies: anonymized disease outbreak data sold as agricultural intelligence

## Key Datasets

- PlantVillage: 87,000+ images, 26 diseases, 14 crop species
- iNaturalist: some Indian plant disease observations
- ICAR: needs partnership — they have large proprietary datasets
- Krishi Vigyan Kendras: 731 KVKs across India, each with field extension workers who could contribute images
- Our own collection: structured photo collection protocol for FPO extension workers

## Success Metrics for MVP

- Diagnosis accuracy > 85% on a held-out India field image test set
- App loads and diagnoses offline in < 5 seconds on a mid-range Android (Rs. 8,000-12,000 price point)
- 80%+ of pilot farmers say the recommendation was useful
- At least one farmer reports following the treatment recommendation and seeing improvement

## Assessment

Strongest candidate for Phase 1 MVP. Software-only, fastest path to a working product, clearest success metric, and directly addresses a real farmer pain point. The Plantix competition is real but the India smallholder and FPO distribution angle gives us a genuine wedge.
