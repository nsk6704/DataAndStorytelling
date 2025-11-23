# **Homework 1.1 — Sports Analytics Industry**

## **1. Industry Chosen: Sports Analytics**

Modern sports teams, broadcasters, and performance labs rely heavily on both structured and unstructured data to improve player performance, broadcasting quality, fan experience, and strategic decision-making.

## **2. Examples of Data Types in Sports Analytics**

### **Structured Data (Highly organized, tabular)**

* **Match statistics** such as runs, goals, passes completed, speed, distance covered, ball possession percentage, player fitness metrics (heart rate, sprint count).
  **Example:** A player-tracking table with columns: Player_ID, Speed, Acceleration, Distance Covered.

### **Unstructured Data (Non-tabular, variable format)**

* **Video streams** from multiple cameras (4K match footage, drone angles, stump cam).
* **Audio data** (crowd noise, umpire microphones).
* **Social media posts** expressing fan sentiment.

**Example:** A 90-minute match video from 20 different camera angles.

## **3. How Each Type of Data Is Stored and Processed**

### **Structured Data**

Stored using:

* **Relational databases** (MySQL, PostgreSQL) for match stats.
* **Data warehouses** for long-term analytics (Snowflake, BigQuery).
* **Time-series databases** (InfluxDB) for player biometric data.

Processed using:

* SQL queries
* BI dashboards (Tableau, Power BI)
* Statistical models (regression, clustering)

### **Unstructured Data**

Stored in:

* **Data lakes** (Hadoop HDFS, AWS S3, Azure Blob)
* **Distributed storage** for large video archives

Processed using:

* **Computer vision models** (pose estimation, player tracking)
* **Natural language processing** for commentary and fan sentiment
* **Deep learning** for automatic highlights generation

## **4. Engineering Challenges in Integrating Both Data Types**

* **High volume storage:** Multiple 4K video feeds + sensor data require petabyte-scale systems.
* **High velocity:** Real-time tracking data must update in milliseconds for live broadcasts.
* **Synchronization:** Aligning structured player stats with unstructured video frames is complex.
* **Data quality issues:** Inconsistent sensor readings, occluded players, noisy audio.
* **Scalability:** Balancing compute for peak match times vs idle periods.
* **Latency:** Delivering real-time insights (speed, xG, trajectory) during live games.

## **5. Technologies / Algorithms / Architectures Used**

### **Databases & Storage**

* **SQL databases:** PostgreSQL, MySQL
* **NoSQL databases:** MongoDB, Cassandra
* **Data lakes:** Hadoop, AWS S3

### **Big Data & Distributed Systems**

* **Apache Spark** for large-scale processing
* **Hadoop** for storing and batch processing match archives

### **AI / ML Algorithms**

* **Computer vision:** YOLO, OpenPose, DeepSORT for player tracking
* **Time-series models:** LSTMs, ARIMA for performance prediction
* **NLP:** Sentiment analysis on fan posts
* **Clustering:** Identify player styles, fitness patterns

### **Architectures**

* Lambda architecture for combining real-time + batch analytics
* Microservices for scalable match insights
* Edge computing (stadium-level capture + processing)
