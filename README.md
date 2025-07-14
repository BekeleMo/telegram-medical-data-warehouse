10 Academy: AI Mastery - Week 7 Challenge
Project: Ethiopian Medical Business Data Warehouse
Duration: July 09 – July 15, 2025

Summary
This project involves developing a data warehouse system for Ethiopian medical business data extracted from Telegram channels. It includes data scraping, cleaning, transformation using DBT, image analysis with YOLO, and API deployment with FastAPI. The final system provides a scalable solution for structured analysis and public access to insights.

Business Context
Kara Solutions, a data science company, seeks a centralized system to collect and analyze medical business data from Telegram. The warehouse will enable trend analysis and informed decision-making for clients.

Main Tasks
Data Collection: Scrape text and image data from relevant Telegram channels.

Data Preparation: Clean and transform the raw data for analysis.

Object Detection: Apply YOLO to detect objects in collected images.

Warehouse Setup: Design and implement a data warehouse to store processed data.

Data Integration: Enhance and organize the data in structured formats.

API Development: Use FastAPI to expose the data through a RESTful interface.

Deliverables
Task 1: Data Scraping
Goal: Extract data from Telegram channels.

Use telethon to connect to public medical-related channels like DoctorsET, lobelia4cosmetics, and others.

Download both textual data and images.

Store raw content temporarily.

Log and monitor scraping activities for debugging and tracking.

Task 2: Data Cleaning & Transformation
Goal: Clean and shape data for warehouse ingestion.

Remove duplicates, fill or remove missing values, standardize formats.

Store cleaned data in a database (e.g., PostgreSQL).

Use DBT to define data models and create fact/dimension tables.

Commands include:

bash
Copy
Edit
dbt run
dbt test
dbt docs serve
Maintain logs to ensure pipeline transparency.

Task 3: Object Detection with YOLO
Goal: Analyze images for object identification.

Install YOLO (e.g., YOLOv5 via PyTorch).

Load and process images to detect relevant objects.

Example usage:

python
Copy
Edit
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')
results = model('path/to/image.jpg')
results.save()
Save results (e.g., bounding boxes, labels) to the database.

Enable error tracking and logging.

Task 4: FastAPI Interface
Goal: Provide programmatic access to the processed data.

Set up FastAPI with uvicorn, sqlalchemy, and a PostgreSQL driver.

Project structure:

pgsql
Copy
Edit
├── main.py
├── database.py
├── models.py
├── schemas.py
└── crud.py
Run the API:

bash
Copy
Edit
uvicorn main:app --reload

## Conclusion:

This project successfully demonstrates the end-to-end process of building a data warehouse solution for a real-world business need. By combining data scraping techniques, data cleaning and transformation methodologies using DBT, object detection with YOLO, and a robust data warehouse architecture, this project delivers a valuable tool for analyzing Ethiopian medical business data. The exposed API using FastAPI further enhances accessibility and utility, enabling Kara Solutions and their clients to efficiently query and utilize the collected insights. The key takeaway is the ability to leverage modern data engineering and AI techniques to transform raw, unstructured data into actionable intelligence, ultimately driving better decision-making within the Ethiopian medical business sector. Future work can focus on improving the accuracy of object detection, expanding the data sources, and refining the API to offer more sophisticated analytical capabilities.
