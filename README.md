# Elastic-Stack---The-Basic-
Understand how SOC analysts use the elastic stack (ELK) for log investigations.

# 🔍 Elastic Stack (ELK) - SOC Basics

Understand how SOC analysts use the Elastic Stack (ELK) for log investigation.

---

## 📊 Dashboard Overview

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

<img src="https://github.com/user-attachments/assets/45b28b42-6286-4d82-b595-fa14ed52d9a4" />

<img src="https://github.com/user-attachments/assets/932f0cb8-3cac-4f7e-a338-5486e7f2ab2b" />

<img src="https://github.com/user-attachments/assets/14f67648-5b19-4219-8c2a-9a741b11d765" />

---

## 🔎 KQL (Kibana Query Language)

With KQL, we can search logs in two ways:
- Free-text search
- Field-based search

---

### 🔹 Field-Based Search

**Query:**
```
"United States"
```

---

**Wildcard Search:**
```
United*
```

---

## ⚙️ Logical Operators

### AND
```
"United States" AND "Virginia"
```

### OR
```
"United States" OR "England"
```

### NOT
```
"United States" AND NOT ("Florida")
```

---

## 🧠 Field-Based Query Example

```
Source_ip: 238.163.231.224 AND UserName: Suleman
```

📌 This shows logs where:
- Source IP matches
- Username matches

---

## 🎥 Log Investigation Demo

<img src="https://github.com/user-attachments/assets/ebbe6449-2826-47c7-b64c-15c3f9816b9f" />

---

## 📈 Creating Visualizations

### Failed VPN Login Attempts

- Data View: `vpn_connections`
- Time Range: January 2022
- Filter: `action: failed`
- Fields: `UserName`, `Source_ip`

<img src="https://cdn-images.tryhackme.com/user-uploads/5e8dd9a4a45e18443162feab/room-content/93e9aebb89efb58df9ab5a52eeb0177c.gif" />

---

# 🚀 Conclusion

This lab demonstrates how SOC analysts:
- Search logs using KQL  
- Filter suspicious activity  
- Visualize failed login attempts  
