# Football Analytics Blitz

**Optimizing Kickoff Strategy and Injury Prevention**

A data-driven analysis of NFL kickoff strategy and player injury trends across the 2021–2024 seasons, with a focus on the impact of the 2024 Dynamic Kickoff rule change.

**Authors:** Brady Detwiler, Jonah Lubin, Lucca Ferraz, Savan Patel — Rice University

---

## Contents

| File | Description |
|------|-------------|
| `Blitz_Analytics_Presentation-2.pdf` | Full slide deck with all analysis and visualizations |

---

## Overview

This project was submitted to the Football Analytics Blitz competition and covers two major areas:

### Kickoff Strategies
- Year-over-year trends in touchback %, EPA, return %, and ending field position from 2021–2024
- 2024 deep dive into landing zone vs. end zone kicks, and the effect of returning from each
- Statistical significance testing (t-test, Kolmogorov-Smirnov) confirming meaningful distributional shifts in return outcomes

### Injury Prevention
- Injury trends by type (player contact, ground contact, non-contact) across seasons
- Injury rate on returns — 2024 recorded the lowest rate in the four-season window
- Predictive modeling using XGBoost to identify top injury predictors: hang time, return yards, and kick yards
- Field surface analysis — matrixturf notably reduced ground-contact injuries; surface type is otherwise a weak predictor

---

## Key Findings

**Kickoff Strategy**
- The 2024 Dynamic Kickoff rule brought touchback % from ~75% (2023) back down to ~65.5%
- Return % from the end zone surged 53.8% from 2023 to 2024
- Kicking into the end zone is strategically superior in the first 3 quarters, regardless of score
- Returners perform worse when taking the ball out of the end zone versus receiving from the landing zone

**Injury Prevention**
- 2024 had the lowest injury rate on returns (0.063) and the fewest non-return injuries by a wide margin
- Year-over-year injury differences are not statistically significant (ANOVA, Kruskal-Wallis)
- Hang time and return yards are the strongest predictors of injury severity

---

## Recommendations

**Optimal Kickoff Strategy**
1. Kicking teams should almost always kick into the end zone
2. Returning teams should attempt a return when the ball lands in the landing zone, but not from the end zone
3. When losing late in the game, returning is almost always the best option

**Rule Change Verdict**
- Keep the kick return: it's exciting and injury data does not justify eliminating it
- The Dynamic Kickoff has effectively eliminated unnecessary non-return injuries
- Further study warranted on the relationship between hang time and injury severity

---

## Data Sources

- NFL play-by-play data via nflfastR
- Injury and surface data from NFL tracking datasets
