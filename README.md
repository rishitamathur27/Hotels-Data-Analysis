# Hotels-Data-Analysis
Interactive dashboard using Power BI 

In this project, I've designed a realistic hotels infor dataset's interactive dashboard based on the few key matrix.

Some of the key matrices includes:

1. RevPar (Revenue Per Available Room) = Total Revenue / Total rooms available to sell
2. Occupancy % = DIVIDE([Total Succesful Bookings],[Total Capacity],0)
3. Average Rating = AVERAGE(fact_bookings[ratings_given])
4. No. of days = DATEDIFF(MIN(dim_date[date]),MAX(dim_date[date]),DAY) +1
5. Total cancelled bookings = CALCULATE([Total Bookings], fact_bookings[booking_status] = "Cancelled")
6. Cancellation % = DIVIDE([Total cancelled bookings],[Total Bookings])
7. Total no show bookings = CALCULATE([Total Bookings],fact_bookings[booking_status]="No Show")
8. Total Checked Out = CALCULATE([Total Bookings],fact_bookings[booking_status]="Checked Out")
9. No Show rate % = DIVIDE([Total no show bookings],[Total Bookings])
10. ADR (Average Daily rate) = DIVIDE([Revenue], [Total Bookings],0)
11. Realisation % = 1- ([Cancellation %]+[No Show rate %])
12. RevPAR (Revenue Per Available Room) = DIVIDE([Revenue],[Total Capacity])
13. DSRN (Daily Sellable Room Nights) = DIVIDE([Total Capacity], [No of days])
14. DSRN (Daily Sellable Room Nights) = DIVIDE([Total Capacity], [No of days])
15. DURN(Daily Utilized Room Nights) = DIVIDE([Total Checked Out],[No of days])
