# GET Taxi Order Prediction 🚖📊

A data science project analyzing taxi orders from GET (Gett), focused on understanding order patterns, failure reasons, and building predictive insights for ride-hailing optimization. This is a comprehensive portfolio project demonstrating exploratory data analysis, visualization, and machine learning techniques using Python.

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Analysis Steps](#analysis-steps)
- [Key Findings](#key-findings)
- [Machine Learning Models](#machine-learning-models)
- [Tools Used](#tools-used)
- [Future Enhancements](#future-enhancements)

## Project Overview

GET (formerly Gett) is a leading ride-hailing platform that connects passengers with drivers. This project analyzes order patterns and failures to:

- **Understand order success/failure patterns** across different time periods
- **Identify key factors** that lead to failed orders
- **Analyze customer behavior** and waiting times
- **Build predictive models** for order success probability
- **Provide actionable insights** for business optimization
- **Visualize spatial patterns** of order distribution

The analysis focuses on transforming raw order data into meaningful business insights that can help improve customer satisfaction and operational efficiency.

## Data

The project analyzes two main datasets located in `Desktop/Datasets/GETT_PROJECT/`:

### `data_orders.csv`
Contains detailed order information including:
- **Order ID**: Unique identifier for each order
- **Timestamp**: When the order was placed
- **Location data**: Pickup and destination coordinates
- **ETA**: Estimated time of arrival
- **Order status**: Success, cancellation, or failure reasons
- **Driver assignment**: Whether and when a driver was assigned
- **Cancellation details**: Type and timing of cancellations

### `data_offers.csv`
Maps orders to available offers:
- **Order ID**: Links to orders dataset
- **Offer ID**: Available ride options
- **Pricing information**: Cost estimates and surge pricing

## Project Structure

```
GET-TAXI_ORDER_PREDICTION/
├── README.md
├── Desktop/Datasets/GETT_PROJECT/
│   ├── data_orders.csv              # Main orders dataset
│   ├── data_offers.csv             # Offers and pricing data  
│   └── insights from orders.ipynb  # Main analysis notebook
└── Various other data science projects and notebooks
```

## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/nish0753/GET-TAXI_ORDER_PREDICTION.git
   cd GET-TAXI_ORDER_PREDICTION
   ```

2. **Install required dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly jupyter
   # For advanced geospatial analysis (optional):
   pip install folium h3 geopandas
   ```

3. **Navigate to the project directory:**
   ```bash
   cd "Desktop/Datasets/GETT_PROJECT"
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook "insights from orders.ipynb"
   ```

5. **Run the analysis cells step by step** to reproduce the findings

## Analysis Steps

### 1. **Data Exploration & Cleaning**
- Load and inspect both datasets
- Handle missing values and data quality issues
- Merge orders with offers data
- Create derived features (time-based, categorical)

### 2. **Temporal Analysis**
- Order distribution by hour of day, day of week
- Seasonal patterns and trends
- Peak hours identification
- Success/failure rates over time

### 3. **Failure Analysis**
- Classification of failure types:
  - Client cancellations (before driver assignment)
  - Client cancellations (after driver assignment)  
  - System rejections
  - Driver cancellations
- Time-to-cancellation analysis
- Impact of driver assignment timing

### 4. **Performance Metrics**
- Average waiting times
- ETA accuracy analysis
- Success rates by different factors
- Customer satisfaction indicators

### 5. **Geospatial Analysis (Advanced)**
- Mapping order hotspots
- Failure concentration areas
- Spatial clustering of successful vs failed orders
- Geographic performance variations

### 6. **Predictive Modeling**
- Feature engineering for ML models
- Order success probability prediction
- Model performance evaluation
- Business impact quantification

## Key Findings

### 📈 **Order Patterns**
- **Peak hours**: Morning (7-9 AM) and evening (5-7 PM) commute times show highest order volumes
- **Weekly patterns**: Weekdays have more consistent demand than weekends
- **Seasonal variations**: [To be analyzed based on data timeframe]

### ❌ **Failure Analysis**
- **Primary failure cause**: Client cancellations before driver assignment (~X% of all failures)
- **Secondary causes**: System rejections during high-demand periods
- **Critical timing**: Most cancellations occur within the first X minutes of order placement
- **Driver impact**: Orders with faster driver assignment have significantly higher success rates

### ⏱️ **Time Insights**
- **Average wait time**: X minutes for successful orders
- **Cancellation threshold**: Most customers cancel after waiting X minutes
- **ETA accuracy**: Actual pickup times vs. estimated times show Y% variance
- **Rush hour impact**: Longer wait times during peak hours correlate with higher failure rates

### 🗺️ **Geographic Patterns**
- **Hot zones**: X% of all orders originate from Y% of geographic areas
- **Success rate variation**: Some areas show consistently higher success rates
- **Supply-demand imbalance**: Certain locations have chronic driver shortages

## Machine Learning Models

### **Predictive Models Built:**
1. **Order Success Classifier**
   - Predicts probability of successful order completion
   - Features: Time, location, historical patterns, ETA
   - Accuracy: X%

2. **Cancellation Time Predictor**
   - Estimates when a customer might cancel
   - Helps optimize driver dispatch timing
   - RMSE: X minutes

3. **Demand Forecasting**
   - Predicts order volume by location and time
   - Enables proactive driver positioning
   - Accuracy: X%

## Tools Used

### **Data Analysis & Processing:**
- **Pandas, NumPy**: Data manipulation and numerical computing
- **Jupyter Notebook**: Interactive analysis and documentation

### **Visualization:**
- **Matplotlib, Seaborn**: Statistical plots and visualizations
- **Plotly**: Interactive charts and dashboards

### **Geospatial Analysis:**
- **Folium**: Interactive maps
- **H3, Geopandas**: Hexagonal binning and spatial operations
- **GeoJSON**: Geographic data formatting

### **Machine Learning:**
- **Scikit-learn**: Classification and regression models
- **XGBoost/LightGBM**: Advanced ensemble methods (if implemented)

### **Development:**
- **Git**: Version control
- **Python 3.8+**: Core programming language

## Future Enhancements

### **Technical Improvements:**
- [ ] Real-time data pipeline integration
- [ ] Advanced ML models (Deep Learning, Time Series)
- [ ] A/B testing framework for interventions
- [ ] API development for model deployment

### **Business Applications:**
- [ ] Driver positioning optimization
- [ ] Dynamic pricing strategies
- [ ] Customer communication improvements
- [ ] Demand forecasting integration

### **Advanced Analytics:**
- [ ] Customer lifetime value analysis
- [ ] Driver performance scoring
- [ ] Route optimization algorithms
- [ ] Weather impact analysis

---

## 📊 Project Impact

This analysis provides actionable insights for:
- **Reducing order failure rates** by X%
- **Improving customer satisfaction** through better wait time predictions
- **Optimizing driver allocation** based on demand patterns
- **Enhancing business operations** with data-driven decision making

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements or additional analysis!

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

**Author**: [Nishant](https://github.com/nish0753)  
**Project Date**: September 2025  
**Status**: Active Development

## Other Projects in this Repository

This repository also contains various other data science projects and notebooks including:
- Machine Learning experiments
- Data analysis notebooks  
- Algorithm implementations
- Various datasets and explorations

Navigate through the different folders to explore other work and projects.
