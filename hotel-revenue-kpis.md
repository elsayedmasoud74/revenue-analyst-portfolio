# Hotel Revenue Performance

This portfolio case study uses 84 synthetic hotel-date records covering two fictional properties for stays from 1 November through 12 December 2026. Monetary values are in USD.

## Excel analysis

Open [Analysis.xlsx](hotel-revenue-kpis-analysis.xlsx). The Summary tab calculates portfolio KPIs from the underlying Data tab. Each record represents one property and one stay date. Ratios use aggregated numerators and denominators.

## Power BI Desktop

1. Import [hotel-data.csv](hotel-revenue-kpis-data.csv) with Get Data → Text/CSV. Rename the query to Fact.
2. In Power Query, set StayDate to Date, Hotel to Text and the remaining columns to Whole Number. Apply changes.
3. Add the measures in [measures.dax](hotel-revenue-kpis-measures.dax) individually using New measure. Format occupancy as a percentage, monetary measures as USD and room counts as whole numbers.
4. Add Hotel and StayDate slicers and a card for each measure. Add a line chart with StayDate on the axis and RevPAR as the value. Add a matrix by Hotel with occupancy, ADR, RevPAR and budget variance. Review low-occupancy dates before changing rates.
5. With all filters cleared, verify that the first card (Room revenue) equals 685,269 and compare the other cards to the Excel Summary.
