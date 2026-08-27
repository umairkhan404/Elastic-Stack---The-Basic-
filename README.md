# Elastic-Stack---The-Basic-
Understand how SOC analysts use the elastic stack (ELK) for log investigations.

# 🔍 Elastic Stack (ELK) - SOC Log Investigation

Understand how SOC analysts use the Elastic Stack (ELK) for real-world log analysis, threat detection, and security investigations.

---

## 📊 Dashboard Overview

Below dashboards show how logs are visualized inside Kibana:

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

<img src="https://github.com/user-attachments/assets/45b28b42-6286-4d82-b595-fa14ed52d9a4" />

<img width="1739" height="673" alt="image" src="https://github.com/user-attachments/assets/fbebeff4-4606-4c35-a153-3d57f8e4daae" />

<img src="https://github.com/user-attachments/assets/14f67648-5b19-4219-8c2a-9a741b11d765" />

---

## 🔎 KQL (Kibana Query Language)

KQL is used by SOC analysts to search and filter logs efficiently inside Kibana.

We can search logs in two ways:

- 🔹 Free-text search  
- 🔹 Field-based search  

---

### 🧪  Free-text search
 <img width="1739" height="673" alt="image" src="https://github.com/user-attachments/assets/23491f0d-451e-4792-af37-0f0773cfe18d" />


👉 This returns all logs containing the phrase **United States**

---

### 🧪  Wildcard search
<img width="1633" height="630" alt="image 1" src="https://github.com/user-attachments/assets/e0be803b-4e0b-4381-9d24-37ed2aa0dad3" />

👉 This returns all values starting with “United”  
(e.g. United States, United Kingdom)

---

## ⚙️ Logical Operators in KQL

SOC analysts use logical operators to refine search results.

---

### 🔹 AND Operator
<img width="1634" height="627" alt="image 4" src="https://github.com/user-attachments/assets/724b9bfe-2c9d-4249-b1f3-800643b37d30" />


👉 Shows logs that contain **both values**

---

### 🔹 OR Operator
<img width="1741" height="730" alt="image 3" src="https://github.com/user-attachments/assets/0dea6dd4-9f90-4751-9029-ce209a81a02d" />


👉 Shows logs that contain **either value**

---

### 🔹 NOT Operator
<img width="1634" height="627" alt="image 4" src="https://github.com/user-attachments/assets/d025ce47-ae50-42b1-9f40-4553854640c3" />


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

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

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


