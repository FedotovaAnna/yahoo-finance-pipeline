Прогнозування акцій за секторами у Databricks з використанням Prophet
Stock Sector Forecasting in Databricks using Prophet
Опис проекту | Project Description
UA:
Цей проєкт реалізує повний ETL-пайплайн на платформі Databricks за допомогою медальйонної архітектури (Bronze → Silver → Gold) для аналізу та прогнозу цін акцій за секторами. Для прогнозування використовується модель Facebook Prophet.

EN:
This project implements a complete ETL pipeline on Databricks using the medallion architecture (Bronze → Silver → Gold) to analyze and forecast stock prices by sector. Facebook Prophet is used for time series forecasting.

🔧 Основні етапи | Key Pipeline Stages
UA:

📥 Завантаження історичних даних через yfinance (Bronze).

🧹 Очищення та нормалізація даних, додавання секторів (Silver).

📈 Агрегація, прогноз та візуалізація результатів (Gold).

🔁 Автоматизація через Jobs у Databricks.

EN:

📥 Load historical stock data via yfinance (Bronze layer).

🧹 Clean and transform data, including sector tagging (Silver layer).

📈 Aggregate, forecast, and visualize results (Gold layer).

🔁 Automate pipeline execution via Databricks Jobs.

📊 Приклад графіка | Example Visualization
<img src="/files/tmp/gold_forecast_prophet_plot.png" style="max-width:100%; height:auto;">
🛠 Використані технології | Technologies Used
Databricks (Delta Lake, PySpark)

Prophet (forecasting)

yfinance (stock market data)

Pandas, Seaborn, Matplotlib

🗂 Структура проєкту | Project Structure
Файл / File	Опис / Description
01_bronze_load_yfinance.py	UA: Завантаження даних
EN: Load raw data
02_silver_clean_transform.py	UA: Очищення та дод. секторів
EN: Data clean
03_gold_sector_aggregation_with_prophet.py	UA: Прогноз та графік
EN: Forecast & plot
pipeline_logs	UA/EN: Логи виконання пайплайну

🚀 Як запустити | How to Run
UA:

Імпортуйте ноутбуки у Databricks Workspace.

Налаштуйте Job з трьома послідовними етапами.

Переконайтесь, що Prophet встановлено:

perl
Copy
Edit
%pip install prophet
EN:

Import notebooks into Databricks Workspace.

Set up a Job with three sequential tasks.

Make sure Prophet is installed:

perl
Copy
Edit
%pip install prophet
 Майбутні покращення | Future Enhancements
UA: Прогноз по секторам, а не лише по тикерам.

EN: Add sector-level (not just ticker-level) forecasting.

UA/EN: Додати MLflow для моніторингу метрик.

UA/EN: CI/CD та Workflows для повної автоматизації.

