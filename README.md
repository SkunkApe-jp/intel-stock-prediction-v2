
# Stock Analysis & Market Sentiment System

A full-stack web application that combines machine learning-based stock price prediction with sentiment analysis of financial news and integrated portfolio management. This system provides a simulated trading environment where users can experiment with stock predictions and portfolio strategies in a risk-free setting.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Architecture](#architecture)
- [System Components](#system-components)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project presents a Stock Analysis & Market Sentiment system that integrates customer profiles, stock data, and predictive analytics into one full-stack web application. The system provides simulated buy/sell transactions, fund and dividend tracking, broker commission management, and an admin monitoring dashboard.

On the prediction side, an LSTM-based model (with classical ARIMA and Linear Regression baselines) forecasts future stock trends using historical prices, while a sentiment analysis module aggregates recent financial-news sentiment to give additional context. The backend is implemented in Python using Flask, with a SQLite database and responsive web interfaces, and the prediction outputs are visualised through interactive D3-based charts and summary widgets on the results page.

The proposed system is intended for students, researchers, and amateur investors who wish to explore stock prediction and portfolio management in a safe, simulated environment. It closes gaps in the literature by embedding forecasting models into an end-to-end management workflow with explainable dashboards rather than providing prediction in isolation.

## Key Features

### Portfolio Management
- User registration and authentication with role-based access control
- Virtual wallet and fund tracking for simulated trading
- Stock buy/sell operations with commission calculations
- Dividend recording and tracking
- Portfolio holdings visualization and performance metrics

### Prediction Engine
- LSTM neural network for stock price prediction
- Classical baseline models (ARIMA, Linear Regression)
- Financial news sentiment analysis using multiple sources
- Interactive visualization of prediction accuracy
- Seven-day forward price forecasting

### Administration
- User and company management
- Broker configuration with commission rates
- Transaction monitoring and reporting
- System statistics dashboard

## Technology Stack

### Backend
- **Python** - Core programming language
- **Flask** - Web framework
- **SQLite** - Database management
- **SQLAlchemy** - ORM for database operations

### Machine Learning & Analytics
- **TensorFlow/Keras** - Deep learning framework
- **Scikit-learn** - Machine learning algorithms
- **Statsmodels** - Statistical modeling (ARIMA)
- **NLTK** - Natural language processing
- **TextBlob/FinVADER** - Sentiment analysis
- **YFinance** - Stock market data retrieval
- **Alpha Vantage** - Financial data API

### Frontend
- **HTML5/CSS3** - Markup and styling
- **Bootstrap** - Responsive design framework
- **JavaScript** - Client-side interactivity
- **D3.js** - Data visualization
- **jQuery** - DOM manipulation

## Architecture

The system follows a three-tier architecture:

1. **Presentation Layer**: Responsive web interface built with HTML, CSS, Bootstrap, and JavaScript
2. **Application Layer**: Python/Flask backend implementing business logic, prediction models, and data processing
3. **Data Layer**: SQLite database managed through SQLAlchemy ORM

## System Components

### Database Schema
The system uses a relational database with the following key entities:
- **User**: Authentication and profile information
- **Company**: Stock information and metadata
- **Broker**: Commission configuration
- **PortfolioItem**: User holdings tracking
- **Transaction**: Buy/sell records with commission tracking
- **Dividend**: Dividend payout records

### Prediction Models
Three predictive models are implemented:
1. **LSTM Neural Network**: Deep learning model for complex pattern recognition
2. **ARIMA**: Classical statistical model for time series forecasting
3. **Linear Regression**: Simple baseline model for comparison

### Sentiment Analysis
Financial news sentiment is gathered from multiple sources:
- Finviz scraping with FinVADER sentiment analysis
- Alternative news sources as fallbacks
- Aggregation of sentiment scores over time windows

## 🚀 Quick Start for New Users

If you're downloading or cloning this project for the first time, follow these steps immediately:

### 1. Install Python 3.7+
Make sure you have Python installed. Download from [python.org](https://www.python.org/downloads/)

### 2. Create a Virtual Environment
```bash
python -m venv venv
# On Windows:
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. Install All Dependencies (CRITICAL)
```bash
pip install -r requirements.txt
```

### 4. Create Admin Account (Required for Dashboard Access)
```bash
# On Windows:
.\venv\Scripts\python create_admin.py
# On Mac/Linux:
python3 create_admin.py
```
This creates the default admin account: `admin@example.com` / `admin123`

### 5. Run the Application
```bash
# On Windows:
.\venv\Scripts\python main.py
# On Mac/Linux:
python3 main.py
```

### 6. Open in Browser
Go to: http://localhost:5000

---

## Installation

### Prerequisites
- Python 3.7+
- pip package manager

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/SkunkApe-jp/intelligent-stock-prediction-forked.git
cd intelligent-stock-prediction
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the application:
```bash
python main.py
```

5. Access the application at `http://localhost:5000`

### Default Credentials
- **Admin User**: 
  - Username: admin
  - Email: stockpredictorapp@gmail.com
  - Password: Samplepass@123

## Usage

### For Regular Users
1. Register a new account or log in with existing credentials
2. Explore the dashboard to view wallet balance and portfolio holdings
3. Use the prediction feature to analyze stock trends
4. Perform simulated buy/sell transactions
5. Record dividend payouts
6. Monitor portfolio performance

### For Administrators
1. Log in with admin credentials
2. Manage users, companies, and brokers through the admin panel
3. Configure commission rates
4. Monitor system statistics and transaction logs
5. View overall system performance metrics

## Project Structure

```
intelligent-stock-prediction/
├── main.py                 # Flask application entry point
├── news_sentiment.py       # Sentiment analysis implementation
├── requirements.txt        # Python dependencies
├── templates/              # HTML templates
├── static/                 # CSS, JavaScript, and static assets
├── docs/                   # Documentation and diagrams
├── tests/                  # Test suite
├── demos/                  # Demonstration scripts
├── screenshots/            # Application screenshots
└── README.md               # This file
```

## Documentation

Comprehensive documentation is available in the `docs/` directory:

- [Draft Report](docs/draft-report.md) - Complete project documentation
- [Diagrams](docs/diagrams/) - System architecture and design diagrams
- [Advanced Features](docs/ADVANCED_FEATURES.md) - Detailed feature descriptions
- [Testing Framework](docs/COMPREHENSIVE_TESTING_FRAMEWORK.md) - Testing methodologies
- [API Keys Guide](docs/API_KEYS_GUIDE.md) - Configuration instructions

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution.

### How to Contribute
1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

