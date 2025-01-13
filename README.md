# Optimizing Solar Panel Placement in Uganda: A Linear Programming Approach to Achieve Electrification Goals
Linear Optimization with Gurobi to position Solar Panels across district to support the Ugandan Electrical Transformation Plan (ETP)

## Introduction
Access to electricity is fundamental for economic development, health, social equality, environment, job creation, and quality of life. In Uganda, 80% of the population does not have access to electricity, mainly due to the limited reach of the network in rural areas. This has led to a rise in micro-grids and individual solar home systems for tasks such as crop irrigation for farmers. 

Building on this success, the project aims to further decentralize solar energy production so that communities can access a reliable local power source. Increasing solar generation in Uganda can catalyze better healthcare (through vaccine refrigeration and reliable hospital power), higher school enrollment (lighting for evening classes and studying), and economic growth (local businesses and irrigation). It also reduces reliance on bioenergy—benefiting both public health and the environment.

By investing in robust solar infrastructure, Uganda and its partners can bridge the rural-urban divide in energy access. Our aim is to guide government bodies, NGOs, social businesses, and international development agencies in making more informed, data-driven decisions on solar infrastructure.

## Placement Plan
By employing optimization techniques and spatial analysis tools, we have identified where solar panels will yield the most impact at the lowest cost. This article outlines how a Linear Programming model using Gurobi, combined with ArcGIS mapping, supports strategic solar deployment to meet Uganda’s ambitious electrification targets.

To help achieve this, we developed an optimization model that provides:
- Location-based recommendations for installing solar panels
- Cost estimations that factor in both installation and transportation
- Energy distribution analysis to ensure supply meets demand with minimal transmission losses

## Methods: Data Analytics for Sustainable Development

### Data Collection and ArcGIS
We began by gathering geospatial data on Uganda’s districts from publicly available sources. Using ArcGIS, we mapped relevant information such as average solar potential, population density, and existing grid connectivity. ArcGIS also helped us create a distance matrix between district centroids to accurately estimate transport costs and potential energy losses over distance.

### Dataset Description
1. **Solar Potential Data:**
   - Derived from Global Solar Atlas (1994-2018).
2. **Electricity Demand Data:**
   - Population-based demand estimates from Uganda’s Bureau of Statistics.
3. **Geospatial Information:**
   - District-level maps of Uganda including transmission lines and protected areas.

### Linear Programming Methodology with Gurobi
Next, we built a Linear Programming model in Python using the Gurobi solver. The model’s objective function minimizes the total cost of solar installations (fixed costs plus distance-dependent transport costs). 

#### Key constraints include:
1. Meeting local demand in each district (5% in grid-connected and 80% in unconnected districts).
2. Energy transfer between districts connected to the grid.
3. Accounting for transmission losses.
4. Limiting surplus production to avoid overbuilding.
5. Staying within budget.

### Methodology

1. **Exploratory Data Analysis (EDA):**
   - Analyzed Uganda’s solar potential, population, and energy demand distributions.

2. **Optimization Model:**
   - **Objective Functions:**
     - Maximize energy production.
     - Minimize total costs (installation + transportation).

3. **Constraints:**
   - Meeting local demand in each district (5% in grid-connected and 80% in unconnected districts).
   - Energy transfer between districts connected to the grid.
   - Accounting for transmission losses.
   - Limiting surplus production to avoid overbuilding.
   - Staying within budget.

4. **Implementation:**
   - Developed using Python and the Gurobi optimization library.

5. **Validation and Visualization:**
   - Visualized panel distribution, installed capacity, and energy flows.

## Results, Conclusions, and Recommendations

### Results
- **Total cost for the project:** $3,517,563,807.09 (3.5 Billion)
- **Total number of panels installed:** 65,130
- **Total power output achieved:** 2930.85 MW

This 5-year deployment strategy covers the needs of all districts modeled under realistic budget constraints, bringing Uganda closer to its 2030 goal.

### Conclusions
1. **Feasibility:** Even at large scale, data-driven planning allows for efficient and cost-effective solar deployment.
2. **Scalability:** Our approach can easily incorporate new data, such as biodiversity constraints or varying transport costs, ensuring the model remains adaptable over time.
3. **Collaboration:** Continued input from local experts is vital to keep assumptions (like solar panel costs or transmission loss rates) current and accurate.

### Recommendations
Uganda’s Ministry of Energy and Mineral Development, with support from the International Energy Agency (IEA), has created an Energy Transition Plan (ETP) to provide universal access to modern energy and support the economic transformation sustainably and securely.

- **Protect Sensitive Ecosystems:** Refine the model to exclude national parks and other protected lands.
- **Dynamic Costing:** Develop more granular cost matrices based on local labor, logistics, or partnerships.
- **Implementation Timeline:** Prioritize high-demand districts first, then scale to remote areas, ensuring that the highest-impact installations occur early.
- **Socioeconomic Indexing:** Incorporate metrics like poverty rates or healthcare deficits to ensure energy reaches the most vulnerable communities first.

**Article written by Félix Veaux**  

