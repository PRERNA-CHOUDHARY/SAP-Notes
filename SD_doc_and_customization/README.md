
---

### **1. Sales Phase**

The Sales Phase involves creating and managing sales orders, which are agreements between a company and a customer to deliver products or services under specific terms.

#### **1.1 Sales Order Processing**
- **Sales Order:** The central document in the sales process that records the customer's request for products or services. 
  - **Key Elements:**
    - **Header Data:** General information such as order date, customer details, and delivery terms.
    - **Item Data:** Specific details for each product or service, including quantities, prices, and delivery schedules.
    - **Schedule Lines:** Specific dates and quantities for each item in the sales order.

#### **1.2 Sales Document Types**
- **Standard Order (OR):** The most common sales document, used for regular sales transactions.
- **Rush Order:** Orders where the goods are delivered immediately, and billing is processed later.
- **Cash Sales:** The customer pays at the time of order, and the delivery is made immediately.

#### **1.3 Pricing and Conditions**
- **Pricing Procedure:** A sequence of condition types (like base price, discounts, taxes) applied to determine the final price of the order.
  - **Condition Types:** Define specific pricing elements (e.g., PR00 for base price, K007 for customer discount).
  - **Access Sequence:** Determines how the system searches for valid condition records.

#### **1.4 Availability Check**
- **Purpose:** Ensures that the required quantity of a product is available in stock or can be procured by the requested delivery date.
- **Types:**
  - **ATP (Available to Promise):** Checks current stock, incoming deliveries, and planned receipts.
  - **Product Allocation:** Restricts the quantity available for sale based on predefined limits.

#### **1.5 Credit Management**
- **Purpose:** Controls the risk of credit exposure by checking the customer's credit limit before confirming an order.
- **Dynamic Credit Check:** Takes into account open orders, deliveries, and invoices to determine if the customer has exceeded their credit limit.

---

### **2. Delivery Phase**

The Delivery Phase handles the outbound logistics, including the preparation, shipment, and physical movement of goods.

#### **2.1 Delivery Creation**
- **Delivery Document:** A record that facilitates the physical movement of goods from the company to the customer.
  - **Delivery Types:**
    - **Outbound Delivery (LF):** Standard document for shipping goods.
    - **Returns Delivery:** Used when goods are returned by the customer.

#### **2.2 Picking and Packing**
- **Picking:** The process of selecting the goods from storage locations according to the delivery document.
- **Packing:** Organizing the selected goods into suitable containers for shipping.
  - **Handling Units:** Packaging units that track packed goods.

#### **2.3 Post Goods Issue (PGI)**
- **Purpose:** Indicates that the goods have physically left the warehouse and are on their way to the customer.
- **Impact:**
  - **Inventory Reduction:** The system reduces the inventory levels.
  - **Accounting Impact:** A financial document is created to reflect the reduction in inventory and the increase in cost of goods sold (COGS).

#### **2.4 Transportation Management**
- **Purpose:** Manages the planning, execution, and monitoring of transportation activities.
  - **Transportation Planning:** Determines the best route, mode of transport, and carrier for shipping the goods.
  - **Transportation Scheduling:** Aligns the delivery dates and times with transportation schedules.

---

### **3. Billing Phase**

The Billing Phase involves the generation of invoices and other billing documents to request payment from the customer.

#### **3.1 Billing Document**
- **Purpose:** Represents an invoice or credit/debit memo issued to the customer based on the delivery and sales order.
  - **Billing Types:**
    - **Invoice (F2):** Standard billing document for delivered goods or services.
    - **Credit Memo:** Issued when the customer is owed money, often due to returns or pricing adjustments.
    - **Debit Memo:** Issued when the customer needs to pay more, possibly due to undercharging.

#### **3.2 Billing Methods**
- **Individual Billing:** One billing document per delivery or sales order.
- **Collective Billing:** Multiple deliveries or sales orders combined into a single billing document.
- **Invoice Splitting:** A single sales order split into multiple invoices based on specific criteria like delivery dates.

#### **3.3 Revenue Recognition**
- **Purpose:** Ensures that revenue is recognized in the correct accounting period, based on delivery or service completion.
  - **Time-Based Recognition:** Revenue is recognized periodically, such as monthly or quarterly.
  - **Event-Based Recognition:** Revenue is recognized upon the completion of a significant event, like delivery or project completion.

---

### **4. Advanced Topics in SAP SD**

#### **4.1 Customizing Sales Documents**
- **Purpose:** Tailor sales documents to meet specific business requirements.
  - **Sales Document Types:** Customize different types of sales documents, such as orders, contracts, and quotations, to fit business needs.
  - **Item Categories:** Define how items in the sales document behave, including pricing, inventory checks, and shipping requirements.
  - **Schedule Line Categories:** Customize the delivery schedule details, including availability checks and requirement types.

#### **4.2 Delivery Determination**
- **Purpose:** Automates the process of determining which delivery documents are created based on specific criteria in the sales order.
  - **Delivery Group:** Combines multiple items into a single delivery based on common criteria like shipping point, delivery date, and transportation group.
  - **Shipping Point Determination:** Assigns the correct shipping point (warehouse or distribution center) based on the combination of shipping conditions, loading group, and plant.

#### **4.3 Partner Functions**
- **Purpose:** Defines the various business partners involved in a sales transaction, such as sold-to, ship-to, bill-to, and payer.
  - **Customizing Partner Determination:** Configure rules for how partners are automatically assigned to sales documents.

#### **4.4 Output Determination**
- **Purpose:** Manages the automated generation of documents (e.g., order confirmations, invoices) that are sent to customers and other stakeholders.
  - **Output Types:** Different types of outputs like printouts, emails, EDI (Electronic Data Interchange) messages.
  - **Access Sequences:** Determines how the system finds the appropriate output condition records.
  - **Condition Records:** Stores the output conditions (e.g., when an invoice should be printed or emailed).

#### **4.5 Cross-Module Integration**
- **SAP MM Integration:**
  - **Availability Check:** Integrates with Material Management (MM) for checking stock levels.
  - **Procurement:** Sales orders can trigger purchase requisitions for external procurement.
  
- **SAP FI Integration:**
  - **Revenue Posting:** Sales invoices post directly to the accounts receivable in Financial Accounting (FI).
  - **Credit Management:** Monitors credit limits by integrating with the customer accounts in FI.

- **SAP PP Integration:**
  - **Make-to-Order:** Sales orders trigger production orders in Production Planning (PP) if goods are not available.
  - **Availability Check:** Coordinates with PP for component availability during production.

#### **4.6 Sales Information System (SIS)**
- **Purpose:** Provides comprehensive reporting and analysis capabilities for sales data.
  - **Standard Reports:** Pre-configured reports for sales performance, order backlog, delivery performance, etc.
  - **Custom Reports:** Ability to create custom reports using specific criteria like customer, material, sales organization.

---
