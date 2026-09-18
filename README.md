# Beyond the repair event

**B106 Data Visualisation - Individual Project**

## Project question

Which product categories should a community repair network prioritise for follow-up support after a repair event?

I use the Open Repair Alliance July 2025 aggregate snapshot and focus on records from 2024. The analysis is intended for the coordinator of a fictional repair network planning a small follow-up programme. Of the 85,515 recorded attempts in 2024, 14,702 were classified as Repairable. This means that the repair was unfinished but a further step had been identified. These records represent potential follow-up cases, not confirmed future successful repairs.

## Methods and findings

I compare seven aspects of the recorded cases: outcome composition, category counts and shares, provider differences, monthly patterns, the distribution across local groups, repeated brands and product ages. The figures use counts alongside percentages and show distributions where a single average would hide useful differences.

Vacuums have the largest Repairable count, with 1,441 records, and remain first when either of the two largest providers is excluded. Most vacuum-reporting groups recorded at most two Repairable cases, while about a tenth of groups accounted for 43.3% of the cases. I therefore recommend starting with a small vacuum follow-up pilot and considering shared resources or specialist referrals across groups.

The data come from voluntary reporting and contain differences between providers and substantial missing age information. They do not establish owners' willingness to participate, the resources required or later repair success. A pilot would need to record uptake, completed repairs, time and costs before the network decides whether to expand it.

## Main files

- [Jupyter notebook](B106_Data_Visualisation_Assignment.ipynb) contains the complete analysis, seven figures, conclusions and references.
- [Streamlit app](app.py) presents the same report with expandable code and a pilot portfolio comparison.
- [Source data](data/OpenRepairData_v0.3_aggregate_202507.csv) contains the repair records used by both versions.
- [Product categories](data/OpenRepairData_v0.3_Product_Categories.csv) contains the accompanying category lookup.
- [Python requirements](requirements.txt) lists the packages needed to run the notebook and app.

## Running the project

I used Python 3.12. Install the dependencies with `pip install -r requirements.txt`, then run the notebook from the project folder. The source CSV is included in `data/`.

To open the Streamlit version, run `python -m streamlit run app.py`. The sidebar links to each section and switches between wide and centred layouts. The pilot comparison lets you select product categories and a date range to compare their historical Repairable case counts and shares.

## Dataset

The source is the [Open Repair Alliance dataset](https://github.com/openrepair/data), using the July 2025 aggregate snapshot with records from June 2012 to July 2025. The data are available under CC BY-SA 4.0. Field and outcome definitions are described in the [Open Repair Data Standard, version 0.3](https://standard.openrepair.org/standard.html). Full references are included in the notebook.
