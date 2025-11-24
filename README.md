# Walmart-Sales-Forecasting-Dashboard
Power BI dashboard analyzing Walmart weekly sales with forecasting, DAX measures, KPIs, trends, and store-level insights.
Walmart Sales & Forecasting Dashboard | Power BI

This project analyzes Walmart Weekly Sales using Power BI.
It includes KPIs, trend analysis, store-wise performance, forecasting, and DAX calculations for real-time insights.


---

⭐ Dashboard Features

📌 Key KPIs

Total Sales

Average Weekly Sales

Total Holiday Sales

12-Week Forecasted Sales


📊 Visuals Included

Weekly sales trend (line chart)

Holiday vs non-holiday sales

Sales by Store

Highest & Lowest sales by month

Temperature vs Weekly Sales

Fuel Price vs Weekly Sales

Unemployment impact

Multiple slicers (Store, Year, Month)



---

🧮 DAX Measures Used

Total Sales = SUM(Walmart[Weekly_Sales])

Average Sales = AVERAGE(Walmart[Weekly_Sales])

Holiday Sales = CALCULATE(SUM(Walmart[Weekly_Sales]), Walmart[Holiday_Flag] = 1)

GrowthRate =
VAR PrevYearSales =
    CALCULATE(SUM(Walmart[Weekly_Sales]), DATEADD(Walmart[Date], -365, DAY))
VAR CurrYearSales =
    SUM(Walmart[Weekly_Sales])
RETURN DIVIDE(CurrYearSales - PrevYearSales, PrevYearSales)

Forecast_12_Weeks =
[Total Sales] * (1 + [GrowthRate]) ^ 12


---

📚 Dataset Source

Kaggle – Walmart Weekly Sales Forecasting Dataset


---

🛠️ Tools Used

Power BI

DAX

Data Modeling

CSV Dataset

Time Intelligence



---

👤 Author

Kislaynath Tiwari
🔗 GitHub: https://github.com/Kislaynath
🔗 LinkedIn: 
https://www.linkedin.com/in/kislay-tiwari-ba436838b

---