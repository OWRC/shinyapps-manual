---
title: sHydrology
subtitle: A suite of R-Shiny apps built to analyse hydrological time-series data 
output: html_document
---

* TOC
{:toc}

# Introduction

The Oak Ridges Moraine Groundwater Program (ORMGP) hosts an [R-Shiny](https://shiny.rstudio.com/) server from which users are provided an interactive interface to time-series analysis of data queried directly from the ORMGP central database.
sHydrology is a set of dynamic hydrological analyses (e.g. workflows, statistics) packages written to improve access to the ORMGP database and more specifically, the long term environmental monitoring data it holds.


# Philosophy 

The sHydrology web application provides a collection of analytical tools written to improve workflow at the ORMGP. These tools were scripted in R to facilitate and perhaps replace some earlier inefficient practices, including the querying data, cleaning/infilling data, re-formatting data, analysing and plotting data, and outputing figures and tables. While these tools can be found on the [ORMGP web site](https://www.oakridgeswater.ca/), and the source code is [open and free](https://github.com/OWRC/sHydrology), we are not developing an application for distribution and support, rather we are exposing our internal workflows to our partners.

# Intent

The sHydrology web packages originated from a set of scripts created by Mason Marchildon over the years, mostly written in Basic. Recently these scripts have been converted to R as it became apparent that the R community has a wealth of support to offer for comprehensive time series analysis. 


# Goal

The series of pages found here are designed to guide users on the many ways of analysing hydrology related data with sHydrology.


# Tools

1. [**sHydrology**](https://github.com/OWRC/sHydrology) -- a web-map interface used to inspect ORMGP-maintained time series data.
1. [**sHyStreamflow**](https://github.com/OWRC/sHyStreamflow) -- designed to analyse long term daily average stream flow data.
2. **sHyClimate** -- designed to analyse long term daily average climate data.
3. **sHydrograph** -- a general platform for time-series analysis, used specifically for groundwater monitoring.


# Time-series

The initial page that appears when opening a sHyStreamflow/sHyClimate/sHydrograph page is the raw data. This is the most important page because off the bat, not only can one gain an appreciation for the period of record and the data quality, but the general character of the hydrograph can be inspected with a trained eye.

The side bar (to the left of the page) offers some information on the station, such as station name, catchment area (where available), period of record, data quality and simple statistics. Options provided below allow the user to superimpose observation flags for additional quality assessment.

This time-series is plotted using [dygraphs for R](https://rstudio.github.io/dygraphs/), which offers a dynamic means of zooming, scrolling and inspecting the time series data. (Double-click anywhere returns to the default view.)

Upon changing the dygraph pane, the flow duration curve, monthly discharge and side panel information are updated automatically. This feature allows the user to examine the flow regime within a specified time period and compare against the entire period of record.


## sHyStreamflow

### Baseflow separation

A common request from the groundwater community is for an estimate of baseflow computed using automated hydrograph separation techniques. /info/hydrographseparation have been applied on the ORMGP website. (sHydrology relies on the median of daily estimates from these 14 variants.)

### Streamflow recession

A significant understanding of stream behaviour is determined by the recession coefficient $(k)$ which is determined automatically for any streamflow time-series.


### Hydrograph disaggregation

A process of analysing a continuous time series dataset to identify rising limbs, falling limbs and recession periods is revealed when users switch over to the disaggregation plot. From here, additional information can be backed-out of the continuous data set by discretizing the hydrograph into discrete volumes associated with each peak. This allows the user to compare these "event yields" to local precipitation monitoring stations and inspect the reliability of the stream’s watershed-wide monitoring network.


<!-- ## Long term trend analysis

The next section of the... -->


<!-- # Current Apps

[sHydrology "Analysis" — stream flow analysis tools](legacy/sHydrologyAnalysis.html) -->