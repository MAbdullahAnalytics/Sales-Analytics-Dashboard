# Sales-Analytics-Dashboard
🍫 Awesome Chocolates: Sales Analytics Dashboard (Power BI)

An interactive, end-to-end Power BI report analyzing sales, profitability, and shipment behavior for a fictional chocolate company. The project covers the full BI workflow: data modeling, DAX, dashboard design, and publishing.

Portfolio Dashboard

📌 Business Problem

Leadership at Awesome Chocolates needs a single view to answer:

How are sales, costs, and profit trending month over month?
Which salespeople and products are hitting the 60% profit-margin target?
How many shipments are low-box shipments (under 50 boxes, typically samples), and is that share under control?
How do results change by product category and country?
📊 Key Results (Feb 2023 – Feb 2024)
Metric	Value
Total Sales	$34M
Total Profit	$20.5M
Total Cost	$13.5M
Profit Margin	60.3% (target: 60%)
Boxes Shipped	~2M
Shipments	6,113
Low-Box Shipment Rate	10.2% (624 shipments)
✨ Dashboard Features
KPI header cards with month-over-month reference labels and conditional formatting (red/green indicators), plus a profit % gauge against target
Dynamic trend chart driven by a field parameter: one visual switches between Sales, Boxes, Shipments, Cost, and Profit
Shipment distribution histogram built with grouped bins and a zoom slider, paired with a low-box shipment gauge
Salesperson performance table with photos, data bars, and a target-attainment icon indicator (RAG logic via DAX)
Category and geography slicers with custom styling; every visual cross-filters
Custom theme, consistent layout, and a wireframe-first design approach
🧠 Technical Highlights

Data model: star schema with one fact table (Shipments) and four dimensions (Salesperson, Product, Geography, Calendar), a dedicated _Measures table, and a date table marked for time intelligence.

DAX concepts used:

Core measures: Total Sales, Boxes, Shipments, Cost, Profit, Profit %
CALCULATE with filter context for low-box shipment count and percentage
Time intelligence: DATEADD/previous-month logic and month-over-month % change
Variables (VAR) and DIVIDE for safe, readable calculations
"Latest month" measures so KPI cards show correct values at grand-total level
Target logic: parameterized profit target and a 3-tier performance indicator
RELATED for a calculated cost column across tables

Power Query: derived calendar columns (year, month, month name, start of month, weekday) for correct chronological sorting.

Other: field parameters, bookmarks and selection pane, conditional formatting (icons, data bars, background colors), tooltip pages, and publishing to the Power BI Service.
