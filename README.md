# Pharma Commercial Performance Dashboard (Power BI)

A two-page Power BI dashboard that tracks sales performance for a simulated
pharmaceutical commercial operations team in the UAE.

**[View the dashboard (PDF)](Pharma_Sales_Dashboard.pdf)**

## Business questions
- How are we performing against target, and how does that compare with last year?
- Which territories and therapeutic areas are ahead or behind?
- Which reps drive revenue, and where is performance slipping?

## Dashboard pages
1. **Performance overview** - KPI cards, monthly revenue vs target vs prior year,
   revenue by therapeutic area, attainment by territory, key insights.
2. **Rep performance** - rep leaderboard, revenue with a rolling 3-month average,
   revenue by brand, with territory and therapeutic area slicers.

## Data model (star schema)
- Fact tables: `Fact_Sales`, `Fact_Targets`
- Dimensions: `Dim_Date`, `Dim_Product`, `Dim_Territory`, `Dim_Rep`
- All relationships are one-to-many, single direction, from dimension to fact.
- Targets are set monthly per territory and product, so attainment is shown at
  territory, region and product level, not at rep level.

## Key DAX measures
Total Revenue, Total Units, Target Revenue, Attainment %, Variance to Target,
Revenue PY (YTD-aware), YoY Growth %, Rolling 3M Avg, Attainment Status,
Attainment Color.

## Key insights (2026 YTD, simulated data)
1. Sharjah City respiratory revenue is at 80.5% of target; the decline begins
   in July 2025. Action: review rep coverage and stock availability.
2. Ajman (88.6%) and Al Ain (91.8%) are the weakest territories overall.
   Action: pipeline and call-frequency review.
3. Fujairah is at 112.5% of target since January 2025. Action: identify what
   changed and test it in other Northern Emirates territories.


## Tools
Power BI Desktop, DAX, Power Query
