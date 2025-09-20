# Healthcare Spending Survey Application

A full-stack web application built with Flask, MongoDB, and Nginx for collecting and analyzing healthcare spending data. Deployed on AWS EC2 for production use.

## 🚀 Live Demo
**Application URL:** http://13.50.112.196/  
**GitHub Repository:** https://github.com/williamz6/flask-healthcare-app.git

## 📋 Project Overview

This application was developed for a healthcare company to collect and analyze income and spending patterns of participants. The tool helps in market research for a new healthcare product launch.

### Key Features
- **Web Form**: User-friendly survey form for data collection
- **MongoDB Storage**: Secure cloud database storage
- **Data Processing**: Python-based data processing and CSV export
- **Data Visualization**: Jupyter Notebook analysis with charts and insights
- **AWS Deployment**: Production-ready deployment on Amazon EC2
- **Responsive Design**: Works across desktop and mobile devices

## 🏗️ Architecture
User → Nginx (Reverse Proxy) → Gunicorn (WSGI Server) → Flask (Web Framework) → MongoDB (Database)


## 📁 Project Structure
survey-app/
├── app.py # Main Flask application
├── requirements.txt # Python dependencies
├── readme.md 
├── user.py # User class and data processing
|--- mongo_handler.py # MongoDB connection handler
├── templates/ # HTML templates
│ ├── index.html # Survey form
├── static/ # Static assets
│ └── style.css # CSS styles
├── data_processing/ # Data processing scripts
│ analysis.ipynb # Jupyter Notebook analysis
├── export_to_csv # Exported survey data
├── charts/ # Visualization exports
│ ├── age_income_analysis.png
│ ├── gender_spending_analysis.png
│ └── healthcare_age_scatter.png
└── README.md # This file


## 🛠️ Technology Stack

- **Backend**: Python 3.12, Flask 2.3.3
- **Database**: MongoDB Atlas (Cloud)
- **Web Server**: Nginx 1.24.0
- **WSGI Server**: Gunicorn 23.0.0
- **Infrastructure**: AWS EC2 (Ubuntu 22.04)
- **Data Analysis**: Pandas, Matplotlib, Jupyter Notebook
- **Visualization**: Seaborn, Matplotlib

## 📊 Data Collection

The survey collects the following information:
- **Demographics**: Age, Gender
- **Financial Data**: Total Monthly Income
- **Expense Categories**:
  - Utilities
  - Entertainment  
  - School Fees
  - Shopping
  - Healthcare

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8+
- MongoDB Atlas account
- AWS EC2 instance (Ubuntu)
- Nginx

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/williamz6/flask-healthcare-application.git
   cd flask-healthcare-application
   ```
2. **Create Virtual environment**
   ```bash
   python3 -m venv env
   source env/bin/activate
   ```
3. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Set up environment variables** 
    ```bash
    export MONGODB_USER="your_mongodb_user"
    export MONGODB_PASSWORD="your_mongodb_password"
    export MONGODB_CLUSTER="your_cluster_address"
    ```
5. **Run the application**
   ```bash
   python app.py
   ```
### Production Deployment on AWS

1. **Launch EC2 Instance**
     - Ubuntu 22.04 LTS
     - t2.micro or larger
     - Security groups: HTTP (80), HTTPS (443), SSH (22)
  
2. **Server Setup**
   ```bash
   sudo apt update
    sudo apt install python3-pip nginx mongodb
   ```

3. **Deploy Application**
   ```bash
   git clone https://github.com/williamz6/flask-healthcare-application.git
   cd flask-healthcare-application
   python3 -m venv env
   source env/bin/activate
   pip install -r requirements.txt
   ```
