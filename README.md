![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-App-black)
![License](https://img.shields.io/badge/license-MIT-green)


🚀 Sample Fuel Traders — Billing & Ledger App

A lightweight GST billing and ledger management system built for small-scale wholesalers to generate invoices, track payments, and visualize outstanding balances — all in one place.

📌 Why this project?

Many small businesses still rely on manual billing or Excel sheets, which leads to:

- Errors in GST calculations  
- Poor tracking of pending payments  
- No clear financial overview

This app solves that by providing a simple, centralized system for billing + ledger tracking.

✨ Features
🧾 Invoice Generation
Create GST-style invoices using weight × rate + GST
⚡ Auto GST Calculation
2.5% CGST + 2.5% SGST automatically applied (configurable)
🧠 Smart Auto-Suggest
Existing company names auto-fill GSTIN
📊 Dashboard with Chart
Visual overview of total / paid / pending amounts (Chart.js)
📒 Per-Company Ledger
Track complete billing history with filters
💰 Partial Payments
Record part-payments and auto-update pending balance
✏️ Edit & Delete Bills
Full CRUD functionality
🖨️ Print-ready Invoice
Clean invoice layout for printing or PDF export
📅 Date Validation
Prevents invalid invoice and weighbridge dates

🛠️ Tech Stack
Backend: Flask
Database: SQLite
Forms & Security: Flask-WTF (CSRF protection)
Frontend: Jinja2, HTML, CSS, Vanilla JS
Charts: Chart.js (local, no CDN)

## 📁 Project Structure

```plaintext
Ajay_Industries/
├── app.py
├── requirements.txt
├── .gitignore
├── database.db
│
├── modules/
│   ├── db.py
│   ├── calculations.py
│   ├── utils.py
│   └── __init__.py
│
├── static/
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       ├── chart.umd.min.js
│       └── script.js
│
└── templates/
    ├── base.html
    ├── form.html
    ├── dashboard.html
    ├── ledger.html
    ├── edit_bill.html
    ├── invoice.html
    └── error.html
```

⚙️ Setup & Installation
git clone https://github.com/khushboobanjara2005-collab/Billing-Sales-Dashboard-System.git

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

pip install -r requirements.txt
python app.py

App will run at:
http://localhost:8000

## 🔄 How It Works
1. Create a bill from the home page  
2. System calculates GST automatically  
3. Bill gets stored in SQLite database  
4. Dashboard aggregates company-level data  
5. Ledger tracks individual transactions and payments  

SECRET_KEY=your-secret-key
Required for CSRF protection. Default key is unsafe for production.

🧾 Configuration
Update business details in:
templates/invoice.html

Edit:
Company Name
Address
GSTIN
Bank Details

🗑️ Optional Cleanup
You can safely remove:
modules/Bill.py (unused script)
bills/ (empty folder)

🚀 Future Improvements
🔐 User authentication (login system)
📄 Export invoices as PDF
☁️ Switch to PostgreSQL (production-ready DB)
📱 Mobile responsiveness improvements
📊 Advanced analytics dashboard
🌐 Live Demo

Add after deployment
https://your-app-link.com

📜 License
MIT License — free to use and modify.
