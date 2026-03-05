# 🌐 Strategic Logistics Optimizer: Saintgits Campus Hub Selection

![Python](https://img.shields.io/badge/python-3.12-blue.svg)
![Optimization](https://img.shields.io/badge/Optimization-PuLP-green.svg)
![Map](https://img.shields.io/badge/Visualization-Folium-orange.svg)

## 📌 Project Overview
This project addresses a **Facility Location-Allocation Problem** for the **Saintgits College of Engineering** campus in Pathamuttom, Kottayam. Using **Mixed-Integer Linear Programming (MILP)**, the system identifies the most cost-effective warehouse hubs to support campus facilities (Hostels, Medical Centers, and Academic Blocks).

The model balances fixed infrastructure costs (construction and daily operations) against variable transportation costs based on real geospatial coordinates in Kerala.

## 🛠️ Tech Stack
* **Language:** Python 3.12
* **Optimization Library:** `PuLP` (COIN-OR CBC Solver)
* **Data Processing:** `Pandas`, `NumPy`
* **GIS Visualization:** `Folium`

## 📊 Mathematical Model
The goal is to minimize the **Total Annual System Cost** ($Z$):

$$Z = \sum_{i \in W} (\text{FixedCost}_i \cdot y_i) + \sum_{i \in W} \sum_{j \in F} (\text{UnitCost}_{ij} \cdot x_{ij})$$

**Subject to:**
1. **Demand Satisfaction:** $\sum_{i \in W} x_{ij} = \text{Demand}_j, \forall j \in F$
2. **Capacity Constraint:** $\sum_{j \in F} x_{ij} \le \text{Capacity}_i \cdot y_i, \forall i \in W$
3. **Policy Constraint:** $\sum_{i \in W} y_i = 2$ (Exactly two hubs must be active).



## 📂 Repository Contents
| File | Description |
| :--- | :--- |
| `Saintgits_Optimizer.ipynb` | Main Python script containing the PuLP model and Folium map logic. |
| `facilities.csv` | Data for Saintgits campus nodes (Lat/Lon and Demand). |
| `warehouses.csv` | Data for candidate hubs (Changanassery, Kottayam, etc.). |
| `transportation_costs.csv` | Unit cost matrix between all hubs and facilities. |

## 🚀 Usage Instructions
1. **Clone the Repo:**
   ```bash
   git clone [https://github.com/Angelin-ak/Micro_project1_Campus-City-Emergency-Supply-Distribution.git](https://github.com/Angelin-ak/Micro_project1_Campus-City-Emergency-Supply-Distribution.git)
