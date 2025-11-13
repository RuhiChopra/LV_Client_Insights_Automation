# LV Client Insights Automation Project

## Overview
This project is a Python-based automation tool designed for Louis Vuitton's Client Insights & CRM team. It demonstrates skills in Python scripting, SQL querying, data analysis with pandas, and report generation with Excel (using openpyxl) and visualizations (using Matplotlib). The script automates the process of analyzing mock client purchase data to provide CRM insights, such as RFM (Recency, Frequency, Monetary) segmentation for identifying high-value customers.

Key features:
- Generates synthetic LV client data mimicking luxury retail purchases.
- Stores data in a local SQLite database and queries it for high-value clients.
- Performs RFM analysis to segment clients (e.g., 'Champions', 'Loyal', 'Standard').
- Outputs an enhanced Excel report with tables, bar charts, pie charts, and a scatter plot for visual insights.

This project addresses common CRM challenges like manual task automation and dashboard creation.

## Skills Demonstrated
- **Python Automation**: End-to-end scripting for data generation, processing, and reporting.
- **SQL**: Data storage and querying with SQLite (e.g., aggregation, filtering).
- **Data Analysis**: RFM scoring using pandas.
- **Excel Reporting**: Formatted sheets with charts via openpyxl.
- **Visualizations**: Embedded charts (bar, pie) and Matplotlib scatter plots for insightful dashboards.

## Prerequisites
- Python 3.x
- Required libraries: Install via pip
  ```
  pip install pandas openpyxl matplotlib
  ```
- No external data needed—uses mock data.

## How to Run
1. Save the script as `lv_client_insights_automation.py`.
2. Run it in your terminal:
   ```
   python lv_client_insights_automation.py
   ```
3. Outputs:
   - `lv_clients.db`: SQLite database with raw mock data.
   - `lv_client_report.xlsx`: Excel report with:
     - **Client Insights** sheet: Detailed table of high-value clients with RFM scores.
     - **Summary** sheet: Aggregated stats by segment, plus visuals:
       - Bar chart: Total Spend by Segment.
       - Pie chart: Client Distribution by Segment.
       - Scatter plot: Recency vs. Monetary Value (colored by RFM Score).
   - Temporary file: `rfm_scatter.png` (embedded in Excel).

Example console output:
```
Generating mock LV client data...
Setting up SQL DB and querying...
Performing RFM analysis...
Generating Excel report with enhanced visuals...
Report generated: lv_client_report.xlsx
Automation complete! Open 'lv_client_report.xlsx' in Microsoft Excel to view tables and visuals.
```

## Project Structure
- `lv_client_insights_automation.py`: Main script with functions for data generation, SQL operations, RFM analysis, and report creation.
- (Generated) `lv_client_report.xlsx`: Sample output report.
- (Generated) `lv_clients.db`: Sample database.

## Customization
- **Adjust Mock Data**: Modify `generate_mock_data` (e.g., increase `num_records` or add categories).
- **SQL Query Tweaks**: Change thresholds in the query (e.g., spend > 2000, last 90 days).
- **Add Features**: Extend with email notifications (smtplib) or interactive dashboards (Streamlit—install via `pip install streamlit` and add a function).
- **Real Data Integration**: Replace mock data with actual CRM exports (e.g., CSV import) or connect to production databases (e.g., PostgreSQL via psycopg2).

## Relevance to Client Insights & CRM
It directly tackles dashboard/report creation and task automation using Python, SQL, and Excel. By automating RFM segmentation, it can help identify clients for targeted campaigns, reducing manual Excel work and enabling quicker insights.

## Limitations
- Mock data is random; results vary per run.
- Visuals require Microsoft Excel for full rendering (Google Sheets may alter charts).
- For production, secure real data handling and scale with larger datasets.
