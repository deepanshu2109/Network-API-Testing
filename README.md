# Network-API-Testing

🚀 Cisco SD-WAN API Test Automation
This project automates API testing for Cisco SD-WAN vManage using Python, Pytest, and Docker. It authenticates with Cisco's vManage sandbox, retrieves device inventory, performs negative testing, and generates HTML and Allure reports with code coverage.

📦 Features
🔐 Login to Cisco vManage via APIs

📋 Fetch SD-WAN device inventory

✅ Positive and Negative Test Cases

📊 Pytest HTML & Allure Reporting

☁️ Dockerized for CI/CD Compatibility

📈 Code Coverage with pytest-cov

🛠️ Tech Stack
Python 3.10

Pytest

Requests

Pytest-HTML

Allure Pytest

Docker + Docker Compose

📁 Project Structure
bash
Copy
Edit
.
├── auth.py                # vManage login & token fetch
├── api_helper.py          # Generic GET method
├── get_inventory.py       # Manual script to print devices
├── tests/
│   ├── test_inventory.py  # Positive test for inventory
│   ├── test_negative.py   # Invalid auth / bad endpoint
│   └── test_token.py      # Token retrieval test
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── reports/               # HTML & Allure reports
└── README.md
🚀 How to Run
🔹 Local (venv)
bash
Copy
Edit
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run tests with HTML report
pytest tests/ --html=report.html --self-contained-html --cov=. --cov-report=html
🔹 Docker
bash
Copy
Edit
docker-compose up --build
📈 Reports
✅ report.html – Pytest test results

🧪 htmlcov/index.html – Code coverage

📊 reports/allure-report/index.html – Allure dashboard

🔐 Cisco Sandbox Used
URL: https://sandbox-sdwan-2.cisco.com

Username: admin

Password: C1sco12345

You must have access to Cisco DevNet to use this sandbox.
