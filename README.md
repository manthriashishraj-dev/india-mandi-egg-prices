# India mandi, egg and cardamom prices (CSV)

Free price history for India from official sources, cleaned and summarised by
[Today Market Rates](https://todaymarketrates.com/) (todaymarketrates.com), a website that publishes the day's egg,
mandi crop, vegetable and cardamom prices in English and Telugu.

- **Mandi crop prices:** Agmarknet (Directorate of Marketing & Inspection, Government of India, via data.gov.in). The
  India median price per quintal of 173 crops, by month (2002-02 to 2026-11) and by week.
- **Egg rates:** NECC (National Egg Co-ordination Committee). The India average and 34 markets, rupees per
  egg, by month (2009-01 to 2026-11).
- **Small cardamom:** Spices Board of India e-auctions. Average price per kg, quantity sold and the best lot, by month.

Last updated **12 Nov 2026**. The same files are on [todaymarketrates.com/data](https://todaymarketrates.com/data/), and this
repository is refreshed from there every week.

## Files

| File | What it holds | Rows | Period |
|---|---|---:|---|
| [`cardamom-small-monthly.csv`](data/cardamom-small-monthly.csv) | Small cardamom auctions: average price, quantity sold, best lot, by month | 14 | 2025-10 to 2026-11 |
| [`egg-india-monthly.csv`](data/egg-india-monthly.csv) | NECC egg rate, India average per egg, by month | 215 | 2009-01 to 2026-11 |
| [`egg-markets-monthly.csv`](data/egg-markets-monthly.csv) | NECC egg rate for each of 34 markets, by month | 6,646 | 2009-01 to 2026-11 |
| [`mandi-india-monthly.csv`](data/mandi-india-monthly.csv) | Mandi prices of 173 crops, India median per quintal, by month | 19,634 | 2002-02 to 2026-11 |
| [`mandi-india-weekly.csv`](data/mandi-india-weekly.csv) | Mandi prices by week (the figures in our weekly reports) | 1,958 | 2026-08-23 to 2026-11-08 |

Lines starting with `#` at the top of each file are notes (source and conditions); the data starts after them. In
Python: `pandas.read_csv("data/mandi-india-monthly.csv", comment="#")`. Prices are in Indian rupees (INR); mandi prices
are per quintal (100 kg), so divide by 100 for the price per kg.

## Using the data

You are welcome to use these figures in articles, reports, research and apps. Please name the original source and link
to the page you used, for example:

- `Source: Today Market Rates (todaymarketrates.com), from Agmarknet mandi prices (data.gov.in)`
- `Source: Today Market Rates (todaymarketrates.com), from NECC egg prices`

Each source sets its own terms:

- **Mandi prices** are published on data.gov.in under the
  [Government Open Data Licence - India](https://www.data.gov.in/Godl).
- **Cardamom auction results** are published by the Spices Board of India (indianspices.com).
- **NECC** asks that anyone sharing its suggested egg prices also shares its clarification:

> “The daily egg prices suggested by NECC, on its official website or through any other medium (including verbal, print and digital media) are merely suggestive and not mandatory. The suggested prices are published solely for the reference and information of the trade and industry. NECC does not by itself or through any person enforce compliance or adherence with such suggested egg prices in any manner whatsoever. If any person not authorized by NECC chooses to disseminate NECC suggested prices through any medium, such person must also include the above clarification while disseminating NECC suggested prices of eggs.”

These figures are given as published by the sources, without warranty, and nothing here is endorsed by the Government
of India, NECC or the Spices Board.

## Need more than these summaries?

Behind these files we keep the daily Agmarknet prices of about 4,500 markets and more than 400 commodities (minimum,
maximum and modal price, by variety and grade). If your business, research or app needs the full data, a regular file
or an API, [tell us what you need](https://todaymarketrates.com/data/#more-data).

Today's prices, charts and city pages: [todaymarketrates.com](https://todaymarketrates.com/) ·
[egg rate today](https://todaymarketrates.com/egg-rate/) · [mandi prices](https://todaymarketrates.com/mandi/)
