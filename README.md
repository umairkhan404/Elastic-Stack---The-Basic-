# Elastic-Stack---The-Basic-
Understand how SOC analysts use the elastic stack (ELK) for log investigations.

# 🔍 Elastic Stack (ELK) - SOC Log Investigation

Understand how SOC analysts use the Elastic Stack (ELK) for real-world log analysis, threat detection, and security investigations.

---

## 📊 Dashboard Overview

Below dashboards show how logs are visualized inside Kibana:

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

<img src="https://github.com/user-attachments/assets/45b28b42-6286-4d82-b595-fa14ed52d9a4" />

<img src="https://github.com/user-attachments/assets/932f0cb8-3cac-4f7e-a338-5486e7f2ab2b" />

<img src="https://github.com/user-attachments/assets/14f67648-5b19-4219-8c2a-9a741b11d765" />

---

## 🔎 KQL (Kibana Query Language)

KQL is used by SOC analysts to search and filter logs efficiently inside Kibana.

We can search logs in two ways:

- 🔹 Free-text search  
- 🔹 Field-based search  

---

### 🧪 Example 1: Free-text search


👉 This returns all logs containing the phrase **United States**

---

### 🧪 Example 2: Wildcard search


👉 This returns all values starting with “United”  
(e.g. United States, United Kingdom)

---

## ⚙️ Logical Operators in KQL

SOC analysts use logical operators to refine search results.

---

### 🔹 AND Operator


👉 Shows logs that contain **both values**

---

### 🔹 OR Operator


👉 Shows logs that contain **either value**

---

### 🔹 NOT Operator


👉 Shows logs from United States but **excludes Florida**

---

## 🧠 Field-Based Query Example


📌 This query filters logs where:
- Source IP matches attacker/host IP
- Username matches specific user

---

## 🎥 Log Investigation Demo (GIF Explained)

Below GIF shows a **real SOC workflow inside Kibana Discover tab**:

<img src="https://github.com/user-attachments/assets/ebbe6449-2826-47c7-b64c-15c3f9816b9f" />

### 🧠 What is happening in this GIF?

✔ Logs are being searched inside Kibana  
✔ SOC analyst is filtering events using KQL  
✔ Relevant events are being isolated from large datasets  
✔ Suspicious activity patterns are identified  

👉 Basically, this shows how SOC analysts move from **raw logs → filtered insights → investigation**

---

## 📈 Creating Visualizations

### 🚨 Failed VPN Login Attempts

SOC analysts often visualize failed login attempts to detect:

- brute force attacks  
- suspicious access patterns  
- unauthorized access attempts  

---

### 🔧 Setup details:

- Data View: `vpn_connections`  
- Time Range: January 2022  
- Filter: `action: failed`  
- Fields used: `UserName`, `Source_ip`  

---

### 🎥 Visualization GIF (Explained)

<img src="https://cdn-images.tryhackme.com/user-uploads/5e8dd9a4a45e18443162feab/room-content/93e9aebb89efb58df9ab5a52eeb0177c.gif" />

### 🧠 What this GIF shows:

✔ Creating a visualization in Kibana  
✔ Filtering failed VPN login attempts  
✔ Building a table/chart from raw logs  
✔ Turning logs into actionable security insights  

👉 This is how SOC analysts convert **logs → visual threat detection dashboards**

---

# 🚀 Conclusion

This lab demonstrates core SOC analyst skills:

✔ Searching logs using KQL  
✔ Filtering suspicious activity  
✔ Investigating authentication events  
✔ Creating visual dashboards  
✔ Turning raw logs into security insights  

---

💡 **Key takeaway:**  
Elastic Stack helps SOC analysts detect threats faster by making huge log data searchable and visual.


