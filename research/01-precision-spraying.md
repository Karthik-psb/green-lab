# Vertical 1: Precision Spraying and Weed Detection

## What It Is

Computer vision mounted on a sprayer identifies individual plants in a field, distinguishes crops from weeds in real time, and applies herbicide only where a weed is detected. Result: up to 77% reduction in herbicide use per pass.

## Technology Landscape

Leading global implementation: John Deere See and Spray (acquired from Blue River Technology). Cameras at 30fps, deep learning models trained on millions of plant images, on-device edge inference, individually addressable nozzles.

Key technologies: YOLO-class object detection, high-speed camera arrays, real-time edge inference.

## India Market Context

India herbicide market: over Rs. 8,000 crore annually and growing. Weed management in paddy, wheat, cotton, and sugarcane is a major labour and chemical burden for farmers.

The John Deere See and Spray unit costs several lakh rupees — out of reach for a 1-2 hectare Indian smallholder. The deployment model in India must be fundamentally different (service model through Custom Hiring Centres, not product sale).

## India-Specific Considerations

- Average Indian farm: 1.08 hectares. Tractor-based systems exist but machines are often hired, not owned. A sprayer attachment must fit Indian tractor sizes (28-50 HP common).
- Crop diversity: Indian farms are often mixed-crop, complicating model training. Monoculture models perform poorly on mixed fields.
- Power and connectivity: Edge inference is essential. No cloud dependency.
- Affordability: Unit economics must work on a pay-per-acre service model through CHCs/FPOs.

## Potential Business Model

Service model via Custom Hiring Centres (CHCs) and FPOs. The sprayer attachment is owned by the CHC/FPO and rented by the acre.

Indicative pricing: Rs. 300-500 per acre per spray pass vs Rs. 200-300 for conventional. Farmer pays small premium but saves Rs. 500-800/acre in herbicide costs.

## Key Unknowns

- Minimum viable camera and compute configuration for India-priced attachment?
- Which crops and weeds to train on first? (Paddy + water hyacinth? Wheat + phalaris minor?)
- Regulatory requirements for herbicide application equipment in India?
- Trained dataset for Indian weed species? (PlantVillage has disease data but limited Indian weed data)

## Key Datasets

- PlantVillage: disease images, limited weed data
- iNaturalist: some Indian weed species images
- ICAR research stations: potential partnership for labelled weed data
- Priority: build a purpose-built Indian weed-vs-crop dataset

## Assessment

High impact if solved, but capital-intensive (hardware + ML + distribution). Better suited to Phase 2-3 after validating a pure software MVP first. Not the recommended first MVP wedge.
