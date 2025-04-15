---
layout: page
title: Bigfoot Visualizations
permalink: /visuals/
---

# 🦶 Bigfoot Sightings Dashboard
Welcome! Below are two visualizations exploring patterns in Bigfoot sightings using data from the BFRO dataset. Each chart is built with Altair and uses visual encodings to make trends easy to understand.


## 1. Sightings by Season

<iframe src="/visuals/plot1.html" width="700" height="400"></iframe>

This visualization displays Bigfoot sightings categorized by season.  
I chose a bar chart to compare frequencies between the four seasons.  
Each bar is color-coded for quick grouping. The chart highlights that most sightings occur in **Fall** and **Summer**, possibly due to increased outdoor activity.
I chose a bar chart to effectively compare the frequency of sightings across the four seasons.
The **x-axis** encodes `season` as a **nominal (categorical)** variable.
The **y-axis** encodes the **count of records** using **quantitative aggregation** (`count()`).
Each bar is also **color-encoded** by season, reinforcing group identity visually.
Encoding used: 
`x = season:N` (nominal)
`y = count():Q` (quantitative aggregate)
`color = season:N` (for visual grouping)

## 2. Interactive Map by Year

<iframe src="/visuals/plot2.html" width="720" height="450"></iframe>

This interactive map lets you explore the **geolocation of Bigfoot sightings** by year.  
Use the dropdown to filter sightings for a specific year. Points are color-coded by season and show detailed info on hover.
Each point represents a sighting with **latitude and longitude** mapped to the chart's spatial projection.
A **dropdown filter** lets you select a year, updating the plot dynamically.
The **color encoding** represents the season, and **tooltips** provide more context (state, county, date, season)
 `longitude = longitude:Q` and `latitude = latitude:Q` (quantitative spatial mapping)
 `color = season:N` (categorical season color)
`tooltip = [state:N, county:N, date:T, season:N]`
`selection_point` filtering for interactivity

