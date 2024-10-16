# Data-Driven Optimization of Pricing Strategies for Retail

## Overview

This project addresses the challenges faced by online fashion retailers in optimizing pricing strategies. By developing data-driven models using machine learning algorithms, this research aims to improve price elasticity estimates, predict sales volume, evaluate discount effectiveness, and forecast demand. The ultimate goal is to optimize pricing strategies to balance profitability with customer satisfaction and efficient inventory management.

## Research Objectives

1. **Price Elasticity of Demand Model**  
   Build machine learning models to quantify the impact of price changes on demand, helping identify optimal pricing points to maximize revenue without losing customers.

2. **Sales Volume Prediction Model**  
   Develop a model to predict how changes in price, promotions, and other factors affect the number of units sold. This model will help optimize pricing strategies and promotional activities.

3. **Discount Effectiveness & Promotional Uplift Model**  
   Create a model to evaluate the true impact of discounts and promotions, distinguishing whether they increase sales or simply shift demand from future periods.

4. **Demand Forecasting Model**  
   Design a time-series model to forecast future demand based on historical sales data. This model will help retailers manage inventory and make better pricing decisions.

5. **Comparative Analysis of Machine Learning Models**  
   Conduct a comparative analysis of various machine learning models to identify the most suitable models for retail fashion pricing strategies, focusing on accuracy, real-time application suitability, and complexity versus performance.

## Domain Area and Problem Area

### Domain Area
- **Machine Learning Modeling for Prediction**

### Problem Area
- **Pricing Strategy Optimization**

Retailers often struggle with setting the right price for products, which can lead to either undercharging or overcharging. This issue is particularly prominent in online fashion, where diverse product categories and dynamic demand patterns exist. The study tackles several key issues:

- **Price Sensitivity**: Quantifying how price changes impact demand and identifying optimal price points.
- **Promotional Cannibalization**: Determining if promotions lead to an actual increase in sales or simply shift future demand.
- **Demand Forecasting**: Enhancing the accuracy of demand forecasting to reduce overstock or stockouts.
- **Cross-Product Influence**: Understanding how the price of one product influences demand for related products (e.g., substitutes or complements).

## Data

The dataset used for this study consists of historical sales and pricing data from an online fashion retailer (https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data/data). 

It includes features such as:
- Product prices
- Sales volumes
- Promotions
- Inventory levels
- Seasonal trends

## Models and Tools Used

- **Price Elasticity of Demand**: Machine learning regression models to quantify the effect of price changes on demand (Linear, Log-Log, Lasso, Ridge)
- **Sales Volume Prediction**: Gradient Boosting, XGBoost, and other regression models to predict units sold. (XGBoost, Light GBM)
- **Discount Effectiveness**: Propensity Score Matching and Causal Inference methods to evaluate promotional impact. (PSM, DiD, XGBoost, Light GBM) 
- **Demand Forecasting**: Time-series models like ARIMA, SARIMA, and Prophet to predict future sales and demand. (SARIMA, Prophet, LSTM)
- **Comparative Model Analysis**: Evaluate models based on accuracy, suitability for real-time applications, and trade-offs between complexity and performance.

  ## Results

- **Price Elasticity**: 
    - Log-Log Regression performed best in minimizing errors (MSE and MAE), though it explained less variance than Linear, Lasso, and Ridge, which had stronger R-squared values. 
- **Sales Volume Prediction**: 
    - LightGBM outperformed XGBoost, with lower MSE and MAE, proving more effective in handling complex interactions between price, promotions, and sales volume. 
- **Discount Effectiveness**: 
    - XGBoost and LightGBM predicted promotional uplift well, while PSM and DiD provided more insights into causal effects, revealing whether promotions genuinely increase sales or cannibalize future demand. 
- **Demand Forecasting**: 
    - Prophet excelled in forecasting demand, capturing seasonality and trends more effectively than SARIMA. LSTM underperformed, likely due to the dataset's short-term nature. 

## Conclusions

- **Best Models**: 
    - LightGBM and XGBoost proved most effective for predicting sales volume and capturing demand fluctuations. Linear and Ridge Regression performed well for simple, real-time applications, while Log-Log captured non-linear relationships better.
- **Promotional Insights**: 
    - PSM and DiD helped identify the true causal impact of promotions, revealing if they led to genuine sales increases or shifted demand from future periods.
- **Demand Forecasting**: 
    - Prophet emerged as the best model for capturing future demand trends, essential for optimizing inventory levels in retail.

Each pricing strategy brings distinct value to fashion retail companies:
- Price elasticity analysis helps retailers determine optimal pricing to maximize revenue without alienating customers.
- Sales volume prediction models like XGBoost and LightGBM offer accurate forecasting of sales, enabling better inventory management and pricing adjustments.
- Discount effectiveness models, such as PSM and DiD, ensure that promotions lead to genuine sales growth rather than cannibalizing future demand.
- Demand forecasting with Prophet helps companies align their inventory and pricing strategies with future demand trends, ensuring they are prepared for both peak and off-peak periods.

## Future Work

- **Hyperparameter Tuning**: 
    - Optimizing XGBoost and LightGBM through techniques like Bayesian Optimization could further improve performance.
- **Advanced Models**: 
    - Testing Random Forest, Neural Networks, or LSTM with larger datasets may provide additional insights.
- **Real-time A/B Testing**: 
    - Conducting live retail experiments will help validate the models' practical applications, ensuring they work in dynamic retail environments.

## How to Use

1. Clone this repository:  
   ```bash
   git clone https://github.com/clarabeldarrain/retail-pricing-optimization.git

