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
  "type": "object",
  "properties": {
    "channels": {
      "type": "array",
      "items": { "type": "string" }
    },
    "spend": {
      "type": "array",
      "items": {
        "type": "array",
        "items": { "type": "number" }
      }
    },
    "sales": {
      "type": "array",
      "items": { "type": "number" }
    },
    "what_if_spend": {
      "type": "array",
      "items": { "type": "number" }
    }
  },
  "required": ["channels", "spend", "sales"]
}
