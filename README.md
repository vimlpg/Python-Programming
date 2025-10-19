# Python-Programming
Design and build a robust Python data processing workflow to demonstrate a sound understanding of the programming concepts covered in the lectures of CMSE11433 Python Programming.

This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.
While the dataset provides detailed operational information, it lacks derived business metrics that could support hotel decision-making. The analytical gap we identified is the absence of engineered indicators that describe customer behaviour and booking value patterns.
To address this, we will design a Python workflow that cleans the raw data, handles missing values, corrects data types, and creates a set of new, rule-based features. These include:

1)len_of_stay: weekday + weekend nights (outlier-capped).
2) revenue_booking:ADR × len_of_stay (set to 0 if cancelled).
3) late_booking_flag: 1 if lead_time < 7 days, else 0.
4) cxl_risk_score (rule-based): weighted sum of long lead_time, off-season month, single-adult bookings, and historical cancel propensity by market.
5) value_segment (Low/Medium/High): revenue_booking quantiles
6) loyalty check if the guest is repeated or has previous cancellation 
7) Customer Segmentation, family, couple or solo
8) Season: arrival_date_month (High/Low/Average)

The enriched dataset will offer a clearer view of booking characteristics, enabling improved insights on revenue, seasonality, segmentation and potential cancellation behaviour.
