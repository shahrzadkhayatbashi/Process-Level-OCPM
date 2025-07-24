# 📝Summary of the log

### 📦 Dataset Overview

The **Logistics OCEL log** simulates an end-to-end supply chain scenario, encompassing the complete lifecycle from order placement to final transportation. The event log adheres to the OCEL standard and captures interactions between various objects involved in the logistics value chain. The log is available in [OCEL format](https://ocel-standard.org/event-logs/simulations/logistics).

### 🌐 Domain Context

- **Scenario**: Simulated global logistics operation
- **Start Point**: Customer places an order
- **End Point**: Goods are shipped via long-distance carriers (ships, trains)
- **Object Types Involved**:
  - `order`
  - `good`
  - `transport_document`
  - `container`

These objects co-occur in events that capture various phases of the logistics process and are linked through object-centric relationships. The following figure illustrates the overall steps involved in the chain:

![Process Abstractions](https://ocel-standard.org/event-logs/simulations/logistics/images/logistics-overview_hu3208343689473859737.webp)

---

## 🛠️ Application in Our Research

To validate our method, we applied it to this dataset using our proposed enrichment framework. We decomposed the end-to-end chain into four interrelated yet distinct processes, reflecting real-world logistics phases:

### 1. **Order Management**

- **Description**: Tracks the lifecycle of customer orders, focusing on the initial flow of orders and associated documentation.
- **Purpose**: Serves as the initiation point for downstream logistical coordination.

### 2. **Goods Management**

- **Description**: Handles pre-shipping activities, encapsulating the preparation of goods for shipping.
- **Purpose**: Prepares physical goods for the dispatch phase.

### 3. **Transportation Management**

- **Description**: Captures ground transport operations, isolating logistical container transfers across warehouse and terminal infrastructure.
- **Purpose**: Models intra-network container movements before export, focusing on mid-chain logistical movement.

### 4. **Export Management**

- **Description**: Represents final outbound activities, dealing with preparing containers for export and executing shipment.
- **Purpose**: Final logistics stage, executing global export.

Each process was modeled independently but maintained object-centric links across shared entities, enabling comprehensive process-centric analysis.
ta.
