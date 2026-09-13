NYC Yellow Taxi 2024: Full Year Analysis & Insights
A comprehensive data analysis of 39.2 million NYC Yellow Taxi trips from 2024, uncovering demand patterns, revenue trends, and operational insights using Python and advanced data processing techniques.

Executive Summary
This project analyzes 39.2 million taxi trips generating $1.12 billion in revenue throughout 2024. Using memory-efficient batch processing techniques, I processed 5.5GB of data to identify peak demand patterns, revenue optimization opportunities, and operational insights for NYC's taxi industry.
Key Metrics at a Glance
Metric
Value
Total Trips
39,212,507
Total Revenue
$1,123,958,804
Total Tips
$132,847,603
Average Fare
$19.79
Average Distance
3.43 miles
Average Duration
16.9 minutes
Average Speed
10.9 mph
Average Tip %
19.1%
Key Findings
1. Seasonal Patterns
Busiest Month: October with 3.65M trips ($107.2M revenue)
Highest Revenue Month: October at $107,160,984
Slowest Month: February with 2.87M trips
Peak Season: September-October shows 15% increase over winter months
2. Daily Demand Patterns
Busiest Day: Thursday with 6.14M trips
Peak Hour: 6:00 PM (2.79M trips across the year)
Rush Hour Impact: Evening rush (5-7 PM) accounts for 18% of daily trips
Weekend vs Weekday: Weekdays show 23% higher volume
3. Financial Insights
Revenue Growth: 38% increase from February ($78.1M) to October ($107.2M)
Fare Trends: Average fare increased from $18.43 (Feb) to $20.47 (Dec)
Tip Behavior: Credit card users tip 19.1% on average
Revenue per Mile: $5.77 average across all trips
4. Operational Efficiency
Average Speed: 10.9 mph (indicating heavy traffic conditions)
Trip Duration: 16.9 minutes average
Distance Distribution: 68% of trips under 5 miles
Peak Efficiency: Early morning hours (4-6 AM) show 40% faster speeds

Business Recommendations
1. Dynamic Pricing Strategy
Implement surge pricing during October peak season
Adjust rates during 6 PM rush hour to maximize revenue
Consider premium pricing for Thursday evening commutes
2. Driver Resource Allocation
Increase driver availability during 5-7 PM window
Focus recruitment efforts for September-October peak season
Optimize Thursday scheduling for maximum coverage
3. Revenue Optimization
Target credit card adoption (higher tip rates)
Promote longer-distance trips during off-peak hours
Implement incentives for high-demand time slots
4. Operational Improvements
Route optimization during peak hours (current avg speed: 10.9 mph)
Focus on short-distance efficiency (68% of trips < 5 miles)
Reduce average trip duration through better routing
🛠️ Technologies Used
Python 3.9+ - Core programming language
Pandas - Data manipulation and analysis
NumPy - Numerical computations
Matplotlib - Data visualization
Seaborn - Statistical visualizations
Jupyter Notebook - Interactive development environment
Git/GitHub - Version control

Project Structure
NYC-Yellow-Taxi-2024-Analysis/
├── README.md
├── requirements.txt
├── .gitignore
├── 01_Data Profiling and Cleaning.ipynb
├── 2024 Analysis.ipynb
├── results/
│   ├── nyc_taxi_2024_monthly_summary.csv
│   ├── nyc_taxi_2024_hourly_summary.csv
│   ├── nyc_taxi_2024_dow_summary.csv
│   └── nyc_taxi_2024_payment_summary.csv
└── visualizations/
    ├── monthly_trends.png
    ├── hourly_patterns.png
    ├── dow_analysis.png
    └── payment_analysis.png

Data Source
Dataset: NYC Yellow Taxi Trip Records (2024)
Source: NYC Taxi & Limousine Commission (TLC)
Size: 39.2 million trips, 5.5GB
Format: Parquet files (monthly)
Time Period: January 1, 2024 - December 31, 2024
Data Dictionary
Column
Description
tpep_pickup_datetime
Trip start date and time
tpep_dropoff_datetime
Trip end date and time
passenger_count
Number of passengers in the vehicle
trip_distance
Trip distance in miles
fare_amount
Base fare amount in dollars
tip_amount
Tip amount in dollars
total_amount
Total amount charged to passengers
payment_type
Payment method (1=Credit card, 2=Cash, etc.)

How to Reproduce This Analysis
Prerequisites
# Clone the repository
git clone https://github.com/Wyclife5X4/NYC-Yellow-Taxi-2024-Full-Year-Analysis-Insights.git
cd NYC-Yellow-Taxi-2024-Full-Year-Analysis-Insights

# Install required packages
pip install -r requirements.txt
Steps
Download Data
Visit NYC TLC Trip Record Data
Download all 12 months of 2024 Yellow Taxi data (Parquet format)
Place files in your working directory
Run Analysis
Open 2024 Analysis.ipynb in Jupyter Notebook
Run all cells sequentially
Visualizations will be generated automatically
View Results
Summary statistics saved in results/ folder
Visualizations saved as PNG files
Note
Raw data files (5.5GB total) are not included in this repository due to GitHub size limitations. Download them separately from the NYC TLC website.

Methodology
Data Processing Pipeline
Data Acquisition
Downloaded 12 monthly Parquet files from NYC TLC
Total dataset: 41M rows before cleaning
Data Cleaning
Removed 88,752 erroneous timestamps (dates outside 2024)
Handled 4M+ missing values using domain-appropriate imputation
Applied quality filters (fare > $0, distance > 0, duration 1-180 min)
Final dataset: 39.2M trips (95.5% retention rate)
Feature Engineering
Extracted temporal features (hour, day, month, day of week)
Calculated derived metrics (speed, tip percentage, revenue per mile)
Created categorical groupings (weekend/weekday, peak/off-peak)
Analysis Approach
Month-by-month batch processing to handle memory constraints
Aggregated statistics across temporal dimensions
Statistical analysis of patterns and trends
Optimization Techniques
Memory-efficient processing (one month at a time)
Garbage collection after each batch
Aggregated results storage (not raw data)

Detailed Monthly Breakdown
Month
Trips
Revenue
Avg Fare
Growth vs Previous
Jan
2,836,874
$77.6M
$18.50
-
Feb
2,866,510
$78.1M
$18.43
+1.0%
Mar
3,398,906
$94.8M
$19.18
+18.6%
Apr
3,373,782
$95.2M
$19.48
+0.4%
May
3,576,039
$103.8M
$20.17
+9.0%
Jun
3,391,658
$97.4M
$19.97
-6.2%
Jul
2,944,057
$85.4M
$20.17
-12.3%
Aug
2,840,244
$83.0M
$20.38
-2.8%
Sep
3,453,015
$101.9M
$20.67
+22.7%
Oct
3,645,466
$107.2M
$20.37
+5.2%
Nov
3,480,414
$99.2M
$19.75
-7.5%
Dec
3,405,542
$100.4M
$20.47
+1.2%

Skills Demonstrated
Data Analysis: Large-scale dataset analysis (39M+ records)
Data Cleaning: Handling missing values, outliers, and data quality issues
Feature Engineering: Creating meaningful derived metrics
Statistical Analysis: Temporal pattern recognition and trend analysis
Data Visualization: Creating clear, informative charts
Python Programming: Pandas, NumPy, Matplotlib, Seaborn
Memory Management: Efficient processing of large datasets
Version Control: Git and GitHub workflow
Documentation: Clear, professional project documentation
Future Enhancements
 Geographic analysis using pickup/dropoff location data
 Predictive modeling for demand forecasting
 Weather data integration for impact analysis
 Interactive dashboard using Plotly/Dash
 Machine learning for fare prediction
 Real-time streaming data analysis
 Comparison with previous years (2022-2023)

Wyclife Ayako
GitHub: @Wyclife5X4
LinkedIn: Connect with me (https://www.linkedin.com/in/wyclife-ayako-9bbb512b5/)

Acknowledgments
NYC Taxi & Limousine Commission for providing open data
Python data science community for excellent libraries
Stack Overflow community for troubleshooting support
