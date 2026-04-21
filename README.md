# QuantMind: AI-Based Investment Analyst 📈🤖

QuantMind is an AI-powered investment research platform that combines real-time financial data with social sentiment analysis to provide a comprehensive view of market opportunities. It aggregates data from sources like Yahoo Finance and social media, stores it in a MongoDB database, and presents it through a clean, interactive web interface.

## ✨ Key Features

*   **Real-time Financial Data:** Automatically fetches stock prices, fundamentals, and key metrics using the `yfinance` library.
*   **Sentiment Analysis Integration:** Aggregates and scores social sentiment for tracked companies.
*   **MongoDB Data Storage:** Robustly stores financial and sentiment data for quick retrieval and analysis.
*   **Dual Frontend Interface:**
    *   A server-rendered dashboard using **EJS**.
    *   A modern, interactive user interface built with **React**.
*   **RESTful API:** Provides a clean JSON API (`/api/data`) for programmatic access to the data.

## 🛠️ Tech Stack

| Area               | Technologies Used                                                                 |
| ------------------ | --------------------------------------------------------------------------------- |
| **Backend**        | Node.js, Express.js, Mongoose (ODM)                                               |
| **Frontend**       | React (TypeScript), EJS (Embedded JavaScript templates)                            |
| **Data Pipeline**  | Python, yfinance, pandas, numpy                                                   |
| **Database**       | MongoDB Atlas                                                                     |
| **DevOps/Tools**   | npm, pip, Git & GitHub, dotenv                                                    |

## 📁 Project Structure

```text
QuantMind_AI-Based-Investment-Analyst/
├── Database/                 # Python data pipeline
│   ├── .env.example          # (To be created) Template for environment variables
│   ├── api.py                # Fetches and processes data from yfinance
│   └── requirements.txt      # Python dependencies
├── views/                    # Frontend templates and code
│   ├── react/                # React application source (App.tsx, etc.)
│   └── index.ejs             # EJS template for the main dashboard
├── .gitignore                # (To be created) Specifies intentionally untracked files
├── package.json              # Node.js dependencies and scripts
├── package-lock.json         # Exact versioning for Node.js dependencies
├── server.js                 # Main Express.js server
└── README.md                 # You are here!
```

## 🚀 Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for development and testing.

**Prerequisites :**
Node.js (v16 or later recommended)
npm (usually comes with Node.js)
Python (v3.8 or later recommended)
pip (Python package installer)
A MongoDB database (you can use a free cluster on MongoDB Atlas)

**Installation**
Clone the repository

```bash
git clone https://github.com/ShikharNotFound/QuantMind_AI-Based-Investment-Analyst.git
cd QuantMind_AI-Based-Investment-Analyst
```
Install Node.js dependencies

```bash
npm install
```
Set up Python environment and dependencies
```bash
# It's highly recommended to use a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

pip install -r Database/requirements.txt
```

Configure Environment Variables

Copy the example file: cp Database/.env.example Database/.env (on Windows use copy Database\.env.example Database\.env)

Edit Database/.env with your actual MongoDB connection string and database name.

```bash
# Database/.env
MONGO_URI="mongodb+srv://<username>:<password>@your-cluster.mongodb.net/"
DB_NAME="QuantMind"
COLLECTION_NAME="yfinance"


```
Running the Application
Start the Node.js Server

```bash
node server.js
```
The server will start on http://localhost:4000. You should see the following messages in your terminal:

```text
Server running on port 4000
Connected to MongoDB
```
Run the Data Pipeline (Optional)
To populate your database with the latest stock data, open a second terminal window and run:

```bash
python Database/api.py
```
You can set this up as a cron job (or Task Scheduler on Windows) to run periodically (e.g., daily) to keep your data fresh.

Access the Application

Main Dashboard: Open your browser and go to http://localhost:4000

API Endpoint: Access the raw JSON data at http://localhost:4000/api/data

🔌 API Endpoints
Method	Endpoint	Description
GET	/	Serves the main dashboard rendered with EJS.
GET	/api/data	Returns a JSON object containing all stock and social sentiment data.