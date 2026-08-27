[ELASTIC-STACK-SEIM.md](https://github.com/user-attachments/files/31527335/ELASTIC-STACK-SEIM.md)# Elastic-Stack---The-Basic-
Understand how SOC analysts use the elastic stack (ELK) for log investigations.

[Uploadin# SEIM

# **`Elasticsearch - KQL (Kibana Query Language)`**

With KQL, we can search logs in two ways:

- Free-text search
- Field-based search

**Field-based search:**

**Search Query:** `"United States"` 

![image.png](image.png)

**Search Query:** `United*` 

![image.png](image%201.png)

## `Logical Operators (AND | OR | NOT)`

## **1. AND Operator**

Use the **AND** operator to create a search that returns logs containing both `"United States"` and `"Virginia"`.

**Search Query:** `"United States" AND "Virginia"`

![image.png](image%202.png)

## **2. OR Operator**

Use the **OR** operator to return logs that contain either `United States` or `England`.

**Search Query:** `"United States" OR "England"` 

![image.png](image%203.png)

## **3. NOT Operator**

Similarly, use the **NOT** operator to exclude a term from the search results. This query returns logs from **the United States** (including all states) while ignoring Florida.

**Search Query:** `"United States" AND NOT ("Florida")` 

![image.png](image%204.png)

## **Field-based search:**

**Search Query:** `Source_ip : 238.163.231.224 AND UserName : Suleman`

**Explanation:** This query tells Kibana to display all logs where `Source_ip` contains `238.163.231.224` and `UserName` is `Suleman`, as shown below.

![ffbf735277d98273d6229f4d9ee586bf.gif](ffbf735277d98273d6229f4d9ee586bf.gif)

## `Creating Visualizations`

## Create Visualization

There are a few ways to navigate to the Visualization tab. One approach is to click any field in the Discover tab, then select **Visualize**, as shown below.

![](https://cdn-images.tryhackme.com/user-uploads/5e8dd9a4a45e18443162feab/room-content/334ed7c0a1e727de35844174434fd4fc.gif)

## **`Failed Connection Attempts Visualization`**

**Failed attempts filter:** For the failed connection visualisation, use the `vpn_connections` data view, set the time picker to include January 2022, then filter for `action: failed`. Do not exclude failed events; the table should only show failed VPN connection attempts. Use `UserName` and `Source_ip` as the table fields.

![](https://cdn-images.tryhackme.com/user-uploads/5e8dd9a4a45e18443162feab/room-content/93e9aebb89efb58df9ab5a52eeb0177c.gif)g ELASTIC-STACK-SEIM.md…]()
