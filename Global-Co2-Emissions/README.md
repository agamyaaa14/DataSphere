# Global CO2 Emissions Analysis

![Project Badge](img/global5.png)

This guided project explores and visualizes global CO2 emissions data, focusing on the largest contributors and the trends between emissions and country populations. The analysis is performed through data profiling, visualization, and the creation of an interactive dashboard using Tableau.

## Objective 1: Profile & QA the Data

**Tasks**:
1. **Connect to the Dataset**: The dataset, `visualizing_global_co2_data.csv`, is used to analyze global CO2 emissions by country.
2. **Data Profiling**:
   - Identify countries that are the largest contributors of CO2 emissions.
   - Exclude records with NULL ISO Codes and convert CO2-related fields to numerical data types (continuous measures).
3. **Parameter Creation**: A new parameter called **Top N** is created to display the top 10 CO2 contributors by default.

## Objective 2: Visualize the Data

**Tasks**:
1. **Line Chart**: Show the percentage of total CO2 emissions by year for the top 10 countries using the **Top N** parameter.
2. **Map Visualization**: Create a country-level map to show CO2 emissions per capita for the year 2021, resolving country/region issues and removing null value countries.
3. **Scatter Plot**: Compare CO2 emissions and population at the country level, with bubbles sized by temperature change from CO2 emissions. A linear regression trend line is added.
4. **Color Scheme**: Apply a divergent color scale based on CO2 per capita for all visualizations.

## Objective 3: Build an Interactive Dashboard

**Tasks**:
1. **Dashboard Creation**: Combine the visualizations (line chart, map, and scatter plot) into a cohesive dashboard, including the **Top N** parameter and a country filter for interactivity.
2. **Design & Layout**: Format and polish the dashboard with a custom layout, title, and filters.
3. **Interactive Features**: Add a country filter to apply across all visualizations, providing users with dynamic insights.

## Tableau Dashboard

Explore the interactive dashboard on [Tableau Public](https://public.tableau.com/app/profile/agamya.david2913/viz/CO2GlobalEmissions_17294405039010/Dashboard1).  

## Project Files

The project folders/files required for this analysis are organized as follows:
- **files**: Contains the datasets `visualizing_global_co2_data.csv`.
- **img**: Contains the project completion badge and screenshots of key insights.

## Insights and Patterns

During the analysis, several interesting patterns and trends emerged regarding CO2 emissions by country, population impacts, and temperature changes due to emissions. The dashboard provides a comprehensive view of these trends, allowing for interactive exploration.
