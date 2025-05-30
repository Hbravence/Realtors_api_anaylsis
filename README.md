# 📊 Realtor API Analysis  

### 🔍 Overview  
This project retrieves **New York City real estate data** from **Realtor.com API** and transforms the raw JSON format into a structured **Pandas DataFrame** for further analysis. 
Then, a random forest model is implemented to predict the price of real estate based on several features. 

### 🏡 Data Structure & Processing  
- The API returns **two nested data levels**:  
  1. **Historic Estimated Property Value**  
  2. **Property Characteristics** (e.g., square footage, number of beds/baths, location).  
- **Data Cleaning & Transformation**:  
  - Renamed columns for clarity.  
  - Dropped unnecessary columns to focus on key insights.  
  - Flattened **both nested values separately** before merging.  
  - Grouped historic estimates by **latest available date**, aligned with **property IDs**.  
  - Merged the transformed **historical values** with property data.  
  - Created a **new calculated column** to compare **estimated vs. listed price**.  

### 📈 Correlation Analysis  
- Examined the **relationship between price and key property attributes**:  
  - **Number of beds & baths**  
  - **Square footage**  
- Visualized the correlation using a **scatter plot with a trend line** to assess pricing patterns.

### Random Forest Model
- Put the real estate data through a random forest model for price prediction.
    - Used SQFT, Beds, and Baths for the first model
    - 2nd Model added zip code with an encoder, didn't see any improvements in the model
A future improvement would be to incorporate the neighborhood where the property is listed and see if that is a better predictor of price than the Zip Code.

