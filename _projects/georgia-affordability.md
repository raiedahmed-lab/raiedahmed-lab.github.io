---
layout: page
title: Mapping water affordability across Georgia
permalink: /research/georgia-affordability/
description: Explore ten socioeconomic indicators across 2,796 Georgia census tracts through an adaptation of GEFA’s affordability criteria.
img: /images/georgia-affordability.svg
importance: 1
status: Mapping project
period: '2026'
methods: SQL Server · QGIS · Census tract analysis
action: Explore the tract map
---

Two neighborhoods in the same county can face very different economic pressures. I adapted the Georgia Environmental Finance Authority’s affordability framework to examine those differences at the census tract level. The map shows where several indicators of socioeconomic disadvantage coincide. It is a starting point for my research on how those conditions relate to the water and wastewater bills households face.

## Explore the map

Hover over a tract to see its ten indicators, or click to keep its profile open. Colors progress from pale yellow for lower scores through orange to burgundy for higher scores. Gray marks the 32 tracts without a final score.

[Open the map in its own tab]({{ '/affordability-map/' | relative_url }}){:target="_blank" rel="noopener"}

<iframe title="Interactive Georgia census tract affordability map" src="{{ '/affordability-map/' | relative_url }}" style="display:block;width:100%;height:clamp(680px,90vh,950px);border:1px solid #cfdcd6;border-radius:8px;" loading="lazy"></iframe>

## How I built the index

1. **Put both years on the same map.** I obtained 2024 ACS five-year estimates through IPUMS NHGIS. To estimate population change, I allocated 2011 block-group populations to the newer tract boundaries using the NHGIS geographic crosswalk, then compared the aligned estimates with 2024 tract populations.
2. **Score ten indicators.** In SQL Server, I calculated statewide tract quartiles for nine measures covering income, employment, poverty, household assistance, and age dependency. Each received 1–4 points, with lower income receiving more points. Population change followed a separate rule. Stable or growing tracts received 1 point, declines up to 1% received 2, declines above 1% through 2% received 3, and larger declines received 4.
3. **Map the combined score.** I summed the ten scores, joined them to tract polygons, and mapped the results in QGIS. A complete score ranges from 10 to 40. I omitted GEFA’s community-size criterion because tract-level water or sewer connection counts were unavailable.

## Reading the pattern

Higher scores appear across parts of central and southern Georgia. Around Atlanta, many tracts have higher incomes and lower scores, although neighboring tracts can differ substantially. Selecting adjacent tracts helps explain those differences. For example, two tracts with similar totals can have different combinations of poverty, population decline, and age dependency.

GEFA explains that it uses its criteria “to score communities for principal forgiveness.” Its published index lists communities and distinguishes scores with and without connections. The estimates here use my recalculated tract thresholds and serve as a research screening measure. They do not establish funding eligibility or measure an individual household’s bill burden. [GEFA 2025 Affordability Criteria](https://gefa.georgia.gov/document/document/2025-affordability-criteria/download) · [GEFA 2026 Affordability Score Index](https://gefa.georgia.gov/document/document/2026-affordability-score-index/download)

## How this connects to affordability research

Teodoro (2018) measures the cost of essential water and sewer service against the income a lower-income household has left after essential expenses. Cardoso and Wichman (2022) show why measuring burden across the income distribution matters: a median-income benchmark can conceal households struggling to pay. Those studies motivate my next question: where do high utility bills coincide with the vulnerabilities visible on this map?

- Teodoro, M. P. (2018). [Measuring Household Affordability for Water and Sewer Utilities](https://doi.org/10.5942/jawwa.2018.110.0002). *Journal AWWA*.
- Cardoso, D. S., and Wichman, C. J. (2022). [Water Affordability in the United States](https://doi.org/10.1029/2022WR032206). *Water Resources Research*.
- Schroeder et al. (2026). [IPUMS National Historical Geographic Information System, Version 21.0](https://doi.org/10.18128/D050.V21.0). ACS estimates and geographic crosswalk.
- [Project tract data (CSV)](https://github.com/raiedahmed-lab/raiedahmed-lab.github.io/blob/main/_projects/affordability/tract2024_mastertable.csv) · [2024 Census tract boundaries for Georgia](https://www2.census.gov/geo/tiger/TIGER2024/TRACT/tl_2024_13_tract.zip)
