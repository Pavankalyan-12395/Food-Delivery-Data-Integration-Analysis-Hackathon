# Food Delivery Data Integration & Analysis Hackathon

## 📌 Project Overview
This project involves building a unified data pipeline to merge fragmented data from three different sources (CSV, JSON, and SQL) into a single "Source of Truth" for a food delivery platform. 

The final dataset was used to analyze order trends, user behavior, and revenue distribution across different cities and memberships.

## 📁 Data Sources
- **orders.csv**: Transactional data containing `order_id`, `user_id`, `restaurant_id`, and `total_amount`.
- **users.json**: User master data including `city` and `membership` (Gold vs. Regular).
- **restaurants.sql**: Restaurant master data containing `cuisine` and `rating` information.

## 🛠️ Technical Workflow (ETL)
1. **Extraction**: Loaded data from CSV and JSON using Pandas. Used `sqlite3` to parse and extract the SQL master data.
2. **Transformation**: 
    - Performed a **Left Join** to ensure no order data was lost.
    - Linked orders to users via `user_id`.
    - Linked orders to restaurants via `restaurant_id`.
3. **Loading**: Exported the consolidated data into `final_food_delivery_dataset.csv`.



## 📊 Key Insights
- **Top Revenue City (Gold Members):** Chennai.
- **High-Value Cuisine:** Mexican cuisine maintains the highest Average Order Value (AOV).
- **Membership Impact:** Gold members account for approximately 50% of total order volume.
- **Peak Performance:** Revenue peaks during Q3 (July–September).

## 🚀 How to Run
1. Clone this repository.
2. Ensure you have `pandas` and `sqlite3` installed.
3. Run the `assessment.ipynb` notebook to regenerate the final dataset and analysis.
