<!--
  CleverMart – README.md
  A modern AI-powered Smart Shop platform built on the Microsoft Power Platform
-->

<h1 align="center">
  🛒 CleverMart
  <br>

  <sub><em>AI-powered Smart-Shop Platform</em></sub>

  <img src="sources/CleverMart_500x250.png" />
</h1>

<p align="center">
  <a href="[https://make.powerapps.com](https://apps.powerapps.com/play/e/5032ff4d-3526-eec9-9323-ffdc94589e4f/a/109defef-1f4f-4870-8634-701203318ea8?tenantId=23e9f3d3-e0d0-4d38-b8cf-44b82c7fabdb&hint=8b472384-d5c0-4702-ba51-4081179c3f12&sourcetime=1753201026825&source=portal#)">Power Apps</a> •
  <a href="https://powerautomate.microsoft.com">Power Automate</a> •
  <a href="[https://copilotstudio.microsoft.com](https://web.powerva.microsoft.com/environments/5032ff4d-3526-eec9-9323-ffdc94589e4f/bots/58a592be-f366-f011-bec2-6045bd886c2f/overview)">Copilot Studio</a> •
  <a href="https://learn.microsoft.com/power-platform">Microsoft Power Platform</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20Apps-Low%20Code-742774?logo=microsoftpowerapps&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" />
  <img src="https://img.shields.io/github/last-commit/YOUR-ORG/clevermart" />
</p>

---

## ✨ What is CleverMart?

*CleverMart* is a dual-mode shop-management solution:

| Role            | Experience                                                         |
|-----------------|--------------------------------------------------------------------|
| **Business Owner** | Manage products, inventory, vendors, and sales analytics—right from Power Apps |
| **Customer**        | Scan a QR code and chat/voice with an AI assistant to browse items, place orders, and receive invoices |

Behind the scenes, Copilot Studio serves as the **virtual General Manager**, while Power Automate orchestrates orders, invoicing, and stock alerts.

---

## 📸 Screenshots

| Owner Dashboard | Customer Chatbot |
|-----------------|------------------|
| ![](docs/screenshot-dashboard.png) | ![](docs/screenshot-chatbot.png) |

*(replace the `docs/` images with your own)*

---

## 🏗 Architecture

```text
Power Apps (Canvas)  <--->  SharePoint Lists ─ Products / Orders / Vendors / Customers
        │
        ├─ Power Automate flows  (order-to-invoice, stock alerts, QR generation)
        │
        └─ Copilot Studio agent “CleverMart GM” (chat / voice)
                 │
                 └─ Azure Cognitive Services  (Speech, TTS)
Data model: see /solution/CleverMart_DataModel.drawio.

🚀 Getting Started
1. Prerequisites
Power Apps licence with AI Builder credits

Environment roles: Environment Maker + AI Builder User

SharePoint site (or Dataverse) for backend lists

2. Setup Steps
shell
Copy
Edit
# 1. Import the managed solution (Settings → Solutions → Import)
# 2. Configure environment variables (SharePoint URLs, list IDs)
# 3. Run the 'Provision Lists' flow to create demo data
# 4. Share the Canvas app with users (Owner and Customer roles)
# 5. Publish Copilot Studio agent and test chat/voice
See docs/deployment-guide.md for a full walkthrough.

🧩 Tech Stack
Layer	Tech
Frontend	Power Apps Canvas (Tablet)
Automation	Power Automate (cloud flows)
AI	Copilot Studio (Power Virtual Agents) + Azure Speech
Data	SharePoint Lists (Products, Orders, Inventory, etc.)
Analytics	Power BI Embedded

🙌 Contributing
Fork the repo & create your branch: git checkout -b feature/awesome

Commit your changes: git commit -m "Add awesome feature"

Push and open a Pull Request

We follow Conventional Commits and run solution checker before PR approval.


❤️ Acknowledgements
Microsoft Power Platform community

Open-source icon libraries (Fluent UI, Hero Icons)

Inspiration from retail analytics best practices

Need help?
• Open an issue • ping @YourName in discussions • or drop us a message on <your Slack/Discord>
