---
title: R-Shiny apps
subtitle: General description
author: M.Marchildon
output: html_document
---

* TOC
{:toc}

# Introduction

The Oak Ridges Moraine Groundwater Program (ORMGP) hosts an [R-Shiny](https://shiny.rstudio.com/) server from which users are provided an interactive interface to time-series analysis of data queried directly from our central database.

sHydrology is a set of dynamic hydrological analyses packages written to improve access to environmental monitoring databases through a variety of workflows, statistics and perspectives.

# Philosophy

The sHydrology web application provides a collection of analytical tools written to improve workflow at the ORMGP. These tools were scripted in R to replace our past/inefficient practice of quering data, cleaning/infilling data, re-formatting data, analysing and plotting data, output figures and tables every time we need to provide figure for reporting. While these tools can be found on [ORMGP web site](https://www.oakridgeswater.ca/), and the source code is [open and free](https://github.com/maseology/sHydrology), we are not developing an application for distribution and support, rather we are exposing our internal workflows to our parteners. 

# Intent

The sHydrology web packages originated from a set of scripts I had created over the years, mostly written in Basic. Recently I had begun to convert these scripts to R as it became apparent to me that the R community has so much to offer for comprehensive time series analysis. I work as a hydrolgist whose interest is in long term hydrology at the regional (>10,000\ km$^2$) scale

# Goal

In a series of pages, this will guide users on the many means of analysis included with sHydrology.



# Versions

1. **sHydrology** -- designed to analyse long term daily average stream flow data.
1. **shyMet** -- designed to analyse long term daily average climate data.
1. **sHdrograph** -- a general platform for timeseries analysis, used specifically for groundater monitoring.



# Timeseries

The initial page that appears when opening a sHydrology page is the raw data. This is the most important page because off the bat, not only can one gain an appreciation for the period of record and the data quality, but the general character of the hydrograph can be inspected with a trained eye. 

The side bar (to the left of the page) offers some information on the station, such as station name, catchment area (where available), period of record, data quality and simple statistics. Options provided below allow the user to superimpose observation flags for additional quality assessment.

This timeseries is plotted using [dygraphs for R](https://rstudio.github.io/dygraphs/), which offers a dynamic means of zooming, scrolling and inspecting the time series. (Double-click anywhere returns to the default view.)

Upon changing the dygraph pane, the flow duration curve, monthly discharge and side panel information are updated automatically. This feature allows the user to examine the flow regieme within a specifed time period and compare against the entire period of record.

### Baseflow separation

A common request of me from the groundwater community is an estimate of baseflow computed using automated hydrgraph separation techniques. [Fourteen variants of hydrgraph separation algorithms](https://owrc.github.io/interpolants/modelling/hydrographseparation.html) are applied. (sHydrology relies on the median of daily estimates from these 14 variants.)

### Hydrograph dissaggregation

This is a process of analysing a continuous time series signal to identify rising limbs, falling limbs and recession periods. From this, additional inforamtion can be backed-out of the continous data set by discretizing the hydrograph into discrete volumes associted with each peak. This allows the user to compare these "event yeilds" to local precipitation monitoring stations and inspect the quality of the basin's monitoring network.


## Long term trend analysis

The next section of the...


# Current Apps

[sHydrology "Analysis" — stream flow analysis tools](legacy/sHydrologyAnalysis.html)