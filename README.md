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
(income − expenses) / income

- Income = deposits  
- Expenses = withdrawals  

Displayed as a Streamlit KPI metric.

### 4. **Short-Term Expense Forecasting**
`predict_future_expenses(transactions, months_ahead=3)`

- Computes average daily spending  
- Scales to monthly spending  
- Applies incremental projected growth (+2% per month)
- Outputs a time series for Plotly line chart  

### 5. **AI-Generated Financial Plan**
`generate_financial_plan(simulated_data, user_goal)`

- Sends structured user financial profile to GPT  
- Produces a detailed personalized plan including:
  - Spending diagnosis
  - Savings optimization strategies
  - Debt management guidelines
  - Practical, actionable recommendation  

### 6. **Follow-Up Q&A Assistant**

- Users can ask questions about their finances  
- GPT responds using contextual data from the simulation  
- Custom prompt injection ensures responses are personalized  

