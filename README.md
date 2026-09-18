CAREX --- AI-Powered Healthcare Inventory Intelligence

CAREX is a healthcare inventory management and intelligence
platform designed for pharmacies, hospitals, and clinics. It helps
monitor medicine stock, predict demand, identify expiry risks, track
sales, support procurement decisions, and surface AI-driven alerts.

🚀 Overview

Managing healthcare inventory involves more than simply counting
medicines. Stock-outs, overstocking, expiry, changing demand, and
delayed procurement can directly affect operational efficiency.

CAREX brings these activities into a single dashboard and adds an
intelligence layer that helps users identify what needs attention.

The system is designed around a simple workflow:

Monitor → Predict → Alert → Review → Approve → Act

✨ Key Features

📊 Operations Dashboard

Total active medicines

Today's sales and units sold

Low-stock count

Medicines expiring soon

Pending procurement requests

Live AI alerts

Weekly demand overview

AI priority levels: Urgent, High, Medium, Low

Quick report generation

💊 Medicine Inventory

Medicine and batch-level inventory

Current stock visibility

Minimum-stock threshold

Safety-stock information

Expiry status

Supplier details

Priority classification

Demand prediction for the next 7 days

Add-stock workflow

🧾 Sales & Billing

Select a medicine and batch

Enter quantity sold

Record transactions

Maintain recent transaction history

Connect sales activity with inventory monitoring

⏳ Expiry Monitoring

Identify medicines approaching expiry

Display expiry warnings

Track individual batches

Generate alerts for medicines requiring review

🚨 AI Alerts

CAREX can surface operational events such as: - Low stock detected -
Expiry warning - Unusual sales activity

Example:

Sales volume is significantly higher than the normal average,
triggering an unusual-activity alert.

📦 Intelligent Procurement

Review suggested orders

View current stock

Compare forecast demand and safety stock

View supplier and lead time

Generate suggested order quantity

Assign procurement priority

Approve / Hold / Escalate procurement requests

🤖 CAREX AI Assistant

The integrated assistant can answer inventory-related questions using
available system data.

Example:

User: Which medicine has the highest demand?

CAREX: Paracetamol has the highest sales this week with 126 units
sold.

This provides a conversational way to access inventory insights without
manually checking multiple screens.

⚙️ Configurable Inventory Rules

The settings module provides configurable inventory parameters such
as: - Minimum stock threshold - Safety stock - Expiry warning period -
Auto-order mode

The prototype uses the following planning logic:

Required Stock =
Forecast Demand During Planning Period
+ Safety Stock
+ Expected Demand During Supplier Lead Time

Suggested Order =
max(0, Required Stock - Available Stock)

🖥️ Interface

CAREX uses a clean, healthcare-oriented interface with: - Responsive
dashboard cards - Clear status and priority badges - Data tables for
inventory and procurement - Visual demand prediction - Notification
indicators - AI assistant panel - Approval-oriented workflows

Main Screens

Module        Purpose

Dashboard     Overall operations and AI overview
Inventory     Medicine and batch management
Sales         Sales and billing transactions
Expiry        Expiry monitoring
Alerts        AI-generated operational alerts
Procurement   Stock replenishment and approval
Analytics     Inventory and demand insights
Settings      Inventory configuration

🔄 System Workflow

                    ┌─────────────────────┐
                    │   Medicine Data     │
                    │ Stock / Batch /     │
                    │ Sales / Expiry      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   CAREX Engine      │
                    │ Monitoring +         │
                    │ Forecasting + Rules  │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
        ┌───────────┐   ┌────────────┐   ┌────────────┐
        │ Low Stock │   │   Expiry   │   │  Demand    │
        │ Detection │   │ Monitoring │   │ Prediction │
        └─────┬─────┘   └─────┬──────┘   └─────┬──────┘
              │               │                │
              └───────────────┼────────────────┘
                              ▼
                    ┌─────────────────────┐
                    │    AI Alerts &      │
                    │    Prioritization   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Procurement Review  │
                    │ Approve / Hold /    │
                    │ Escalate            │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Inventory Updated   │
                    └─────────────────────┘

🧠 Intelligence Layer

CAREX is designed to move from reactive inventory management to
proactive inventory intelligence.

1. Demand Prediction

Historical/transaction data can be used to estimate upcoming medicine
demand.

2. Low-Stock Detection

Current stock is compared against configured inventory thresholds and
planning requirements.

3. Expiry Risk Detection

Batch expiry dates are monitored so medicines approaching expiry can be
reviewed early.

4. Unusual Sales Detection

Current sales activity can be compared with normal sales patterns to
identify unusual demand.

5. Procurement Recommendation

The system calculates a suggested order quantity using forecast demand,
safety stock, available inventory, and supplier lead time.

6. Priority Classification

Inventory events can be organized into:

🔴 Urgent

🟠 High

🔵 Medium

🟢 Low

This helps users focus on the events requiring the earliest review.

👥 User Roles

Admin

Designed for administrative control and overall system monitoring.

Pharmacist

Designed for day-to-day inventory operations, sales, alerts, expiry
review, and procurement workflows.

Role permissions can be extended as the system evolves.

🛠️ Tech Stack

Update this section with the exact technologies used in your
implementation.

Suggested structure:

Frontend: [React / HTML-CSS-JS / other]

Backend: [Node.js / Python / Java / other]

Database: [MySQL / PostgreSQL / MongoDB / other]

AI / ML: [Model or framework used]

APIs: [REST API / FastAPI / Express / other]

Authentication: [Authentication method]

Deployment: [Vercel / Render / AWS / other]


⚙️ Installation & Setup

1. Clone the repository

git clone <YOUR-GITHUB-REPOSITORY-URL>
cd CAREX

2. Install dependencies

Use the commands required by your selected frontend/backend stack.

Example:

npm install

3. Configure environment variables

Create a .env file and add the required configuration:

DATABASE_URL=your_database_url
API_URL=your_api_url
AI_API_KEY=your_ai_api_key

Do not commit real API keys, passwords, database credentials, or
other secrets to GitHub.

4. Run the application

Use the appropriate development command for your implementation.

Example:

npm run dev

📸 Screenshots

Login

The CAREX login screen provides separate access paths for administrative
and pharmacist users.

Dashboard

The dashboard provides a consolidated view of stock, sales, expiry,
procurement, and AI alerts.

Inventory

The inventory module displays medicine, batch, stock, threshold, safety
stock, expiry, and supplier information.

Procurement

The procurement screen provides AI-assisted suggested order quantities
and an approval workflow.

Alerts

The alerts screen brings important inventory events into one place,
including low stock, expiry, and unusual sales activity.

Sales & Billing

The sales screen allows users to record medicine transactions and review
recent sales.

Place the project screenshots inside a screenshots/ folder and
uncomment the image links below.

![CAREX Login](screenshots/login.png)
![CAREX Dashboard](screenshots/dashboard.png)
![CAREX Inventory](screenshots/inventory.png)
![CAREX Procurement](screenshots/procurement.png)
![CAREX Alerts](screenshots/alerts.png)
![CAREX Sales](screenshots/sales.png)

📈 Example Inventory Scenario

Suppose a medicine has:

Current Stock       = 240 units
Forecast Demand    = 300 units
Safety Stock        = 50 units
Supplier Lead Time = 7 days

CAREX uses the configured forecasting and replenishment logic to
determine whether additional stock should be reviewed and generates a
suggested procurement quantity.

The procurement screen then presents the recommendation to an authorized
user for:

Approve  →  Hold  →  Escalate

This keeps the system decision-support oriented, rather than
automatically placing an order without review.

🎯 Objectives

CAREX aims to:

Reduce medicine stock-out risk

Improve visibility of inventory levels

Identify expiry risks earlier

Support demand-aware procurement

Detect unusual sales patterns

Reduce manual inventory monitoring

Provide actionable alerts

Help pharmacists and administrators make faster operational
decisions

🔮 Future Enhancements

Potential future improvements include:

Advanced time-series demand forecasting

Multi-location inventory management

Supplier performance analytics

Purchase-order integration

Barcode/QR-based stock entry

Automated batch tracking

Role-based access control

Audit logs

Real-time database synchronization

Advanced analytics and reporting

Mobile application

Integration with pharmacy/hospital management systems

Explainable AI recommendations

Automated notification channels

🔐 Security Considerations

Because CAREX is designed for healthcare environments, production
deployment should include:

Secure authentication

Role-based authorization

Encrypted data transmission

Secure secret management

Database access controls

Audit logging

Input validation

Protection against common web vulnerabilities

Appropriate handling of sensitive healthcare data

The current project should be treated as a prototype/demo unless
production-grade security and compliance requirements have been
implemented and verified.

🧪 Project Status

Status: 🚧 Prototype / Development

CAREX currently demonstrates the core user experience and
inventory-intelligence workflow through dashboard, inventory, sales,
alerts, procurement, and configuration modules.

🤝 Contributing

Contributions are welcome.

Fork the repository

Create a feature branch

git checkout -b feature/your-feature

Commit your changes

git commit -m "Add your feature"

Push the branch

git push origin feature/your-feature

Open a Pull Request

📄 License

Add the license appropriate for your project.

Example:

MIT License

👩‍💻 Team

CAREX --- AI Inventory Intelligence

Built as a software project focused on applying AI-assisted monitoring
and forecasting to healthcare inventory operations.

Add your team members, institution, GitHub profiles, and project links
here.

⭐ Support

If you find CAREX useful, consider giving the repository a ⭐ on GitHub.
