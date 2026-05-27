# Lean Canvas — green-lab MVP

Working document. Update before moving to Phase 1 build. Current assumption: Smartphone-based crop disease detection MVP.

## Problem

1. A farmer sees disease on their crop but has no fast access to expert diagnosis. The nearest agronomist may be 20+ km away. By the time they get advice, the disease has spread.
2. Existing apps (Plantix, etc.) require reliable internet, don't work well in local languages, and aren't integrated with the FPO ecosystem.
3. Disease outbreaks spread through a village before anyone knows — there is no community-level early warning system.

## Customer Segments

Primary: Smallholder farmers in India (0.5-5 hectares), food crops (paddy, wheat, vegetables), smartphone owners.
Secondary (B2B): Farmer Producer Organizations — 10,000+ registered in India.
Tertiary: Input companies and agri-lenders wanting real-time crop health intelligence.

## Unique Value Proposition

Instant crop disease diagnosis in your language, offline, through your FPO.

## Solution

- Android app with on-device AI model: photograph leaf, get disease + treatment in local language, under 5 seconds, no internet required.
- FPO portal: aggregated outbreak data, early warning alerts across member farms.
- Farmer: free (10 diagnoses/month) or paid (Rs. 99/month).
- FPO: bulk license (Rs. 5-10 per farmer per month).

## Channels

- FPO network: 5-10 FPO partners in pilot geography, extension workers introduce app to members.
- Krishi Vigyan Kendras (KVKs): 731 across India, field extension workers.
- WhatsApp: farmers already share information this way; if it works, word of mouth spreads it.
- State agriculture department partnerships.

## Revenue Streams

- Farmer subscription: Rs. 99/month (freemium, 5-10% conversion of active users)
- FPO bulk license: Rs. 5-10 per farmer per month
- B2B data: aggregated disease outbreak data to input companies and insurance firms
- Sponsored treatment recommendations (with strict ethical guardrails)

## Cost Structure

Fixed: Engineering team (2-3 people): Rs. 3-6 lakh/month. Cloud infra: Rs. 20,000-50,000/month. Data labelling: Rs. 50,000-1 lakh/month.
Variable: FPO acquisition (Rs. 5,000-20,000 per FPO). Image collection (Rs. 10-50 per labelled image).

## Key Metrics

- Monthly active farmers
- Diagnosis accuracy on India field image test set (target: > 85%)
- FPO partners (5 in Phase 1, 20 by end of Phase 2)
- Paid conversion rate
- Disease outbreak alerts generated and acted upon

## Unfair Advantage

- India FPO distribution: deep FPO relationships early are very hard for a global player to replicate.
- India field image dataset: 50,000+ India field images give model accuracy advantage over global competitors using only PlantVillage.
- Local language + voice: designed for the actual farmer, not a translation of a western app.

## Pilot Geography (TBD in Phase 0)

Candidates: Tamil Nadu (strong FPO ecosystem, TNAU partnership potential), Maharashtra (agri-VC ecosystem, Custom Hiring Centre network), Andhra Pradesh / Telangana (large paddy and cotton).

Decision criteria: FPO density, disease incidence, team relationships, state government support.
