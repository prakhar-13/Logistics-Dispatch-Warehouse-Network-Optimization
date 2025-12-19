# Logistics-Dispatch-Warehouse-Network-Optimization
A Data-Driven Approach to Heatmapping Dispatches, Identifying Warehouse Hubs &amp; Evaluating Lane Efficiency
# Project Overview

This project analyzes trip-level logistics data for XYZ Company to answer two key business questions:

Where are my orders getting dispatched from, and where should I place warehouses (Network Design) to minimize transportation cost?

Which shipping lanes are most cost-efficient, and what optimizations can be suggested?

Using city-level shipment, cost, mileage, and revenue data, this project uses geospatial analysis and clustering to recommend optimal warehouse locations and identify high-efficiency lanes.

## Key Features
 #### 1. Dispatch Heat Map

A city-wise and state-wise heatmap showing:

Shipments

Total miles

Total cost

Revenue

Helps visualize dispatch intensity and geographical demand patterns.

#### 2. Mapbox Geospatial Visualization

Each origin city is geocoded using GeoPy (Nominatim)

A scatter mapbox plot highlights:

Dispatch hotspots

Cost intensity

Shipment volume

 #### 3. Warehouse Hub Recommendation (Network Design)

Using K-Means clustering on standardized variables:

Shipments

Total miles

Total cost

Revenue

The algorithm identifies:

Optimal warehouse hubs (closest to cluster centroids)

Cities that minimize intra-cluster distances → lower overall transportation costs.

#### 4. Lane Efficiency Analysis

For each Origin → Destination pair:

Cost per mile

Average miles

Total shipments

A horizontal bar chart of the most cost-efficient lanes

This helps identify:

Profitable lanes

High-cost lanes that may need renegotiation or consolidation

Possible multimodal or route optimization opportunities

### Tech Stack & Libraries

Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-Learn, GeoPy

### Project Workflow
#### Step 1: Data Loading & Cleaning

Load Excel file

Remove unnecessary columns

Compute city-level aggregation

#### Step 2: EDA & Visualization

Bar charts for shipments, cost, miles, revenue

Heatmaps for state/city patterns

#### Step 3: Geocoding

Map each OriginCity to latitude and longitude

Create interactive dispatch density map

#### Step 4: Clustering for Warehouse Suggestions

Scale features using StandardScaler

Determine cluster count with Elbow Method

Identify warehouse hub cities

#### Step 5: Lane-Level Cost Optimization

Compute cost per mile

Identify efficient lanes

Visualize top cost-efficient shipping lanes

### Insights Delivered
#### 1. Dispatch Concentration Zones

Heatmaps show where demand is high and where logistics activity is concentrated.

#### 2. Optimal Warehouse Locations

K-Means clustering suggests ideal central cities within each cluster to reduce mileage and cost.

#### 3. Cost-Efficient Shipping Lanes

Identifies lanes with:

Lower cost-per-mile

High shipment volumes

Opportunities for consolidation

#### 4. Potential Optimization Suggestions

Place warehouses closer to cluster centroids

Increase volume on cost-efficient lanes

Renegotiate contracts or explore alternate routing on high-cost lanes

Consider multimodal options for cost-heavy corridors

## [PowerBI Dashboard](https://app.powerbi.com/groups/me/reports/14fec0b8-ca11-469f-9c28-40e9ea6e27c1/115554f31d00c0a871a1?experience=power-bi)
