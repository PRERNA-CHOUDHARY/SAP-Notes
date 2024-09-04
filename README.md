### SAP SD (Sales and Distribution) Overview: Beginner's Guide

**SAP Sales and Distribution (SD)** is a core module of SAP ERP that deals with the processes of order-to-cash (OTC) cycle. It integrates with other SAP modules such as Materials Management (MM), Finance (FI), and Production Planning (PP). Below is a structured overview of the key concepts and processes in SAP SD, designed to help beginners understand and revise the essentials.

---

## 1. **Introduction to SAP SD**

- **Purpose:** Manages customer relationships from order creation to delivery and billing.
- **Key Processes:** Sales order processing, shipping, billing, pricing, credit management.

### Key Components:
- **Master Data:** Customer Master, Material Master, Pricing Conditions.
- **Sales:** Sales Orders, Contracts, Scheduling Agreements.
- **Shipping:** Delivery Documents, Picking, Packing, Post Goods Issue.
- **Billing:** Invoice Generation, Credit/Debit Memo.
- **Sales Support:** Inquiries, Quotations, Sales Reporting.

---

## 2. **Master Data in SAP SD**

### 2.1 Customer Master Data
- **Definition:** Stores all data related to customers (e.g., contact information, payment terms).
- **Structure:**
  - **General Data:** Basic information, valid across company codes and sales areas.
  - **Company Code Data:** Financial accounting-related data.
  - **Sales Area Data:** Data specific to sales, distribution, and partner functions.

### 2.2 Material Master Data
- **Definition:** Central repository of all information about products/services sold by the company.
- **Structure:**
  - **Basic Data:** General information about the product (e.g., weight, volume).
  - **Sales Organization Data:** Sales-specific data like pricing, tax classification.
  - **Sales General/Plant Data:** Data related to inventory management and distribution.

### 2.3 Pricing Conditions
- **Definition:** Determines the price of a product based on various factors (e.g., customer, material, quantity).
- **Components:**
  - **Condition Types:** Define the pricing elements (e.g., base price, discount, tax).
  - **Access Sequence:** Determines the order in which the system searches for valid pricing conditions.
  - **Pricing Procedure:** Sequence of condition types applied during sales order processing.

---

## 3. **Sales Order Processing**

### 3.1 Sales Document Structure
- **Sales Order:** Central document in SD, representing an agreement with the customer to deliver products/services at a specific price and date.
- **Key Components:**
  - **Header:** General data (e.g., customer, date).
  - **Item:** Data for individual products/services.
  - **Schedule Lines:** Delivery dates, quantities, and times.

### 3.2 Order Types
- **Standard Order:** Typical sales order with fixed pricing and delivery.
- **Rush Order:** Immediate delivery after order is placed.
- **Cash Sales:** Customer pays immediately, delivery happens on the spot.

### 3.3 Sales Order Cycle
1. **Inquiry:** Customer request for information about products/services.
2. **Quotation:** Detailed offer provided to the customer.
3. **Sales Order:** Formal order based on the quotation or inquiry.
4. **Delivery:** Shipping process begins.
5. **Billing:** Invoice is generated and sent to the customer.
6. **Payment:** Customer makes the payment.

---

## 4. **Shipping and Delivery**

### 4.1 Delivery Processing
- **Definition:** Handling the outbound logistics, including picking, packing, and shipping goods.
- **Delivery Document:** Controls and monitors the delivery process.
- **Picking:** Selection of goods from storage locations.
- **Packing:** Organizing goods into packages.
- **Post Goods Issue (PGI):** Legal ownership of goods is transferred to the customer, reducing inventory.

### 4.2 Delivery Types
- **Standard Delivery:** Regular shipping process.
- **Partial Delivery:** Part of the order is shipped, the rest follows later.
- **Returns Delivery:** Goods returned by the customer are processed here.

---

## 5. **Billing and Invoicing**

### 5.1 Billing Process
- **Definition:** Creating and managing invoices for goods or services provided.
- **Billing Document:** Represents the invoice issued to the customer.
- **Types of Billing:**
  - **Invoice:** Standard billing document.
  - **Credit Memo:** Issued when the customer is owed money.
  - **Debit Memo:** Issued when the customer owes more money.

### 5.2 Billing Methods
- **Individual Billing:** One invoice per delivery.
- **Collective Billing:** Multiple deliveries combined into a single invoice.
- **Invoice Split:** One sales order split into multiple invoices.

---

## 6. **Key Configuration in SAP SD**

### 6.1 Organizational Structure
- **Sales Organization:** Central unit responsible for selling products/services.
- **Distribution Channel:** Path through which products/services reach customers (e.g., direct sales, retail).
- **Division:** Product line or service group.

### 6.2 Sales Document Configuration
- **Sales Document Types:** Customizing document types (e.g., order, contract).
- **Item Categories:** Define how items behave in sales documents (e.g., standard, free goods).
- **Schedule Line Categories:** Manage delivery dates and quantities.

### 6.3 Pricing Configuration
- **Condition Tables:** Storage for all condition records.
- **Access Sequences:** Order in which the system accesses condition tables.
- **Condition Exclusion:** Used to prevent certain pricing conditions from being applied.

---

## 7. **Integration with Other SAP Modules**

### 7.1 SAP MM (Materials Management)
- **Integration Points:** Availability check, inventory management, procurement.
- **Example:** When creating a sales order, the system checks material availability in MM.

### 7.2 SAP FI (Financial Accounting)
- **Integration Points:** Invoice generation, revenue recognition, credit management.
- **Example:** Posting a sales invoice in SD automatically updates the accounts receivable in FI.

### 7.3 SAP PP (Production Planning)
- **Integration Points:** Make-to-order production, availability of finished goods.
- **Example:** A sales order might trigger a production order if the goods aren’t available.

---

## 8. **Common Transactions in SAP SD**

- **VA01:** Create Sales Order
- **VA02:** Change Sales Order
- **VA03:** Display Sales Order
- **VL01N:** Create Outbound Delivery
- **VF01:** Create Billing Document
- **XD01:** Create Customer Master
- **MM02:** Change Material Master

---

## 9. **Key Terms and Concepts**

- **Document Flow:** Tracks the status and history of all documents related to a sales process.
- **Credit Management:** Monitors customer credit limits to reduce risk of non-payment.
- **Availability Check:** Ensures goods are available before confirming a sales order.

---
