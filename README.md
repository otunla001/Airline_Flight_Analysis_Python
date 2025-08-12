# ✈ Airline Flight Price Analysis  

This project is an **Exploratory Data Analysis (EDA)** of an airline flights dataset using **Python** in Jupyter Notebook.  
The goal is to uncover trends and patterns in **flight prices**, **routes**, and **travel behavior**, while identifying factors that influence ticket costs.  

---

## 📂 Dataset Overview  

The dataset contains detailed flight information with the following columns:

| Column | Description |
|--------|-------------|
| **index** | Row index |
| **airline** | Name of the airline |
| **flight** | Flight identifier |
| **source_city** | Departure city |
| **departure_time** | Time of departure (categorical) |
| **stops** | Number of stops (e.g., non-stop, 1 stop) |
| **arrival_time** | Time of arrival (categorical) |
| **destination_city** | Arrival city |
| **class** | Ticket class (e.g., Business, Economy) |
| **duration** | Total travel duration |
| **days_left** | Days left before departure |
| **price** | Ticket price |

---

## 🛠 Tools & Libraries Used  

- **Python**
- **Pandas** – data manipulation & cleaning  
- **Matplotlib** & **Seaborn** – visualizations  
- **Jupyter Notebook** – interactive analysis  

---

## 🔍 Analysis & Insights  

### 1️⃣ Descriptive Statistics  
- Used `df.describe()` to view numeric summaries (mean, median, min, max, quartiles)  
- Used `df.describe(include='object')` to summarize categorical features  

---

### 2️⃣ Correlation with Price  
- Identified **top 5 positive correlations** with `price`  
- Identified **top 5 negative correlations** with `price`

## 📈 Top 5 Positively Correlated Attributes to Price  

| Attribute          | Correlation |
|--------------------|-------------|
| class_Business     | 0.937860    |
| airline_Vistara    | 0.360816    |
| duration           | 0.204222    |
| stops_one          | 0.199913    |
| airline_Air_India  | 0.070041    |

---

## 📉 Top 5 Negatively Correlated Attributes to Price  

| Attribute         | Correlation |
|-------------------|-------------|
| airline_AirAsia   | -0.176188   |
| stops_zero        | -0.187277   |
| airline_GO_FIRST  | -0.194179   |
| airline_Indigo    | -0.280882   |
| class_Economy     | -0.937860   |
 

📌 **Key Finding:**  
Features like **class_Business** and **class_Economy** strongly influence price. 

---

### 3️⃣ Price Extremes  
- **Most Expensive Flights** – Top 5 flights with highest fares (mostly business class, long-duration routes)  
- **Cheapest Flights** – Top 5 flights with lowest fares (mostly economy class, short-duration routes)  
## 💰 Most Expensive Flights  

| Index   | Airline | Class    | Duration (hrs) | Price (₹) |
|---------|---------|----------|----------------|-----------|
| 261377  | Vistara | Business | 13.50          | 123,071   |
| 216096  | Vistara | Business | 10.92          | 117,307   |
| 215859  | Vistara | Business | 21.08          | 116,562   |
| 277345  | Vistara | Business | 16.42          | 115,211   |
| 270999  | Vistara | Business | 9.50           | 114,705   |

---

## 🏷 Cheapest Flights  

| Index   | Airline  | Class   | Duration (hrs) | Price (₹) |
|---------|----------|---------|----------------|-----------|
| 203807  | AirAsia  | Economy | 1.17           | 1,105     |
| 203808  | GO_FIRST | Economy | 1.25           | 1,105     |
| 203908  | AirAsia  | Economy | 1.17           | 1,105     |
| 203909  | GO_FIRST | Economy | 1.25           | 1,105     |
| 204003  | AirAsia  | Economy | 1.17           | 1,105     |

---

### 4️⃣ Route Popularity  
- Created a `route` column (`source_city → destination_city`)  
- Found **Top 5 busiest routes** by frequency and visualized with a horizontal bar chart
 
## 📊 Exploratory Data Analysis (EDA)

---

### 5️⃣ Categorical Distributions  
- Plotted histograms for:  
  - **Airline popularity**  
  - **Source cities**  
  - **Departure times**  
  - **Number of stops**  
  - **Arrival times**  
  - **Destination cities**  
  - **Ticket class**  
![Categorical Distributions ](/Files/Flights.jpg)
---

###  Price vs Stops  
- Boxplot analysis showing how ticket prices vary with **number of stops**  
- Found that **non-stop flights** tend to be significantly more expensive than those with stops  
![ Price vs Stops ](/Files/stop.jpg)
---

###  Price Trend by Days Left  
- Line chart of `days_left` vs `price`  
- Inverted x-axis to show **approaching departure date** on the right  

📌 **Insight:** Prices tend to **increase as the departure date gets closer** (classic airline pricing strategy).  

---


### ✈  Top 5 Busiest Routes
![Top 5 Busiest Routes](/Files/Route.jpg)

- The most frequent route is dominated by **major city hubs**
- Popular routes often have **higher competition** among airlines
- Business-heavy routes show **more daily flights**

---

### 📆 Price Trend vs Days Before Departure
![Price Trend vs Days Left](/Files/Trends.jpg)

- Prices **increase sharply** in the last few days before departure
- Early booking often gives **lower prices**
- Trend reflects classic **airline dynamic pricing strategy**

**Insight:** Passengers benefit from booking flights **well in advance**, especially on busy routes.
---

### 💺 Distribution of Flight Classes

- **Business class** flights are fewer but command **significantly higher fares**  
- **Economy class** dominates the dataset, reflecting affordability for the mass market
![Distribution of Classes](/Files/Price.jpg)
---


## 📌 Key Insights Summary  

- **Ticket class** and **duration** are the strongest price influencers  
- **Non-stop flights** are significantly more expensive than flights with stops  
- Popular routes have competitive pricing due to higher demand  
- Last-minute bookings are generally **more expensive**  
- Some airlines consistently price higher regardless of route  

---

#
