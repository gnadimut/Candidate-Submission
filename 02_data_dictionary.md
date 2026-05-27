**BrickLine Motors Enterprise Automotive Data Dictionary (Cross Domain)**

Manufacturing Data Lake  
Dealer Network Data Lake  
Auto Parts E-Commerce Data Lake  
Governance  
Analytics  
Recall Management

Cross Domain Business Data Dictionary  
				

| Business Term | Definition | Domain Owner | Classification	 | Synonym  |
| :---- | :---- | :---- | :---- | :---- |
| VIN (Vehicle Identification Number) | Unique identifier assigned to each manufactured vehicle (vin, trade in vin, received vin) common identifier across domains  | Manufacturing | Confidential | Confidential |
| Supplier ID | Identifier assigned to external suppliers/vendors | Manufacturing | Internal | Vendor ID |
| Plant Code | Identifier for manufacturing plant location | Manufacturing | Internal | Factory Code |
| Customer Master ID | Enterprise unique identifier for a customer | Dealer Network | Restricted | Customer Key |
| Dealer ID | Unique identifier assigned to authorized dealer locations | Dealer Network | Internal | Dealer Code |
| Shipment Tracking Number | Identifier used for logistics tracking of parts/orders | Commerce | Internal | Tracking ID |
| Parts Fulfillment Status | Identifier used for logistics tracking of parts/orders | Commerce | Internal | Order Status |
| Quantity Received | Number of quantity received in one plant it is named as quantity and other plant named as qty\_received | Manufacturing | internal | Quantiy Received |
| Plant Code | Plant, plant\_code name used in different plants | Manufacturing | internal | Plant Code |
| Completion timestamp  | \`line\_completion\_ts\` \`completed\_at\` Completion timestamp  Plus, date format differs: Plant 1 uses \`YYYY-MM-DD\`, Plant 2 uses \`YYYY/MM/DD\`.  | Manufacturing | Internal | Completion Date |

| Classification |     Meaning |
| :---- | :---- |

| Public | Non-sensitive business information |
| :---- | :---- |

| Internal | Internal operational use only |
| :---- | :---- |

| Confidential | Sensitive enterprise operational data |
| :---- | :---- |

| Restricted (PII) | Personally identifiable or regulated information  |
| :---- | :---- |

**Cross Domain Data Entities**

**VIN Master → Manufacturing → Dealer Network → Auto Parts E-Commerce**

# **Governance Integration**

This dictionary feeds:

* Metadata Catalog  
* Lineage Systems  
* Data Quality Rules  
* Power BI Semantic Models  
* MDM Systems  
* Compliance Policies

  # 

  # 

  # **Data Quality Rules Example**

| Business Term | Validation Rule |
| :---- | :---- |
| VIN | Must be unique and 17 characters |
| Recall Status | Allowed values only |
| Dealer ID | Must exist in dealer master |
| Parts Order | Cannot reference invalid VIN |
| Customer Master ID | No duplicate active records |

  # **Recommended Governance Tools**

| Capability | Technology |
| :---- | :---- |
| Metadata Catalog | Collibra / Unity Catalog |
| Data Lineage | OpenLineage |
| MDM | Informatica MDM |
| BI Semantic Layer | Microsoft Power BI |
| Data Quality | Great Expectations |

  # 

  # **Final Outcome**

This enterprise business glossary establishes:

* standardized enterprise vocabulary,  
* cross-domain interoperability,  
* governance consistency,  
* and trusted analytics

across Manufacturing, Dealer Network, and Auto Parts E-Commerce domains.

