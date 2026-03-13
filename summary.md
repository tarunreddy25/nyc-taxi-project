# NYC Taxi Analysis — January 2024

## Dataset
- Source: NYC Taxi & Limousine Commission
- Total trips: 2,964,624
- Cleaned trips: 2,723,805 (removed 240,819 bad rows)

## Key Findings
1. Peak hours are 3pm-7pm (evening rush hour)
2. Wednesday is the highest revenue day ($13.3M)
3. 60% of trips are under 2 miles, averaging $9.91
4. Average tip is exactly 20% — riders tap the default
5. Groups of 4 pay the most on average ($22.86)

## Data Quality Issues Found
- 140,162 rows had missing passenger_count
- Max trip distance was 312,722 miles (impossible — removed)
- 8-passenger trips likely data entry errors

## Files
- results/hourly_trips.csv
- results/daily_revenue.csv
- results/trip_categories.csv
