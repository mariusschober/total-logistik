# Logistics Software ROI Calculator Project
## 1. Project Overview
This project consists of a series of interactive Return on Investment (ROI) calculators built with HTML. The primary goal of these tools is to provide a transparent and data-driven analysis of the financial benefits of implementing the software Total Logistik GmbH, a European platform designed to automate the manual tasks of freight dispatchers.

The calculators are designed for freight forwarding companies and logistics operators to model potential cost savings, productivity gains, and break-even points based on their specific operational data.

This repository contains several versions of the calculator, each developed iteratively to offer different levels of flexibility and user input.

## 2. Core Calculation Logic & Assumptions
Transparency is the core principle of this calculator. All calculations are derived from the user's inputs and a clear set of hard-coded assumptions.

**User-Configurable Inputs:**
- Hourly Employer Cost (€): The fully-loaded hourly cost for a single dispatcher, including gross wage, social security, insurance, and all other ancillary labor costs.
- Number of Dispatchers: The total number of employees who would be using the software.
- Shipments per Day (per Dispatcher): The average number of shipments one dispatcher processes in a single working day.
- Manual Time per Shipment (minutes): The total time it currently takes for a dispatcher to manually process one shipment from start to finish. This is a critical input for modeling the "As-Is" state.
- Working Days per Month: The average number of operational days in a month.
- Freight Exchanges: A selection of specific freight exchanges the user's company is integrated with.

**Fixed (Hard-Coded) Assumptions:**
Automation Efficiency: 85%. This is the foundational assumption of the calculator. It posits that the software automates or streamlines tasks to such an extent that it reduces the Manual Time per Shipment by 85%. The remaining 15% of the time is assumed to be for tasks requiring human oversight or exception handling. This is an experiential value from internal process improvement analysis from pre and post API implementation.

Software Pricing Model:
- Platform Base Fee: €50 per month. This is a fixed flat fee for using the platform.
- Cost per Dispatcher: €25 per month. A per-user license fee.
- Cost per Freight Exchange: €25 per month. A fee for each freight exchange integration selected by the user.

Calculation Breakdown:
1. Time Saved per Shipment (minutes) = Manual Time per Shipment * Automation Efficiency (0.85)
2. Cost Savings per Shipment (€) = (Hourly Employer Cost / 60) * Time Saved per Shipment (minutes)
3. Total Monthly Software Cost (€) = Base Fee + (Number of Dispatchers * Cost per Dispatcher) + (Number of Selected Exchanges * Cost per Exchange)
4. Total Monthly Labor Savings (€) = Cost Savings per Shipment * Shipments per Day * Working Days per Month * Number of Dispatchers
5. Net Monthly Savings (€) = Total Monthly Labor Savings - Total Monthly Software Cost
6. Break-Even Point (Shipments) = Total Monthly Software Cost / Cost Savings per Shipment
7. Workforce Equivalence (FTEs) = Number of Dispatchers * (1 - Automation Efficiency)

This metric calculates how many Full-Time Equivalents (FTEs) would be required to handle the same workload with the software's productivity gains. For example, 10 dispatchers might be able to achieve the output of what previously required more, or conversely, the same 10 dispatchers can handle a vastly larger volume of shipments. The calculator simplifies this to show the theoretical number of people needed to perform the new, reduced amount of manual work.

# 3. Project Files & Versions
This repository contains multiple HTML files, representing different stages of the calculator's development:

**index.html**: The first complete version. It uses a dropdown menu to select a country, which then looks up a hard-coded hourly labor cost.

# 4. How to Use
1. Download any of the .html files from this repository or visit https://mariusschober.github.io/total-logistik/
2. Open the file directly in a modern web browser (e.g., Chrome, Firefox, Edge).
3. The calculator is fully interactive. Adjust the values in the "Configuration" panel on the left.
4. The results on the right will update in real-time to reflect your changes.

# 5. Disclaimer
**This is a financial modeling tool intended for demonstrative purposes only. The assumptions, particularly the 85% automation efficiency, are generalized and may not reflect the specific conditions of every organization! The calculated ROI and savings are directly dependent on the accuracy of the data you provide. For a precise and binding offer, please contact the software provider Total Logistik GmbH directly.**
