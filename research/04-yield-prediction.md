# Vertical 4: Satellite and Drone Yield Prediction

## What It Is

Using multispectral satellite or drone imagery combined with ground truth yield data, AI models predict crop yield at the field level weeks before harvest. This enables Farmer Producer Organizations (FPOs), agri-lenders, crop insurance companies, and commodity buyers to plan based on data rather than estimates.

## Technology Landscape

Key tools and data sources:
- Sentinel-2 (ESA): free 10m resolution multispectral imagery, 5-day revisit
- Landsat 8/9 (USGS/NASA): free 30m resolution, 16-day revisit
- Planet Labs: commercial 3-5m resolution, daily revisit (expensive)
- NDVI (Normalized Difference Vegetation Index): the standard crop health indicator
- Vegetation indices: EVI, SAVI, LAI (Leaf Area Index) for more specific signals
- Deep learning approaches: LSTM and Transformer models for time-series NDVI + weather data

Bayer's Climate Corporation uses this approach at scale globally, covering hundreds of millions of acres.

## India Market Context

India's agricultural credit and insurance markets are massive:
- Pradhan Mantri Fasal Bima Yojana (PMFBY): government crop insurance scheme, covers tens of millions of farmers
- Kisan Credit Card: short-term crop loans for 70+ million farmers
- FPO sector: 10,000+ FPOs registered, growing as the government's preferred model for smallholder aggregation

Current pain points:
- PMFBY uses crop cutting experiments (manual physical sampling) for yield estimation — slow, expensive, and inaccurate
- Banks and MFIs underwriting agri-loans lack field-level crop health data
- Commodity buyers (traders, processors) cannot plan procurement without reliable yield forecasts

An accurate satellite-based yield prediction system could save hundreds of crores in PMFBY assessment costs alone, and open a large B2B revenue opportunity.

## India-Specific Challenges

- Cloud cover: during kharif season (July-September, when paddy is grown), cloud cover in many Indian regions is 80-100% for weeks at a time, making optical satellite data unreliable
- Solution approaches: SAR (Synthetic Aperture Radar) imagery from Sentinel-1 penetrates clouds; data fusion with reanalysis weather products
- Small field sizes: India's average farm is 1.08 hectares, which may be smaller than a single Sentinel-2 pixel for some use cases. Sentinel-2's 10m pixel is actually enough for a 1-hectare field
- Ground truth data: need historical yield records for model training. These exist in ICRISAT and some state agriculture departments but access is restricted

## Business Model

B2B to crop insurance companies: sell field-level yield predictions as an input to PMFBY claims processing. Revenue per acre assessed.
B2B to agri-lenders: credit underwriting scores based on real-time crop health monitoring. Revenue per loan processed.
B2B to FPOs: seasonal crop advisory and pre-harvest yield estimates for procurement planning. SaaS fee per FPO.
B2G (government): partner with state agriculture departments to replace crop cutting experiments.

## Assessment

High B2B revenue potential and large market. More complex technically than disease detection (requires time-series modelling, SAR data handling, and ground truth collection). Better positioned as a Phase 2-3 vertical once we have credibility and distribution from Phase 1. The FPO relationship built during disease detection MVP is the natural distribution channel for this product.
