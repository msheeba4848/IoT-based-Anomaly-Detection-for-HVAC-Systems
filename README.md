# IoT-based-Anomaly-Detection-for-HVAC-Systems

Steps done

1. created env 
2. created requirements.txt

Basic Idea;

1. Having Iot Data
Tools: Python, Faker, NumPy, CSV/JSON.
Write a Python script (data_simulator.py) 
Save the generated data to CSV or JSON files locally (e.g., data/raw/).
1. Data Ingestion
Tools: Python, File I/O.
Create a script (data_ingestion.py) to:
Read raw data from data/raw/.
Perform basic validation (e.g., check for missing values or incorrect formats).
Save the validated data to a local database (e.g., SQLite or PostgreSQL).
1. Data Storage
Tools: SQLite or PostgreSQL.
Set up a local SQLite database (boiler_data.db).
Create tables for raw data, transformed data, and summary metrics.
Use Python libraries like sqlite3 or SQLAlchemy to interact with the database.
1. Data Transformation
Tools: Python, Pandas, PySpark (optional).
Write a script (data_transformation.py) to:
Aggregate hourly metrics (e.g., average temperature, total power consumption).
Identify anomalies in data using threshold-based logic or a simple statistical model.
Save transformed data to the database.
1. Data Processing and Automation
Tools: Prefect, Python.
Use Prefect to orchestrate the pipeline:
Schedule tasks like data ingestion, transformation, and anomaly detection.
Create a Prefect flow (pipeline.py) to link all tasks.
1. Data Visualization
Tools: Streamlit, Matplotlib, or Dash.
Build a Streamlit app (dashboard.py) to:
Display real-time and historical trends in temperature, pressure, and power consumption.
Highlight detected faults and anomalies.
Use Python libraries like Matplotlib or Plotly for graphs and charts.
1. Anomaly Detection
Tools: scikit-learn, NumPy.
Train a simple machine learning model (e.g., Isolation Forest, k-Means) to detect anomalies.
Save the model using joblib and use it in the pipeline for real-time fault detection.
1. Documentation
Tools: Markdown, GitHub.
Document your project in a README.md file:
Describe the setup, project structure, and how to run each component.
Include diagrams for your pipeline architecture.