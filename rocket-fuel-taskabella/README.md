# Rocket Fuel: TaskaBella Field Experiment

## Case
Rocket Fuel, an AI-driven digital advertising company, ran a pilot display campaign for TaskaBella, a luxury handbag brand, from November 2015 to February 2016. Roughly 590,000 consumers were targeted with 14.5 million impressions, with 4% held out as a control group shown public service ads instead of product ads. The case asks whether the campaign actually caused incremental sales, and how it should be optimized going forward.

## Objective
Determine whether digital display advertising produced sales beyond what would have happened organically, evaluate the campaign's profitability, and identify the impression frequency and timing that maximize conversions.

## Approach
Used the randomized control group design (difference-in-differences) to isolate advertising's causal effect on conversion, then tested statistical significance with t-tests and chi-square/Fisher's exact tests, and broke conversion rates down by impression frequency, day of week, and hour of day.

## Key Findings
- The treatment group converted at 30% versus 0% for the control group, a 30 point lift attributable to advertising, significant under the Satterthwaite t-test (p = 0.0102).
- The campaign generated $238.97 in net profit against $1.03 in media cost, roughly a 23,292% ROI.
- Conversion is effectively a frequency threshold effect: 1-5 impressions produced 0% conversion, 6-8 impressions produced 66.7% conversion, and 9+ impressions produced 100% conversion.
- Saturday and the 8-10pm window produced the only conversions in the dataset, pointing to weekend evening browsing as the highest-intent moment for this audience.

## Recommendation
Scale the campaign given the demonstrated ROI, but restructure delivery to guarantee each targeted user reaches at least 6-8 impressions rather than spreading impressions thinly across a wider audience. Concentrate bids on Saturday evenings (8-10pm) and reduce spend during weekday daytime hours. Keep the control group in future campaigns, since the opportunity cost is small relative to the value of being able to prove causality to stakeholders, and use the experimental data to build out audience segmentation for future targeting.

## Contributors
Abdul-Rahim Baba Abdul-Mumin, Joon Kim, Likhitha Srinivas, Vivian Umelo
