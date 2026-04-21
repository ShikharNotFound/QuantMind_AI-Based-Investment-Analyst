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