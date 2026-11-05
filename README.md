# LEGO Market Intelligence

**Research project · Early-stage proof of concept · Not a live investment service**

LEGO Market Intelligence explores whether publicly observable demand signals can help identify collectible LEGO sets with an increased probability of appreciating after retirement (end of life, or **EOL**).

The long-term goal is an **early-warning and opportunity-monitoring system**: a research-driven tool that combines market prices, retirement risk, availability, and demand indicators to flag products worth investigating. The initial scope is LEGO sets; the methodology may later be tested on other collectible markets.

> **Current status:** Exploratory research and methodology design. Historical hypotheses and data-access methods are being tested. No predictive accuracy, investment returns, production API integration, or automated alerts are claimed at this stage.

## Research questions

1. Do changes in search interest, community discussion, or broader pop-culture attention precede secondary-market price changes?
2. Which signals add predictive value beyond basic information such as theme, release year, retail price, current market price, and EOL status?
3. How do exclusive or unusually designed minifigures, gifts with purchase (GWPs), and magazine-distributed figures influence the economics of a complete set?
4. How can the system distinguish a genuine purchasing opportunity from inflated asking prices, short-term hype, and thinly traded items?
5. How do regional differences in prices, promotions, stock availability, and search behavior affect conclusions?

## Candidate data sources

| Area | Example signals | Research purpose |
| --- | --- | --- |
| Secondary market | Historical completed-sale prices where available, active offers, transaction volume, spreads | Measure price movement and market liquidity |
| Product lifecycle | Launch date, retirement announcements or estimates, retailer availability | Model EOL timing and supply changes |
| Search interest | Google Trends time series for product IDs, names, themes, and licensed franchises | Test leading indicators of demand |
| LEGO communities | Public discussions, reviews, wish lists, and collector sentiment | Detect changes in product-level interest |
| Pop culture | Series releases, film announcements, character visibility, anniversaries | Test demand shocks for licensed products |
| Product composition | Exclusive minifigures, distinctive molds, parts, GWPs and magazine gifts | Test scarcity and substitution hypotheses |
| Local market | Polish and international prices, discounts, shipping and selling costs | Estimate realistic net opportunities |

Google Trends is an **optional input**, not a prerequisite for an alert. Rare product-level searches may have insufficient data or inconsistent coverage. We are exploring access to the official Google Trends API to evaluate consistent historical and regional comparisons; access and integration are **not yet established**.

## Proposed evaluation approach

- **Diverse samples:** Compare licensed and non-licensed themes, different price segments, and retired as well as currently sold sets. Avoid drawing conclusions from a single popular franchise or one exceptional set.
- **Time-aware backtesting:** Use only information that would have been available at each historical decision date. Reserve later periods for out-of-sample evaluation.
- **Baselines first:** Compare models using price, age, EOL and availability data against models that additionally include search, community, and cultural signals.
- **Realistic economics:** Evaluate realized or transaction-based prices where available, not just seller asking prices. Account for fees, shipping, storage, taxes when relevant, and the time needed to sell.
- **Uncertainty and data quality:** Track sparse observations, estimated EOL dates, region, product condition, sealed/open status, and minifigure or packaging variants. Do not treat rarity anecdotes as universal rules.
- **Actionable metrics:** Assess ranking quality, false-positive alerts, risk-adjusted outcomes, liquidity, and the sensitivity of results to transaction costs.

## Illustrative case studies

These sets are research examples, **not recommendations or validated forecasts**:

- **75374 — The Onyx Cinder:** Test how interest in a new *Star Wars* storyline and distinctive characters might affect later demand.
- **75357 — Ghost & Phantom II** and **75053 — The Ghost:** Examine franchise continuity, set re-releases, retired-product prices, and exclusive-minifigure effects without assuming their historical outcomes will repeat.
- Selected licensed and non-licensed products: Provide controls for broader LEGO demand and franchise-specific effects.

## Planned milestones

- [x] Define research questions and candidate demand, supply, and price signals.
- [ ] Document a reproducible product sample, regional scope, and data dictionary.
- [ ] Establish reliable, permission-compliant historical data collection.
- [ ] Implement baseline EOL/price models and rolling out-of-sample backtests.
- [ ] Quantify the incremental value of Google Trends and other public demand signals.
- [ ] Prototype interpretable alerts with confidence levels, expected net margins, and source provenance.
- [ ] Validate stability across themes, markets, and different historical periods.

## Data access and responsible use

This repository is intended to document methodology and, in future, publish reusable code where rights permit. Third-party data belongs to its respective owners. Collection and reuse will be subject to applicable terms of service, licensing, access controls, and privacy requirements. No API secrets, personal data, or proprietary third-party datasets will be published here.

## Disclaimer

This is an independent research project and is **not affiliated with, sponsored by, or endorsed by the LEGO Group, Google, Disney, Lucasfilm, or any marketplace**. LEGO and other names are trademarks of their respective owners. This project is not financial advice; collectible markets are illiquid and price appreciation is not guaranteed.