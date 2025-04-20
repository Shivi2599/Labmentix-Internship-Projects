# Project Background

FedEx Corporation, established in 1971, is an American multinational conglomerate holding company specializing in transportation, e-commerce, and business services. The company is headquartered in Memphis, Tennessee.

**Objective** 

To explore patterns in shipment logistics, vendor contributions, insurance costs, and product distribution using visual analytics, and to derive actionable business insights that can drive operational efficiency.

**Key Analyses Conducted**

- **Shipment Distribution by Country:** Identified top receiving countries by shipment frequency and volume.

- **Vendor and Manufacturing Site Analysis:** Assessed supplier dominance and manufacturing location trends.

- **Brand Distribution:** Evaluated brand usage concentration, revealing heavy reliance on generics.

- **INCO Terms and Vendor Terms:** Analyzed shipping agreements and vendor contributions to understand logistic preferences.

- **Shipment Mode vs. Line Item Value:** Highlighted how specific transportation methods contribute disproportionately to overall shipment value.

- **Insurance vs. Weight Analysis:** Investigated the relationship between shipment weight and insurance cost, showing a positive trend.

**Problem Statement**

- Are shipments managed by specific teams (e.g., PMO – US) more likely to be delivered on time?

- Does the mode of shipment (air, sea, etc.) affect delivery performance?

- Do certain countries face more frequent delays?

- Is there a relationship between the shipment mode and frequency of on-time deliveries?

- Does the time gap between the PO Sent to Vendor Date and the Scheduled Delivery Date influence delivery performance?

We also explored whether the weight of shipments affected the insurance cost and if INCO terms had any significant impact on vendor delivery reliability

Python Code used to clean, organise, and prepare data for EDA is [here.](https://github.com/Shivi2599/Labmentix-Internship-Projects/blob/main/FedEx/FedEx_EDA_%20(1).ipynb)

Python code to visualize the dataset is [here.](https://github.com/Shivi2599/Labmentix-Internship-Projects/blob/main/FedEx/FedEx_EDA_%20(1).ipynb)

# Data Structure and Initial Checks

FedEx's database structure as seen below consists of 

| **Column Name**                     | **Description** |
|------------------------------------|-----------------|
| **ID**                             | Unique identifier for each row/record. |
| **Project Code**                   | Code representing the project or initiative tied to shipment. |
| **PQ #**                           | Price Quotation reference number. |
| **PO / SO #**                      | Purchase Order or Sales Order associated with the shipment. |
| **ASN/DN #**                       | Advanced Shipment Notice or Delivery Note refernce; uniquely identifies the shipment. |
| **Freight Cost (USD)**            | Shipping cost in US Dollars for the line item. |
| **Weight (Kilograms)**            | Total weight of the shipment for the line item. |
| **Country**                        | Destination country for the shipment. |
| **Managed By**                     | Internal team managing the order or shipment. |
| **Fulfill Via**                    | Fulfillment route, e.g., direct drop or distribution hub. |
| **Vendor INCO Term**              | International Commercial Terms used to define shipping responsibilities (e.g., EXW, FOB). |
| **Shipment Mode**                 | Method of shipment — Air, Ocean, Truck, Air Charter. |
| **PQ First Sent to Client Date**  | Date the first price quotation was sent to the client. |
| **PO Sent to Vendor Date**        | Date the purchase order was sent to the vendor. |
| **Scheduled Delivery Date**       | The planned delivery date for the delivery. |
| **Delivered to Client Date**      | The actual date the shipment was delivered to the client. |
| **Delivery Recorded Date**        | Date when delivery was officially recorded in the system. |
| **Product Group**                 | High-level category of the product (e.g., HRDT, medical supplies). |
| **Sub Classification**            | More specific classification within the product group. |
| **Vendor**                         | Name of the supplier/vendor fulfilling the order. |
| **Brand**                          | Product brand name. |
| **Dosage**                         | Dosage value, if applicable (may be N/A for test kits). |
| **Dosage Form**                    | Form in which the drug/product is delivered (e.g., tablet, test kit). |
| **Unit of Measure (Per Pack)**     | Quantity or measure of items contained per pack. |
| **Line Item Quantity**             | Number of units/packs ordered for that item. |
| **Line Item Value**                | Total value of the line item (Line Item Quantity × Pack Price). |
| **Pack Price**                     | Price per pack/unit as defined in the PO. |
| **Unit Price**                     | Price per individual unit of the item. |
| **Line Item Insurance (USD)**      | Insurance cost for the line item, if applicable. |


# Executive Summary

This exploratory data analysis focuses on pharmaceutical shipments across multiple countries. The objective was to uncover operational patterns and insights related to delivery performance, shipment modes, vendor distribution, insurance, and costs, enabling better data-driven decision-making.

## Overview of Key Findings

**Top Shipment Destinations**
- **South Africa, Vietnam, and Haiti** received the highest shipment volumes.

- **Countries such as Guyana, Belize, Dominican Republic, Nigeria, Uganda, Burundi, Swaziland, and Rwanda** received shipments 15+ days ahead of their scheduled delivery date.

- **Congo DRC, Togo, Benin, Senegal, and Kenya** frequently experience late deliveries.

**Shipment Mode & Performance**
- **Air and Air Charter** modes have **~90% on-time delivery rates**, making them reliable for urgent deliveries.

- **Ocean and Truck modes** perform slightly lower, at **~80%**, indicating potential for improvement.

- **Air Charter and Truck** have the **highest average early delivery** (15 and 10 days, respectively).

- Despite carrying the **highest volume**, the **Air** mode carries the **lowest average weight**, suggesting frequent but lightweight shipments.

**Cost & Insurance Analysis**
- **Heavier shipments** are generally associated with **higher insurance costs**.

- **Air Charter and Ocean** have the **highest freight costs**, despite **lower shipment frequency** and **lower item value.**

- **Air and Truck** offer the best cost-to-volume performance, being both cost-effective and frequently used.

**Shipment Value Insights**
- **Air and Truck** dominate in shipment value (approx. 6×10⁸ each).

- **ARV and HRDT** product groups contribute the most to overall shipment value.

- The most valuable item: **Lamivudine/Nevirapine/Zidovudine 150/200/300mg Tablets (60 Tabs)** – worth nearly 2.5×10⁸.

**Vendors & Manufacturing Sites**
- Vendor SCMS From RDC leads in shipment frequency, followed by Orgenics, Ltd.

- **RDC (Regional Distribution Center)** and **EXW** are the most used INCO terms.

- Top **manufacturing sites** (e.g., Aurobindo Unit III, Mylan, Hetero) are **India-based**, indicating geographic concentration.

**Dosage & Brand Trends**
- **Generic** products dominate, with over 7,000 shipments.

- The top dosage form by value is **Tablet - FDC**, totaling approximately 8×10⁸ in shipment value.

- Most branded products are low in volume, suggesting a cost-effective strategy focusing on generics.

**Delivery & Operations**
- **PMO-US** manages **99.4%** of all shipments.

- The **South Africa Field Office**, though managing only **0.587%** of operations, has the **highest on-time delivery rate (98.2%)**.

- On-time delivery is consistently high across all lead time ranges, indicating process stability.

# Summary
This analysis highlights key areas for optimization:

- Strengthen operations in high-volume countries and underperforming regions.
- Diversify vendor and manufacturing reliance beyond India and RDCs.
- Leverage air and truck modes for cost-effective and timely deliveries.
- Re-evaluate use of ocean and air charter modes to reduce unnecessary freight costs.
