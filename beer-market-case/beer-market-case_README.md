# Beer Market: Brand Portfolio & Marketing Mix Strategy

## Case
A grocery supermarket brand manager oversees five beer brands (Coors Light, Budweiser, Corona, Michelob Ultra, Heineken) in a market facing declining overall consumption, premiumization, and rising health-conscious demand. The case provides 1,000 days of brand-level sales, price, advertising spend, and in-flyer feature data, and asks how the brand manager should approach marketing mix decisions across the portfolio.

## Objective
Describe an approach to managing marketing mix activities given the state of the beer market, build and interpret a data-driven marketing mix strategy (own-price and cross-price elasticity, and feature/promotion effects), and identify how the models could be improved.

## Approach
Estimated three sets of regressions per brand in SAS (PROC REG) using the 1,000-day panel:
- **Own-price elasticity models** (log-log): logSales = f(logPrice, logAdvertising, Feature)
- **Cross-price elasticity models** (log-log): logSales = f(own logPrice, all four competitor logPrices, own logAdvertising)
- **Feature impact models** (linear): Sales = f(Feature dummy)

## Key Findings
- All five brands show inelastic demand. Budweiser is the most price-sensitive (-0.091), Heineken the least (-0.022); Michelob Ultra is also surprisingly price-inelastic (-0.036) despite its premium positioning.
- Advertising elasticities are positive and significant for every brand. Coors Light shows the strongest advertising response (0.195), Heineken the weakest (0.056).
- No brand shows a statistically significant cross-price effect from any competitor, across all 20 competitor-price coefficients tested. This points to strong brand differentiation and loyalty rather than direct price-based switching between brands.
- Feature/promotion effects are mostly insignificant, with one exception: Heineken shows a statistically significant *negative* feature effect (-0.73, p = 0.0381) in the linear model, and its log-log model's feature coefficient is also significant (p = 0.0336), suggesting that featuring this brand in promotions may hurt sales by undercutting its premium image. Note this runs counter to the write-up's summary sentence describing log-linear feature effects as insignificant across all five brands; the SAS table above is the source of truth.

## Recommendation
- **Pricing:** Hold prices stable for Michelob Ultra and Heineken, which can sustain premium pricing given their low elasticity. Budweiser has the most room for tactical price cuts to drive volume; Coors Light and Corona allow limited, targeted adjustments.
- **Advertising:** Prioritize spend on Coors Light (highest ROI) and Michelob Ultra (second-highest, and aligned with the health/moderation trend). Maintain steady spend on Budweiser and Corona; keep Heineken's advertising narrow and premium-targeted rather than broad.
- **Features/promotions:** Drop feature promotions for Heineken given its negative, significant effect. For the other four brands, feature effects aren't reliably positive, so use promotions selectively and pair them with other tactics rather than relying on features alone.
- **Competitive response:** Since no significant cross-price effects were found, each brand can set its strategy independently of competitor pricing moves, and should focus on protecting its own brand equity rather than reacting to rivals.

## Model Improvements (Q3)
Three extensions were proposed to address limitations in the base models:
- **Interaction effects** between price, advertising, and feature variables, since the current models assume these operate independently.
- **Advertising carryover (adstock)**, to capture the fact that advertising's effect builds across periods rather than resetting each day; requires estimating a decay parameter via PROC MODEL or by testing fixed decay values.
- **Time effects**, to account for evolving market conditions and brand-specific fixed effects over the 1,000-day window, including a lagged sales term and linear/quadratic time trends.

## Contributors
Abdul-Rahim Baba Abdul-Mumin, Joon Kim, Likhitha Srinivas, Vivian Umelo
