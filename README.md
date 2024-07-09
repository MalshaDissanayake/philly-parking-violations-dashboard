# Philly Parking Violations Dashboard

This repository contains an interactive dashboard created with R, visualizing the number of parking violations and total fines collected each day in 2017 for the city of Philadelphia. The dashboard is built using `flexdashboard` and includes various visualizations to provide insights into parking patterns and enforcement trends.

## Repository Structure

- **`flex_dashboard.Rmd`**: The RMarkdown file containing the code for the dashboard.
- **`output/`**: Directory containing the output HTML file.
  - **`flex_dashboard.html`**: The rendered interactive dashboard.

## Dashboard Overview

### 1. Calendar Heatmap
Visualizes daily fines collected over the year.

### 2. Fines Over Time
Shows the trend of total fines collected over the year.

### 3. Tickets by Day of the Week
Displays the number of tickets issued each day of the week.

### 4. Total Fine Amount by Day of the Week
Shows the total fines collected each day of the week.

### 5. Special Patterns (Currently Commented Out)

```{r}
# Interactive map using plotly
#Please refer the documentation
#library(plotly)

#philly_geo <- philly %>% 
  #filter(!is.na(lat) & !is.na(lon))

#map_plot <- plot_geo(philly_geo, lat = ~lat, lon = ~lon) %>%
  #add_markers(
    #text = ~paste("Violation:", violation_desc, "<br>Fine:", fine),
    #color = ~fine, colors = "red",
    #marker = list(size = 5)
  #) %>%
  #layout(
    #title = 'Philadelphia Parking Violations (2017)',
    #geo = list(
      #scope = 'usa',
      #projection = list(type = 'albers usa'),
      #showland = TRUE,
      #landcolor = toRGB("gray85"),
      #subunitcolor = toRGB("white")
    #)
 # )

#map_plot
```


## How to Run the Dashboard

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/yourusername/philly-parking-violations-dashboard.git
   cd philly-parking-violations-dashboard
   ```

2. **Install Necessary Packages:**
   Ensure you have R and RStudio installed. Open RStudio and install the required packages by running:
   ```r
   install.packages(c("flexdashboard", "tidyverse", "lubridate", "scales", "viridis"))
   ```

3. **Render the Dashboard:**
   Open `flex_dashboard.Rmd` in RStudio and click the `Knit` button to generate the `flex_dashboard.html` file in the `output` directory.

## Data Source

The data used in this dashboard is sourced from the [TidyTuesday project](https://github.com/rfordatascience/tidytuesday). The specific dataset can be found [here](https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2019/2019-12-03/tickets.csv).

## Explanation of Visualizations

### Calendar Heatmap
The calendar heatmap shows the daily fines collected. Each tile represents a day, and the color intensity indicates the amount of fines collected. The visualization helps identify patterns in parking violations throughout the year.

### Fines Over Time
This line chart shows the trend of total fines collected over the year. It helps in understanding the temporal distribution of fines and identifying any spikes or trends.

### Tickets by Day of the Week
This bar plot shows the number of tickets issued each day of the week. It helps in understanding which days have higher parking violations.

### Total Fine Amount by Day of the Week
This bar plot shows the total fines collected each day of the week. It helps in understanding the financial impact of parking violations on different days.
