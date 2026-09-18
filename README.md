# CAREX — AI-Powered Healthcare Inventory Intelligence

> **CAREX** is an AI-powered healthcare inventory intelligence platform designed to help pharmacies, hospitals, and clinics monitor medicine stock, predict demand, identify expiry risks, detect unusual sales, and make data-driven procurement decisions.

---

## 1. 🚨 Problem Statement

Healthcare facilities manage large numbers of medicines, batches, suppliers, and daily sales transactions. Traditional inventory management often depends on manual monitoring, making it difficult to identify critical situations early.

Common challenges include:

* 💊 **Stock-outs** of essential medicines due to insufficient monitoring.
* 📦 **Overstocking**, resulting in unnecessary inventory costs.
* ⏳ **Medicine expiry**, especially when multiple batches are maintained.
* 📈 **Unpredictable demand**, making procurement planning difficult.
* 🚨 **Unusual sales patterns** that may go unnoticed.
* 🧾 **Manual inventory tracking** across multiple operations.
* 🚚 Supplier lead times not being adequately considered during replenishment.
* 👨‍⚕️ Staff having to manually analyze multiple inventory parameters before making procurement decisions.

These challenges can make healthcare inventory management **reactive rather than proactive**.

---

# 2. 💡 Solution

**CAREX** addresses these challenges by combining healthcare inventory management with an intelligence layer.

The system brings together:

**Inventory + Sales + Expiry + Demand Prediction + Alerts + Procurement**

into a single platform.

CAREX analyzes available inventory and transaction information to identify potential risks and provide actionable recommendations.

### How CAREX works

```text
Inventory & Sales Data
        ↓
Data Processing
        ↓
Demand Prediction
        ↓
Inventory Risk Detection
        ↓
AI Alerts
        ↓
Procurement Recommendation
        ↓
Human Review
        ↓
Approve / Hold / Escalate
```

Instead of simply showing the current stock, CAREX helps users understand:

> **What is happening → What may happen next → What needs attention → What action can be considered**

The procurement process remains **human-controlled**, with recommendations presented for review rather than automatically placing orders.

---

# 3. ✨ Features

## 📊 3.1 Intelligent Dashboard

The CAREX dashboard provides a centralized overview of healthcare inventory operations.

It displays:

* Total medicines
* Today's sales
* Units sold
* Low-stock medicines
* Medicines expiring soon
* Pending procurement
* Active AI alerts
* Weekly demand information
* Inventory priority levels

---

## 💊 3.2 Medicine Inventory Management

CAREX provides medicine and batch-level visibility.

Users can view:

* Medicine name
* Generic name
* Batch ID
* Current stock
* Minimum stock
* Safety stock
* Expiry date/status
* Supplier
* Supplier lead time
* Demand forecast
* Priority

This allows users to understand the complete inventory position of a medicine.

---

## 🧾 3.3 Sales & Billing

The Sales module allows users to:

1. Select a medicine.
2. Select the relevant batch.
3. Enter quantity sold.
4. Record the transaction.
5. View recent transactions.

Sales information can subsequently contribute to demand analysis and unusual-sales detection.

---

## ⏳ 3.4 Expiry Monitoring

CAREX monitors medicine batch expiry dates.

The system can identify medicines approaching expiry and generate warnings based on the configured expiry-warning period.

Example:

```text
Medicine: Insulin
Batch: INS-2026-04
Expiry: 15 Days
Status: Expiring Soon
Priority: Urgent
```

---

## 🚨 3.5 AI-Powered Alerts

CAREX identifies important inventory events and presents them as alerts.

Examples include:

### Low Stock

```text
Paracetamol stock has fallen below the configured threshold.
```

### Expiry Warning

```text
Insulin Batch INS-2026-04 is approaching expiry.
```

### Unusual Sales

```text
Sales volume is significantly higher than the normal sales pattern.
```

Alerts can be categorized according to priority:

* 🔴 Urgent
* 🟠 High
* 🔵 Medium
* 🟢 Low

---

## 📈 3.6 Demand Prediction

CAREX uses available sales/inventory data to estimate upcoming medicine demand.

The predicted demand can help users:

* Understand upcoming requirements.
* Identify potential stock shortages.
* Plan replenishment.
* Reduce unnecessary overstocking.

The forecasting model can be replaced or upgraded as more historical data becomes available.

---

## 📦 3.7 Intelligent Procurement

CAREX provides procurement recommendations based on inventory planning parameters.

The system considers factors such as:

* Current stock
* Forecast demand
* Safety stock
* Supplier lead time
* Expected lead-time demand

### Suggested Order Logic

```text
Required Stock =
Forecast Demand
+ Safety Stock
+ Expected Lead-Time Demand
```

Then:

```text
Suggested Order =
max(0, Required Stock - Available Stock)
```

The resulting recommendation is displayed for review.

---

## ✅ 3.8 Procurement Approval Gate

CAREX does not require procurement recommendations to be automatically executed.

An authorized user can review the recommendation and select:

```text
Approve
   │
   ├── Hold
   │
   └── Escalate
```

This creates a human-in-the-loop decision process.

---

## 🤖 3.9 CAREX AI Assistant

The integrated AI assistant allows users to ask inventory-related questions using natural language.

Example:

**User:**

> Which medicine has the highest demand?

**CAREX:**

> Paracetamol has the highest sales this week with 126 units sold.

This provides users with a conversational way to access inventory insights.

---

## ⚙️ 3.10 Configurable Inventory Rules

The Settings module allows inventory planning parameters to be configured.

Examples:

* Minimum stock threshold
* Safety stock
* Expiry warning period
* Auto-order mode
* Approval requirements

This allows CAREX to adapt its recommendations according to the organization's inventory policies.

---

# 4. 🛠️ Technology Stack

> Replace the placeholders below with the exact technologies used in your final implementation.

### Frontend

* **React.js / HTML / CSS / JavaScript**
* Responsive UI
* Component-based interface
* Dashboard and data visualization

### Backend

* **Node.js / Python / Java**
* REST API
* Business logic
* Authentication
* Inventory processing

### Database

* **MySQL / PostgreSQL / MongoDB**
* Medicine records
* Batch information
* Sales transactions
* Supplier information
* Alerts
* Procurement records
* User information

### AI / Machine Learning

* Demand forecasting
* Inventory risk detection
* Unusual-sales detection
* AI assistant
* Procurement recommendation engine

### Development Tools

* Git
* GitHub
* VS Code
* API testing tools

### Deployment

* Frontend: `[Deployment Platform]`
* Backend: `[Deployment Platform]`
* Database: `[Database Hosting]`

---

# 5. 🏗️ Architecture

CAREX follows a modular architecture consisting of the **frontend, backend/API, database, intelligence layer, and user interaction layer**.

```text
                         ┌───────────────────────┐
                         │       CAREX UI        │
                         │                       │
                         │ Dashboard             │
                         │ Inventory             │
                         │ Sales                 │
                         │ Expiry               │
                         │ Alerts                │
                         │ Procurement           │
                         │ Analytics             │
                         │ AI Assistant          │
                         └───────────┬───────────┘
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │      Backend API      │
                         │                       │
                         │ Authentication        │
                         │ Inventory Services    │
                         │ Sales Services        │
                         │ Procurement Services  │
                         │ Alert Services        │
                         └───────────┬───────────┘
                                     │
                    ┌────────────────┴────────────────┐
                    │                                 │
                    ▼                                 ▼
          ┌──────────────────┐             ┌──────────────────┐
          │    Database      │             │ Intelligence     │
          │                  │             │ Layer            │
          │ Medicines        │             │                  │
          │ Batches          │             │ Demand Forecast  │
          │ Sales            │             │ Risk Detection   │
          │ Suppliers        │             │ Anomaly Detection│
          │ Alerts           │             │ Recommendations  │
          │ Procurement      │             │ AI Assistant     │
          └──────────────────┘             └────────┬─────────┘
                                                    │
                                                    ▼
                                          ┌────────────────────┐
                                          │ AI Alerts &        │
                                          │ Recommendations    │
                                          └─────────┬──────────┘
                                                    │
                                                    ▼
                                          ┌────────────────────┐
                                          │ Human Review       │
                                          │                    │
                                          │ Approve / Hold /   │
                                          │ Escalate           │
                                          └────────────────────┘
```

### Architecture Layers

| Layer                  | Responsibility                   |
| ---------------------- | -------------------------------- |
| **Frontend**           | User interface and visualization |
| **Backend/API**        | Business logic and communication |
| **Database**           | Persistent storage               |
| **AI/ML Layer**        | Prediction and intelligence      |
| **Alert Engine**       | Risk and event detection         |
| **Procurement Engine** | Replenishment recommendations    |
| **Human Review**       | Final procurement decision       |

---

# 6. ⚙️ Setup Instructions

## Prerequisites

Make sure the following are installed:

* Git
* Node.js / required runtime
* Database server
* VS Code or another development environment
* Required AI/API credentials

---

## Step 1 — Clone the Repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

Navigate into the project:

```bash
cd CAREX
```

---

## Step 2 — Install Dependencies

If the frontend/backend uses Node.js:

```bash
npm install
```

If the project contains separate frontend and backend directories:

```bash
cd frontend
npm install
```

Then:

```bash
cd ../backend
npm install
```

Use the commands specified by your actual project structure.

---

## Step 3 — Configure Environment Variables

Create a `.env` file for the required configuration.

Example:

```env
DATABASE_URL=your_database_url
API_URL=your_api_url
AI_API_KEY=your_ai_api_key
JWT_SECRET=your_secret
```

⚠️ **Never upload actual passwords, API keys, database credentials, or secrets to GitHub.**

Add `.env` to `.gitignore`:

```text
.env
.env.local
node_modules/
```

---

## Step 4 — Configure the Database

Create the CAREX database and initialize the required tables.

The database should contain entities such as:

```text
Users
Medicines
Batches
Suppliers
Sales
Alerts
Procurement
Settings
```

Add initial/demo inventory data if required.

---

## Step 5 — Start the Backend

Example:

```bash
npm run server
```

or:

```bash
npm run dev
```

depending on the implementation.

---

## Step 6 — Start the Frontend

Open another terminal:

```bash
npm run dev
```

The application should then be available through the local development URL displayed by the frontend framework.

---

## Step 7 — Verify the Application

Test the following workflows:

```text
Login
  ↓
Dashboard
  ↓
Inventory
  ↓
Sales
  ↓
Alerts
  ↓
Expiry
  ↓
Procurement
  ↓
Approve / Hold / Escalate
  ↓
Analytics / AI Assistant
```

---

# 7. 🔄 Project Workflow

CAREX follows an end-to-end inventory intelligence workflow.

## Step 1 — Data Collection

The system collects information about:

```text
Medicine
Batch
Stock
Sales
Expiry
Supplier
Lead Time
Safety Stock
```

↓

## Step 2 — Data Processing

The backend processes the available inventory and transaction data.

↓

## Step 3 — Inventory Monitoring

CAREX continuously checks:

```text
Current Stock
        +
Minimum Stock
        +
Safety Stock
        +
Expiry
```

↓

## Step 4 — Demand Analysis

Historical/current sales information is used to estimate upcoming demand.

↓

## Step 5 — Risk Detection

The system identifies conditions such as:

```text
Low Stock
Expiry Risk
Unusual Sales
Potential Shortage
```

↓

## Step 6 — AI Alerts

Detected events are converted into actionable alerts.

Example:

```text
⚠ LOW STOCK

Medicine: Omeprazole
Current Stock: 90
Minimum Stock: 100
Priority: HIGH
```

↓

## Step 7 — Procurement Recommendation

CAREX calculates a suggested replenishment quantity.

```text
Forecast Demand
       +
Safety Stock
       +
Lead-Time Demand
       ↓
Required Stock
       ↓
Suggested Order Quantity
```

↓

## Step 8 — Human Review

The procurement recommendation is presented to an authorized user.

```text
┌───────────┐
│  REVIEW   │
└─────┬─────┘
      │
 ┌────┼─────────────┐
 ▼    ▼             ▼
Approve Hold     Escalate
```

↓

## Step 9 — Inventory Action

Once approved, the procurement action can proceed according to the organization's workflow.

↓

## Step 10 — Continuous Monitoring

New stock and sales data feed back into the system.

```text
New Data
   ↓
Monitoring
   ↓
Prediction
   ↓
Alerts
   ↓
Procurement
   ↓
Review
   ↓
Updated Inventory
   ↓
New Data
```

This creates a **continuous inventory intelligence cycle**.

---

## 🔁 CAREX at a Glance

```text
             ┌───────────────┐
             │   INVENTORY   │
             │   + SALES     │
             └───────┬───────┘
                     ↓
             ┌───────────────┐
             │  ANALYSIS &   │
             │  PREDICTION   │
             └───────┬───────┘
                     ↓
          ┌──────────┴──────────┐
          ↓                     ↓
     ┌─────────┐          ┌───────────┐
     │  ALERTS │          │  DEMAND   │
     │         │          │ FORECAST  │
     └────┬────┘          └─────┬─────┘
          │                     │
          └──────────┬──────────┘
                     ↓
             ┌───────────────┐
             │ PROCUREMENT   │
             │ RECOMMENDATION│
             └───────┬───────┘
                     ↓
             ┌───────────────┐
             │ HUMAN REVIEW  │
             └───────┬───────┘
                     ↓
             ┌───────────────┐
             │    ACTION     │
             └───────┬───────┘
                     ↓
             ┌───────────────┐
             │ UPDATED DATA  │
             └───────┬───────┘
                     │
                     └──────→ CONTINUOUS MONITORING
```

> **CAREX transforms healthcare inventory data into timely insights, alerts, and procurement recommendations while keeping final operational decisions under human control.**
