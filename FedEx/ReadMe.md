# Project Background

FedEx Corporation, established in 1971, is an American multinational conglomerate holding company specializing in transportation, e-commerce, and business services. The company is headquartered in Memphis, Tennessee.

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

