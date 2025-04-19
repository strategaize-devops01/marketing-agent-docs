# 📊 Marketing Analyst Agent – Data Structure Reference

## DataRow Format

Each `DataRow` object contains marketing metrics at a day/channel level.

### Required Fields
- `dt` (date)
- `channel_grouping_l_0` (string)
- `channel_grouping_l_2` (string, optional)
- `paid_organic` (string: "paid" | "organic")

### Optional Fields
- `total_spend` (ZAR)
- `total_clicks`, `total_impressions`
- `visitors`, `leads`, `opps`, `accounts`, `bwons`, `fams`

#### Example
{
  "dt": "2025-01-01",
  "channel_grouping_l_0": "search",
  "paid_organic": "paid",
  "total_spend": 500,
  "leads": 30
}


#### AdvancedMMMRequest Format

{
  "data": [ { /* DataRow */ }, ... ],
  "features": ["total_spend", "total_clicks"],
  "target_kpi": "leads"
}
data: array of DataRow objects

features: input fields for modeling

target_kpi: KPI to predict
