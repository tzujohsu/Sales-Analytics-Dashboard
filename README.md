# Sales-Analytics-Dashboard

<img src="dashboard.png" width="700">

[Tableau Link](https://public.tableau.com/views/Sales-Dashboard_17384750055410/OverviewDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Milestones: 
* ✅ Sales Performance Overview: Build comprehensive dashboard displaying YoY comparisons for sales, profits, and quantity with monthly trend analysis and dynamic progress bars, including subcategory performance tracking.
* ✅ Customer Segmentation Analysis: Track gender distribution, days-to-first purchase, customer distribution by order frequency and top 10 profit generators, supported by interactive filters for deep-dive analysis.
* ✅ Order Details Management: Create comprehensive order tracking dashboard with Customer Name, Segment, and Sub-category, featuring customizable shipping threshold alerts (red indicators for delays).
* ✅ Detailed filters: Support year range, product category, and regional selections.
* ✅ Deployment & Sharing Publish dashboards to Tableau Public



Issues:
* Parameter Control Threshold: I had a parameter in Tableau called "Days to ship threshold", which is controlled by +/- buttons to increase or decrease its value dynamically. However, clicking them did not update the threshold in my visualization. After troubleshooting, I’ve figured the bug in the calculated field, and I reformated and customized the parameter itself to better suit my needs.
* Dynamic Calculation in Tooltips: When using {[% Diff Sales per Customers]} in tooltips, the values remained static and didn't update with context changes. This occurred because the field reference wasn't properly aggregating at the correct level. The solution was to explicitly use the aggregated version <AGG(% Diff Sales per Customers)> to ensure dynamic updates for Sales Differences calculations.
