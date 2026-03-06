# Hotel Demand Forecasting & Revenue Management Insights

## Overview

This project analyzes hotel booking data to forecast **future demand (room nights)** and evaluate how different **distribution channels contribute to total hotel demand**.

The goal is to combine **time series forecasting** with **Revenue Management analysis** to understand how demand evolves and how the distribution mix of the hotel is changing.

The forecasting models were built using **Prophet**, focusing on both **total hotel demand** and key **market segments**.

---

## Dataset

Hotel Booking Demand Dataset  

Key variables used in the analysis:

- Arrival date
- Market segment
- Cancellation status
- Length of stay

Only **non-cancelled bookings** were used to measure **real demand**.

Room nights were calculated as:

```

room_nights = stays_in_weekend_nights + stays_in_week_nights

```

Demand was then aggregated **monthly**.

---

## Forecasting Models

Forecasts were created for:

- **Total Hotel Demand**
- **Direct segment**
- **Online Travel Agencies (OTA)**
- **Offline TA / Tour Operators**

The model used was **Prophet**, configured with yearly seasonality to capture demand cycles.

---

## Forecast Results (Total Hotel Demand)

| Month | Forecast Room Nights |
|------|----------------------|
| September | ~12,904 |
| October | ~12,416 |
| November | ~8,966 |

The forecast shows a **gradual decline after peak summer demand**, consistent with seasonal patterns observed in the historical data.

---

## Segment Insights

### Direct

- Stable demand pattern
- Lower forecasting error
- Most profitable channel

Direct bookings represent the **most predictable and profitable demand source**.

---

### Online Travel Agencies (OTA)

- Strong demand growth
- Largest contributor to total demand
- Higher volatility

OTAs act as the **main driver of booking volume**.

---

### Offline TA / Tour Operators

- Irregular demand
- Structural decline in contribution

This channel appears to be **losing relevance compared to digital channels**.

---

## Revenue Management Insights

The comparison between **segment forecasts and total demand** reveals a clear shift in the hotel’s distribution strategy.

Key insights:

- Demand growth is driven mainly by **OTA and Direct channels**
- **Tour operators are losing structural importance**
- **OTA drives volume**, while **Direct drives profitability**
- Increasing Direct share could reduce **distribution costs and commissions**

Overall, the hotel appears to be transitioning toward a **more digital distribution model**, relying less on traditional intermediaries.

---

## Tools

- Python
- Pandas
- Prophet
- Matplotlib

