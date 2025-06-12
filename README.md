# Automotive-Recall-Insights-Trends-Impacts-2000-2025
1. Introduction


This project analyzes automotive recall data from the NHTSA (National Highway Traffic Safety Administration) spanning 2000-2025. The goal is to identify trends, high-risk manufacturers, critical safety issues, and the scale of vehicle impacts in the U.S. automotive industry.

2. Data Description
   

Source: NHTSA recall database (CSV format)

Records: 29,071 recalls after cleaning

Time Span: 1966–2025 (with focus on 2000–2025)

Key Columns:

Manufacturer: Original manufacturer name

Potentially Affected: # of vehicles impacted

Component: Defective part (e.g., air bags, brakes)

Critical_Recall: Flags "Do Not Drive" or "Park Outside" advisories

Issue_Category: Standardized failure categories (e.g., "Battery/Fire Risk")

Vehicle_Type: Car, SUV, Truck, etc.

3. Methodologies

   
Data Cleaning & Transformation
Standardized Manufacturer Names:

Consolidated brands under parent companies (e.g., Chrysler/FCA → Stellantis; Hyundai/Kia → Hyundai-Kia Group).

Example: "Tesla/Rivian" → "EV Startups".

Vehicle Type Classification:

Derived from Subject field using keyword rules (e.g., "SUV" → SUV; "truck" → Truck).

Critical Recall Flag:

Created Critical_Recall (1/0) if "Do Not Drive" or "Park Outside" advisory exists.

Issue Categorization:

Grouped defects into 8 categories (e.g., "Brake System", "Battery/Fire Risk") based on Component and Recall Description.

Missing Data Handling:

Replaced "NR (Not Reported)" in Potentially Affected with NaN.

Filled missing Component with "Other".

Analytical Techniques
Trend Analysis: Annual recall counts and vehicles affected.

Manufacturer Benchmarking: Recalls/vehicles affected by company.

Failure Mode Analysis: Top defect categories and critical risks.

Severity Scoring: Ranked recalls by Critical_Recall + Potentially Affected.

4. Key Results


Overall Insights
Total Recalls: 29,071 (2000–2025)

Vehicles Affected: 1.3 billion

Critical Recalls: 167 (0.57% of total)

Top Manufacturers
Rank	By Recalls	By Vehicles Affected
1	General Motors (1,691)	Ford (214M)
2	Ford (1,590)	GM (204M)
3	Stellantis (1,469)	Stellantis (143M)
Failure Categories
Most Common Issues:

Other (20,622 recalls)

Brake System (2,100)

Safety Restraint (1,523)

Most Critical Risks:

Safety Restraint (34 critical recalls)

Steering (17)

Brake System (13)

Manufacturer-Specific Findings
Ford:

19 critical recalls; worst issue: air bags (e.g., 2016 recall: 1.9M vehicles, fatal fragmentation risk).

Top components: Fuel system (165), Powertrain (155).

General Motors:

4 critical recalls; worst issue: suspension (e.g., 2021 recall: 380k vehicles, loss of control risk).

Dominant vehicle type: "Other" (1,576 recalls).

Stellantis:

3 critical recalls; worst issue: air bags (2015 recall: 385k trucks, fragmentation risk).

Top components: Brakes (171), Powertrain (134).

5. Visualizations


Annual Trends: Recall counts peaked in mid-2010s (e.g., 2014–2016).

Manufacturer Comparison:

Ford/GM led in vehicles affected; Forest River Group had high recall volume but low severity.

Critical Issues: "Safety Restraint" dominated critical recalls (e.g., Takata air bags).

6. Conclusion


Safety Critical Trends: Air bags (especially Takata-related) and suspension defects pose the highest lethality risks.

Manufacturer Risks: Legacy automakers (Ford, GM, Stellantis) have the broadest impact due to scale.

EV Startups: Emerging risks in battery/fire issues (e.g., Rivian recalls).

Data Gaps: Low completion rate reporting (36% missing) limits remediation analysis.
