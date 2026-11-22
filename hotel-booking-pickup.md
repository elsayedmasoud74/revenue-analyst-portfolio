# Hotel Booking Pace and Pickup

This portfolio case study uses 84 synthetic hotel-date records covering two fictional properties for stays from 1 November through 12 December 2026. Monetary values are in USD.

## Excel analysis

Open [Analysis.xlsx](hotel-booking-pickup-analysis.xlsx). The Summary tab calculates portfolio KPIs from the underlying Data tab. Each record represents one property and one stay date. Ratios use aggregated numerators and denominators.

## Power BI Desktop

1. Import [hotel-data.csv](hotel-booking-pickup-data.csv) with Get Data → Text/CSV. Rename the query to Fact.
2. In Power Query, set StayDate to Date, Hotel to Text and the remaining columns to Whole Number. Apply changes.
3. Add the measures in [measures.dax](hotel-booking-pickup-measures.dax) individually using New measure. Format occupancy as a percentage, monetary measures as USD and room counts as whole numbers.
4. Add Hotel and StayDate slicers and a card for each measure. Add a line chart with StayDate on the axis and Net pickup as the value. Add a matrix by Hotel and StayDate with net pickup, gap to target and remaining rooms. Investigate negative pickup and prioritize dates with room to sell. Prior and current on-the-books room counts are seven days apart (16 and 23 October 2026). Negative net pickup can represent cancellations or booking changes.
5. With all filters cleared, verify that the first card (Net pickup) equals 294 and compare the other cards to the Excel Summary.
