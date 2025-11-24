# 💸 AI Financial Planner – HackMTY 2024

A Streamlit application that simulates financial data, analyzes spending behavior, forecasts expenses, and generates personalized financial plans using the OpenAI API.

## 🚀 Overview

This project implements an **AI-powered personal finance assistant** that:

- Simulates structured financial data (accounts, transactions, loans, bills)
- Performs automated financial analytics
- Generates personalized financial recommendations using LLMs
- Visualizes insights interactively (spending patterns, savings rate, forecasted expenses)

Built using:
- **Streamlit** for the interactive UI  
- **OpenAI API** (gpt-3.5-turbo) for data simulation + financial planning  
- **Pandas** for data handling  
- **Plotly** for visual analytics  

---

## 🧠 Core Technical Components

### 1. **Financial Data Simulation (LLM-Driven)**
`simulate_nessie_data(user_id)`

- Enforces **valid JSON output** using system prompt constraints  
- Generates synthetic but realistic:
  - Accounts with balances  
  - Recent transactions with categories  
  - Loans with interest rates  
  - Pending bills  
- Includes error handling for malformed JSON  
- Uses OpenAI’s Chat Completions API  

### 2. **Spending Pattern Extraction**
`analyze_spending_patterns(transactions)`

- Categorizes withdrawals  
- Computes total spending per category  
- Data transformed into Plotly pie chart  

### 3. **Savings Rate Computation**
`calculate_savings_rate(transactions)`

Formula:
