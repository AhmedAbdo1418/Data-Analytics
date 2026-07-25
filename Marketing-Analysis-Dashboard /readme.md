📊 Digital Marketing & E-Commerce Performance Dashboard
An end-to-end Business Intelligence & Marketing Analytics Solution built using Power BI and DAX. This project models end-to-end digital campaign operations, multi-channel performance, product line transactions, and customer purchase behaviors to deliver executive-level profitability insights and channel-level optimization strategies.

<img width="997" height="619" alt="Dashboard Screenshot" src="https://github.com/user-attachments/assets/c7a8703a-d84f-456b-a5f1-4ce2a68faacc" />




📌 Executive Summary
Modern e-commerce and digital marketing operations generate massive volumes of disparate transactional and operational data across paid ad channels, customer touchpoints, and product SKUs.

This project bridges the gap between raw data and strategic action by creating a consolidated, star-schema relational data model and an interactive Power BI dashboard. It empowers business leaders to track ROI, CAC, conversion efficiency, and product sales in real time, while pinpointing low-performing campaigns to eliminate ad spend waste.

🛠️ Tech Stack & Tools Used
Business Intelligence Tool: Power BI Desktop

Data Modeling: Star Schema (Fact/Dimension Relationships, 1:Many Single Direction Filters)

Analytical Language: Data Analysis Expressions (DAX)

Custom Styling & UX: Dynamic DAX Visual Formatting (HTML/CSS-driven dynamic borders)

Source Control & Documentation: Git, GitHub

🏗️ Data Architecture & Star-Schema Modeling
To ensure optimal query performance, quick visualization rendering, and clean DAX calculations, the underlying dataset was structured into a robust Star Schema:

                  ┌───────────────────────┐
                  │      Dim_Calendar     │
                  └───────────┬───────────┘
                              │ 1
                              │
                              │ *
┌──────────────────────┐  * ┌─┴───────────────────────┐ *   ┌──────────────────────┐
│     Dim_Campaigns    ├────┤  Fact_Marketing_Sales  ├─────┤     Dim_Products     │
└──────────────────────┘ 1  └─┬──────────────────────┘ 1   └──────────────────────┘
                              │ *
                              │
                              │ 1
                  ┌───────────┴───────────┐
                  │      Dim_Customer     │
                  └───────────────────────┘



Key Tables & Schema Roles:
Fact_Marketing_Sales: Contains core transactional granular data (Impressions, Clicks, Conversions, Revenue, Ad Spend, Quantities Sold, Unit Costs).

Dim_Campaigns: Attributes for ad platforms (Google, Meta, TikTok), campaign types, and targeted demographics.

Dim_Products: Product hierarchy, SKU definitions, category classifications, and standard selling prices.

Dim_Calendar: Dedicated custom date dimension supporting time-intelligence logic.

Measures Table: A dedicated container table isolating all calculated KPIs for clean workspace organization.

🧮 Hand-Crafted DAX Measures & Analytics Logic
All measures were explicitly written in DAX to maintain accuracy, scalability, and transparency across visual elements.

1. Revenue & Financial Performance
Total Revenue:


Total Revenue = SUM(Fact_Marketing_Sales[Revenue])
Total Budget / Ad Spend:


Total Budget = SUM(Fact_Marketing_Sales[Ad_Spend])
Profit:

Profit = [Total Revenue] - [Total Budget]
Average ROI:


Average ROI = 
DIVIDE(
    [Profit],
    [Total Budget],
    0
)
2. Marketing Unit Economics & Conversion Efficiency
Cost Per Click (CPC):


CPC = 
DIVIDE(
    [Total Budget],
    [Total Clicks],
    0
)
Cost Per Result / Conversion (CPR):


CPR = 
DIVIDE(
    [Total Budget],
    [Total Conversions],
    0
)
Conversion Rate (CR):

Conversion Rate (CR) = 
DIVIDE(
    [Total Conversions],
    [Total Clicks],
    0
)
Revenue Per Click (RPC):


Revenue Per Click(RPC) = 
DIVIDE(
    [Total Revenue],
    [Total Clicks],
    0
)
Revenue Per Conversion (RPR):


Revenue Per Conversion(RPR) = 
DIVIDE(
    [Total Revenue],
    [Total Conversions],
    0
)
3. Volume & Operational Metrics
Total Clicks: Total Clicks = SUM(Fact_Marketing_Sales[Clicks])

Total Conversions: Total Conversions = SUM(Fact_Marketing_Sales[Conversions])

Total Units Sold: Total Units Sold = SUM(Fact_Marketing_Sales[Units_Sold])

Number Of Campaigns: Num Of Campaigns = DISTINCTCOUNT(Fact_Marketing_Sales[Campaign_ID])

4. Advanced UI/UX Styling via DAX Dynamic Formatting
To elevate user interactivity without impairing report performance, custom DAX measures were designed to feed dynamic conditional borders into target container visuals:

Animated Border: Custom DAX calculation driving color gradients based on selected KPIs.

Moving Neon Purple Border: Dynamic DAX expression returning conditional color hex codes to highlight active KPI cards and focused slicer selections.

🎨 Dashboard Design & User Experience (UX)
The user interface was built adhering to strict visualization standards:

F-Pattern Visual Layout: Strategic placement of high-level KPI cards along the top, followed by breakdown charts in the center, and granular data tables at the bottom.

Cross-Filtering & Drill-Throughs: Interactive cross-filtering enabled across all visuals to facilitate exploratory analysis by Campaign, Channel, and SKU.

Dynamic Slicers: Date-range sliders, channel selectors, and product category dropdowns for quick context filtering.

Visual Hierarchy: Customized tooltips, clean typography, and neon-highlighted dynamic borders to guide executive visual flow.

💼 Key Business Insights Answered
This analytics platform explicitly answers four critical operational questions:

Optimized Marketing Spend: Identifies highest and lowest performing channels and campaigns to maximize Return on Ad Spend (ROAS) and eliminate wasted marketing budgets.

Customer Retention & Churn Signals: Tracks customer purchasing frequencies and churn indicators early, enabling retention teams to trigger targeted re-engagement campaigns.

Product & Operational Insights: Highlights top-performing SKUs and product combinations to optimize inventory planning and drive cross-selling strategies.

Executive-Ready Visibility: Supplies executive leadership with an immediate, real-time breakdown of net profitability, operational efficiency, and revenue growth drivers.

📁 Repository Structure

Data-Analytics
├── Images/
│   ├── Dashboard Screenshot.png
│   └── Marketing Dashboard Video.mp4
├── Data/
│   └── marketing_and_product_performance.csv
├── src/
│   └── Marketing_Performance_Dashboard.pbix
└── README.md

🚀 How to Run & Inspect This Project
Clone the Repository:

Bash
git clone https://github.com/YourUsername/Digital-Marketing-PowerBI-Dashboard.git
Download Microsoft Power BI Desktop (if not already installed).

Open the Report: Navigate to src/ and open Marketing_Performance_Dashboard.pbix.

Explore: Interact with the dashboard visuals, inspect the data model in Model View, and review explicit calculations in the Data/DAX View.

👨‍💻 Author

Ahmed Abdo Shahin
Data Analyst & Operations Specialist

LinkedIn: http://www.linkedin.com/in/ahmed-abdo-shahin

Email: AhmedAbdo1418@gmail.com

