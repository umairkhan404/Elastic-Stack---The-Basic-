#  Elastic-Stack---The-Basic-

 Understand how SOC analysts use the elastic stack (ELK) for log investigations.
---

# 🔍 Elastic Stack (ELK) - SOC Log Investigation

🛡️ Understand how SOC analysts use the Elastic Stack (ELK) for real-world log analysis, threat detection, and security investigations.

---

## 📊 Dashboard Overview

📌 Below dashboards show how logs are visualized inside Kibana:

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

<img src="https://github.com/user-attachments/assets/45b28b42-6286-4d82-b595-fa14ed52d9a4" />

<img width="1739" height="673" alt="image" src="https://github.com/user-attachments/assets/fbebeff4-4606-4c35-a153-3d57f8e4daae" />

<img src="https://github.com/user-attachments/assets/14f67648-5b19-4219-8c2a-9a741b11d765" />

---

## 🔎 KQL (Kibana Query Language)

⚙️ KQL is used by SOC analysts to search and filter logs efficiently inside Kibana.

We can search logs in two ways:

- 🔹 Free-text search  
- 🔹 Field-based search  

---

## 🧪 Free-text search

<img width="1739" height="673" alt="image" src="https://github.com/user-attachments/assets/23491f0d-451e-4792-af37-0f0773cfe18d" />

👉 This returns all logs containing the phrase **United States**

---

## 🧪 Wildcard search

<img width="1633" height="630" alt="image 1" src="https://github.com/user-attachments/assets/e0be803b-4e0b-4381-9d24-37ed2aa0dad3" />

👉 This returns all values starting with “United”  
(e.g. United States, United Kingdom)

---

## ⚙️ Logical Operators in KQL

🛡️ SOC analysts use logical operators to refine search results.

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
- 🔹 Source IP matches attacker/host IP  
- 🔹 Username matches specific user  

---

## 🎥 Log Investigation Demo (GIF Explained)

📊 Below GIF shows a **real SOC workflow inside Kibana Discover tab**:

<img src="https://github.com/user-attachments/assets/ebbe6449-2826-47c7-b64c-15c3f9816b9f" />

### 🧠 What is happening in this GIF?

✔️ Logs are being searched inside Kibana  
✔️ SOC analyst is filtering events using KQL  
✔️ Relevant events are being isolated from large datasets  
✔️ Suspicious activity patterns are identified  

👉 Basically, this shows how SOC analysts move from **raw logs → filtered insights → investigation**

---

## 📈 Creating Visualizations

<img src="https://github.com/user-attachments/assets/1756f3c3-ac3e-47ba-99fc-f50b760d573b" />

---

### 🚨 Failed VPN Login Attempts

SOC analysts often visualize failed login attempts to detect:

- 🔥 brute force attacks  
- ⚠️ suspicious access patterns  
- 🚨 unauthorized access attempts  

---

### 🔧 Setup details:

- 📊 Data View: `vpn_connections`  
- ⏱️ Time Range: January 2022  
- 🔍 Filter: `action: failed`  
- 📌 Fields used: `UserName`, `Source_ip`  

---

## 🧠 What this GIF shows:

✔️ Creating a visualization in Kibana  
✔️ Filtering failed VPN login attempts  
✔️ Building a table/chart from raw logs  
✔️ Turning logs into actionable security insights  

👉 This is how SOC analysts convert **logs → visual threat detection dashboards**

---
## **`Creating a Custom Dashboard`**

By now, we have saved a few `Searches` from the `Discover tab`, created some `Visualizations`, and saved them. It's time to explore the dashboard tab and create a custom dashboard. The steps to create a dashboard are:

<img width="697" height="469" alt="image" src="https://github.com/user-attachments/assets/1e5673be-b754-4c31-8368-152bf2ab3113" />


- Click on `Add from Library.`
- Click on the visualizations and saved searches. It will be added to the dashboard.
- Once the items are added, adjust them accordingly, as shown below.
- Don't forget to save the dashboard after completing it.


<img width="1914" height="1034" alt="05016a6cc1c12d40b90ce9d29052537811-ezgif com-optimize" src="https://github.com/user-attachments/assets/0d966a1a-49bf-4d74-bd98-4ddefcfcc8bf" />


# 🚀 Conclusion

This lab demonstrates core SOC analyst skills:

✔️ Searching logs using KQL  
✔️ Filtering suspicious activity  
✔️ Investigating authentication events  
✔️ Creating visual dashboards  
✔️ Turning raw logs into security insights  

---

<h2>🛡️ Elastic Stack</h2>

Elastic Stack helps SOC analysts detect threats faster by making huge log data searchable and visual.

<h2>SOC Simulation (TryHackMe)</h2>

Practiced triaging security alerts in a simulated SOC environment — classifying alerts as true/false positives, assigning them for handling, and documenting findings in case reports for L2 escalation.

<img width="1886" height="967" alt="image" src="https://github.com/user-attachments/assets/1c26d38b-7db0-4ecc-b16c-3398fd0627a7" />

<h3>Alert Classification</h3>

I assigned these alerts as True Positive, since they involved phishing tactics using a malicious URL.

<img width="660" height="330" alt="image" src="https://github.com/user-attachments/assets/ee5778a0-2f4a-43f6-b67d-1d32dc054562" />

<h3>Initial Triage</h3>

The alert severity was High on the dashboard, so it was important to prioritize this alert as it appeared to be a real attack. As an L1 SOC analyst, the first step was to check the URL using an analysis tool, referencing the MITRE ATT&CK framework for context.

<img width="1882" height="435" alt="image" src="https://github.com/user-attachments/assets/c875a13a-8d39-4237-bec2-6392e3eb0d6d" />

<img width="1882" height="435" alt="image" src="https://github.com/user-attachments/assets/2e04dfe0-3ff2-48fe-970b-f4ba4e69d343" />

<img width="1797" height="560" alt="image" src="https://github.com/user-attachments/assets/b0969bbb-c3d0-434c-a69e-234a69048f61" />

<h3>Case Report</h3>

After assigning the alert to myself, I analyzed it and wrote a case report explaining the alert triage details for the L2 analyst to continue further investigation.

<img width="1810" height="897" alt="image" src="https://github.com/user-attachments/assets/a3cf4512-2b31-43ee-b441-3cbec2b4f02c" />

<img width="1826" height="882" alt="image" src="https://github.com/user-attachments/assets/1f1552a5-eb82-442d-9822-0c171b069988" />

<h3>SIEM Investigation (Kibana Discover)</h3>

I used the SIEM tool (Kibana Discover) to investigate in depth. In this screenshot, I investigated the repeated IP address and the repeated requests sent by the attacker. In this scenario, I looked at the malicious source IP that was blocked by the firewall due to the rules set in place.

<img width="1906" height="977" alt="image" src="https://github.com/user-attachments/assets/a9ff32fd-43a2-4265-8098-29e186ba7fce" />

<h3>Log Analysis</h3>

Log 1 (blocked, port 80): a bit.ly shortened link → this is what triggered the block, since shortened/obfuscated URLs are commonly used to hide phishing destinations, and it was likely already listed in threat intel/blacklist feeds.
Log 2 (allowed, port 443): a direct google.com search query about payroll systems → clean, legitimate traffic, unrelated to the blocked request.

The same internal source IP generated two separate requests. One was a shortened bit.ly link on port 80, which the firewall blocked as it matched a known-malicious/blacklisted URL. The other was a legitimate Google search on port 443, related to payroll system research, which was correctly allowed. This shows the value of correlating multiple log entries from the same host to distinguish malicious activity from normal user behavior.

That's why I'm doing a deeper investigation in the Elastic Stack (SIEM), because sometimes I need to look at the attacker's tactics, or check whether an employee accessed a fake attacker link while browsing what appeared to be a normal URL. Sometimes attackers leave a trap on a duplicate website — the employee believes it's the real site, but in the backend they get redirected to the attacker's webpage. That's why the firewall blocked the malicious URL on port 80, while port 443 was allowed as normal traffic, depending on the rule set in each case.

<img width="1911" height="933" alt="image" src="https://github.com/user-attachments/assets/0825cf1f-205d-4a4f-b997-a8606417dd1d" />

<h3>Escalation Report – Alert ID: 8816</h3>

<img width="1847" height="945" alt="image" src="https://github.com/user-attachments/assets/b81ebc1c-6f3d-49bb-bbd9-3c1c65397d2b" />

<img width="1865" height="967" alt="image" src="https://github.com/user-attachments/assets/213a57e2-2bfb-4f41-8aea-1d5f140016d8" />

<h3>Closing the Alert</h3>

After completing the investigation, I closed the alert as SOC Analyst L1.

<img width="1886" height="951" alt="image" src="https://github.com/user-attachments/assets/bc9ab956-aea2-4f61-bdbf-2f3262a4d4ba" />

<h3>What I Learned</h3>

From all of this, what I learned is how to investigate logs, how to assign an alert to myself, and how to write a case report for L2 for further investigation. I also learned how to check whether an alert is a real alarm or a false alarm, and determine if it's a false positive or true positive. I investigated this using Discover in Kibana (Elastic Stack) for log analysis, and after the investigation, I found it to be a true positive and closed the alert accordingly, as shown in the screenshots above. All of this — including the Elastic Stack — was provided by the TryHackMe platform, where I got hands-on practice for the SOC Analyst L1 role.
