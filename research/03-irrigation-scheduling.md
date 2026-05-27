# Vertical 3: AI-Driven Irrigation Scheduling

## What It Is

AI analyses soil moisture data, weather forecasts, crop growth stage, and evapotranspiration models to determine precisely when to irrigate and how much water to apply. Compared to schedule-based or intuition-based irrigation, AI systems can reduce water use by 20-40% while maintaining or improving yields.

## Why This Matters for India

India uses roughly 80% of its freshwater for agriculture. Groundwater depletion is severe: 16% of assessed groundwater units are over-exploited (CGWB data). Punjab, Haryana, and Rajasthan face severe groundwater stress driven by flood irrigation for paddy and wheat. This vertical has the highest long-term societal impact of the five.

## Technology Components

- Soil moisture sensors (capacitive, low cost: Rs. 500-2,000 per unit)
- Weather API: IMD, OpenWeather, Skymet
- Crop evapotranspiration model: FAO-56 Penman-Monteith (global standard)
- Scheduling algorithm: ML model or rule-based system trained on crop water requirements
- Delivery: SMS alert, app notification, or direct solenoid valve control

## India-Specific Considerations

- Most Indian smallholders use flood irrigation. Drip and sprinkler adoption is growing but still low.
- Biggest impact: reducing flood irrigation frequency and duration, not just optimising drip systems.
- Soil moisture sensors at Rs. 500-2,000 are affordable but require installation, calibration, and maintenance.
- Irregular rural power supply affects sensor and actuator reliability.
- Most practical first step: advisory system (tell farmer when to irrigate), not automated actuation.

## Business Model Options

- Hardware-as-a-service: sensor + subscription bundle. Complex logistics.
- Pure advisory: public weather data + crop model, no proprietary sensor. Lower accuracy but zero hardware cost.
- FPO-level: one sensor network covers a cluster of farms, cost shared.
- Water utility partnership: irrigation departments pay for data to improve canal management.

## Key Data Sources

- IMD: historical and forecast weather data
- FAO AquaCrop: crop water productivity model
- ISRIC SoilGrids: global soil data (250m resolution)
- NASA POWER: satellite-derived meteorological data

## Assessment

Very high long-term impact but hardware dependency and monetisation challenges. Better as a Phase 3 vertical after disease detection MVP builds farmer trust and FPO distribution.
