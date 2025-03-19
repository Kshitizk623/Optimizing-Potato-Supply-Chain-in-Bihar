# Optimizing Potato Supply Chain in Bihar: A Data-Driven Analysis of Cold Storage Utilization and Transport Costs

## Project Overview
This project aims to optimize the potato supply chain in Bihar by analyzing cold storage utilization and transportation costs. Using a computational model based on linear programming, the study identifies surplus and shortfall districts and optimizes storage allocation while maximizing profit.

## Abstract
The project focuses on addressing inefficiencies in Bihar's cold storage supply chain for potatoes. It optimizes storage allocation across 22 districts, considering transportation and storage constraints. The key findings include:
- Significant economic returns from high-performing districts like Supaul and Madhubani.
- Identification of inefficiencies in districts with high unutilized storage capacity (e.g., Sitamarhi and Kishanganj).
- A proposed reinforcement learning approach for adaptive improvements.

## Data Sources
1. **Cold Storage Data of Bihar**: Information on 237 cold storages (public and private) and their capacities.
2. **Potato Production Data (2022-2023)**: District-wise area, production, and yield statistics.
3. **Wholesale Price Data (2022-2024)**: District-wise price trends for three years.
4. **Geodesic Distance Data**: Distance calculations between districts using OpenCage API.

## Methodology
1. **Data Collection & Cleaning**: Used Pandas library to preprocess data.
2. **Exploratory Data Analysis (EDA)**: Analyzed cold storage, production, and price trends.
3. **Cold Storage Sufficiency Analysis**: Compared district-wise production with available storage capacity.
4. **Optimization Model**: Implemented linear programming using PuLP to allocate storage optimally.
5. **Profit Calculation**: Incorporated transport costs and potato prices to determine profitability.

## Optimization Model
- **Model 1 (Strict Constraints)**: Allocated storage for 18 out of 22 shortfall districts.
- **Model 2 (Relaxed Constraints)**: Allocated storage for 13 out of 22 shortfall districts but resulted in higher profit.

### Key Constraints:
- Storage availability in surplus districts.
- Transport distances and costs.
- Wastage percentage during transportation.

## Results & Findings
- **Total Profit**:
  - Model 1: ₹248,103,738.40
  - Model 2: ₹297,888,748.96
- **Storage Utilization**: Model 2 achieved better utilization (23.56%) compared to Model 1 (21.43%).
- **Allocation Efficiency**: Districts like Madhubani and Munger had high allocation percentages (~85%), while Sitamarhi and Kishanganj had significant unallocated space (>90%).

## Limitations & Future Scope
- **Static Parameters**: Current model does not account for real-time variations in demand and infrastructure conditions.
- **Low Allocation Efficiency**: Certain districts remain underutilized due to transport constraints.
- **Proposed Enhancements**:
  - Dynamic parameters such as transport conditions and turnover rates.
  - Reinforcement learning to refine model predictions over time.
  - Prioritization of nearby storage centers with penalties for long-distance transport.

## Data & Code Repository
- **Cold storage data of Bihar**: [Link](https://agriexchange.apeda.gov.in/Ready%20Reckoner/Cold_Storage/EasternRegion/Bihar.aspx)
- **Potato price data (2022-2024)**: [Link](https://agmarknet.ceda.ashoka.edu.in/home/download)
- **Potato production data (2022-2023)**: [Link](https://aps.dac.gov.in/APY/Public_Report1.aspx)
- **Code and Analysis Results**: [Google Drive](https://drive.google.com/drive/folders/1BrNrcL59oISIbJZhZH1uwwZzTzX58NNl?usp=sharing)
- **Freight Calculator**: [KisanSabha](https://kisansabha.in/FreightCalculator.aspx)

## How to Use the Code
1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd <repo_folder>
   ```
2. Install required dependencies:
   ```bash
   pip install pandas pulp requests
   ```
3. Run the optimization model:
   ```bash
   python optimize.py
   ```
4. View results in the output directory.



