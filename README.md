# Measuring the Real Impact of Carbon Pricing on Global Emissions

## Project Overview

This project examines whether carbon pricing policies (carbon taxes and cap-and-trade systems) actually reduce national CO₂ emissions. Using statistical methods that isolate cause-and-effect relationships, I'll analyze emissions data from 1990 to 2024 across countries with and without carbon pricing.

## Hypothesis and Research Objective

**Primary Hypothesis:** Countries that implement carbon pricing see slower emissions growth compared to countries without these policies, even after accounting for differences in economic development, population, and energy systems.

**Research Objectives:**
- Measure how much carbon pricing reduces emissions in practice
- Calculate how sensitive emissions are to different carbon price levels
- Compare results between wealthy and developing countries

## Why This Matters

Carbon pricing is widely promoted as a key climate solution, but there's ongoing debate about whether it works in the real world. This analysis provides evidence that matters for:
- Policymakers: Understanding which carbon pricing designs actually deliver results
- Investors: Assessing climate policy risk when making ESG investment decisions
- Climate Negotiators: Evaluating market-based approaches under international agreements like the Paris Accord

**Practical Uses:**
- Setting appropriate carbon prices for companies and governments
- Projecting future emissions under different policy scenarios
- Identifying the price level needed to hit specific climate targets

## Data Sources

### Carbon Pricing Policy Data
- [World Bank Carbon Pricing Dashboard](https://carbonpricingdashboard.worldbank.org/) - Tracks which countries have carbon taxes or trading systems, when they started, and price levels
- [Resources for the Future World Carbon Pricing Database](https://www.rff.org/publications/data-tools/world-carbon-pricing-database/) - Details on policy design, exemptions, and how revenues are used
- [Our World in Data Emissions-Weighted Carbon Price](https://ourworldindata.org/grapher/emissions-weighted-carbon-price) - Average carbon prices weighted by how much emissions they cover
- [Carbon Monitor](https://carbonmonitor.org/) - Real-time CO₂ emissions by sector (2019-2024)
- [Kaggle Global CO₂ Emissions Database](https://www.kaggle.com/datasets/patricklford/global-co-emissions) - Historical country-level emissions (1990-2023)

### Economic and Control Variables
- World Bank Development Indicators - GDP, population, energy use, industrial makeup
- OECD Green Growth Indicators - Environmental policy strength, renewable energy adoption

## Data Quality

**Strengths:**
- Multiple independent sources that I can cross-check
- Data collected using consistent methods by trusted international organizations

**Challenges and Solutions:**
- **Different implementation dates across sources:** I'll verify dates by checking government announcements and prioritizing official records
- **Missing data for some countries:** I'll use statistical methods to fill gaps and test whether results hold when excluding imputed data
- **Other policies happening simultaneously:** I'll control for other environmental regulations that might confuse the carbon pricing effect
- **Different emissions accounting methods:** I'll run analyses using both territorial emissions (what's emitted within borders) and consumption-based emissions (including imports/exports)

**What the Data Shows:**
- 47 countries or regions have carbon pricing today
- Prices range from $1 to $150 per ton of CO₂
- Countries with carbon pricing account for about 30% of global emissions
- Plenty of countries without pricing to serve as comparison groups

## Analytical Approach

### 1. Price Sensitivity Analysis

Figuring out how much emissions drop for each dollar increase in carbon price.

**Approach:**
- Use regression models that directly estimate elasticity (percent change in emissions per percent change in price)
- Test whether the effect differs by country income, starting emissions level, or policy type (tax vs. trading system)
- Address the problem that high-polluting countries might be more likely to adopt pricing (which could bias results)

### 2. Timing Analysis

Carbon pricing doesn't work instantly. Technology takes time to change, factories last decades, and people adjust behavior gradually.

**What I'll examine:**
- How emissions respond in years 0, 1, 2, 3, 4, and 5 after implementation
- Create graphs showing the full trajectory of emissions before and after policy adoption
- Identify when the biggest effects show up

### 3. Synthetic Control Method

For early adopters like Sweden or British Columbia, I'll construct a "synthetic twin" by combining other countries that match their pre-policy characteristics.

**Process:**
- Find the weighted combination of non-pricing countries that best matches the treated country before policy
- Compare actual emissions to this synthetic counterfactual after policy
- Cross-check these results against the main difference-in-differences estimates

## Expected Results

This analysis will deliver:
- Estimates of the carbon price level needed to achieve specific reductions
- Insights into which country types see the biggest effects
- Recommendations for improving policy design
- A reusable framework for evaluating other climate policies

## Visualizations

- Global map showing carbon pricing adoption over time (1990-2024)
- Timeline of when each country implemented pricing and at what level
- Line graphs comparing emissions paths for countries with vs. without pricing
- Charts showing estimated effects with uncertainty ranges
- Analysis of how effects vary by carbon price level and country characteristics
- Sector-by-sector breakdowns (power, transport, industry)
