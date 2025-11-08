# 📊 Azure Data Explorer

**Azure Data Explorer (ADX)** is a fast, fully managed data analytics service for real-time analysis of large volumes of data streaming from applications, websites, IoT devices, and more.

---

## 🧩 What Does It Do?

- Ingests and stores massive amounts of structured, semi-structured, and unstructured data.
- Enables fast, ad-hoc querying using Kusto Query Language (KQL).
- Supports time-series analysis, log analytics, telemetry, and monitoring scenarios.
- Scales to handle billions of events per day.

---

## 🛠 Key Features

- **High-speed ingestion**: Supports batch and streaming data sources.
- **Kusto Query Language (KQL)**: Powerful query language for analytics and visualization.
- **Integration**: Works with Azure Monitor, Log Analytics, Power BI, and other Azure services.
- **Data visualization**: Built-in dashboards and export to Power BI.
- **Security**: Role-based access control, managed identities, and encryption.

---

## 🔗 Integration

- Can be used as a data platform for Azure Monitor and Log Analytics.
- Integrates with Event Hub, IoT Hub, Azure Data Factory, and Power BI.
- Supports ingestion from CSV, JSON, Avro, Parquet, and other formats.

---

## 🔍 Querying & Analysis

- Use **KQL** for filtering, aggregating, and visualizing data.
- Supports advanced analytics: time-series, anomaly detection, machine learning integration.
- Example query:
  ```kql
  StormEvents
  | where State == "TEXAS"
  | summarize EventCount = count() by EventType
  ```

---

## 💰 Pricing

- Charged based on cluster size, data ingestion, and storage.
- Pricing details: [Azure Data Explorer Pricing](https://azure.microsoft.com/pricing/details/data-explorer/)

---

## 🧠 Exam Tips

- Know how ADX integrates with Azure Monitor and Log Analytics.
- Be familiar with KQL basics and query optimization.
- Understand ingestion methods and supported data formats.
- Know security and access control options.

---

## 📚 Reference

- [Azure Data Explorer documentation](https://learn.microsoft.com/azure/data-explorer/)
