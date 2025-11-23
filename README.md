# Financial-Advisor---HackMty24
This is the project developed for Capital One Finance challenge in MackMTY 2024.

## Overview

This project is a comprehensive financial planning tool that leverages AI to provide personalized financial insights and advice. Developed as part of a hackathon, it combines data simulation, machine learning, and natural language processing to offer users a unique and interactive financial planning experience.

## Features

- **Financial Data Simulation**: Uses OpenAI's GPT-3.5 API to generate realistic financial profiles for users, including multiple accounts, transactions, loans, and bills.
- **Expense Forecasting**: Implements LSTM networks to predict future expenses based on simulated historical data.
- **Interactive Dashboard**: Utilizes Plotly Express to create visually appealing charts and graphs for financial data visualization.
- **Personalized Financial Advice**: Integrates OpenAI's API to generate tailored financial plans and answer user queries.
- **Real-time Updates**: Optimized for quick response times, allowing for dynamic updates based on user input and simulated market conditions.

## Technologies Used

- Python
- Streamlit
- OpenAI API
- Plotly Express
- Pandas
- TensorFlow (for LSTM implementation)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/financial-planning-tool.git
   ```

2. Navigate to the project directory:
   ```
   cd financial-planning-tool
   ```

3. Set up your OpenAI API key:
   - Create a `.env` file in the root directory
   - Add your API key: `OPENAI_API_KEY=your_api_key_here`

## Usage

1. Run the Streamlit app:
   ```
   streamlit run app.py
   ```

2. Open a web browser and go to `http://localhost:8501`

3. Enter a user ID to simulate financial data and explore the features of the tool.

## Project Structure

- `app.py`: Main Streamlit application
- `data_simulation.py`: Functions for simulating financial data using OpenAI API
- `analysis.py`: Data analysis and financial metrics calculation
- `forecasting.py`: LSTM model for expense prediction
- `visualization.py`: Plotly Express charts and graphs
- `utils.py`: Utility functions and helpers


## Acknowledgments

- Thanks to the hackathon organizers for the opportunity to develop this project.
- Special thanks to OpenAI for providing the GPT-3.5 API used in this project.

