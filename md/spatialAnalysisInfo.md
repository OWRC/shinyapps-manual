---
title: Spatial Analysis
output: html_document
---




## 5-day Antecedent Precipitation

The cumulative 5-day precipitation $(P_5)$ is used to determine the Antecedent Moisture Condition (AMC) base on the following 3 tiers:

1. **Wet** -- $P_5 > 27\text{ mm}$
1. **Dry** -- $P_5 < 12\text{ mm}$
1. **Normal** -- Otherwise


## Latest/current Streamflow

For stations reporting data within the last 7 days, the latest reported streamflow value $Q_l$ is compared to the statistical distribution of historical measurements at the gauge.

1. **Wet** -- $Q_l > Q_{P84}$
1. **Dry** -- $Q_l < Q_{P16}$
1. **Normal** -- Otherwise

where $Q_{Pn}$ is the $n^\text{th}$ percentile flow.