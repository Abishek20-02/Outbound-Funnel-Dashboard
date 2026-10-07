# Outbound Funnel Dashboard

An interactive dashboard that shows where a B2B outbound calling funnel stalls, and whether a process fix moved the numbers.

**Live demo:** (https://nimble-kashata-22580f.netlify.app)

> **About the data:** every number here is synthetic. I generated it to demonstrate the analysis method. It is not real company data, and nothing on this page should be read as an actual result.

## Why I built it

In a staffing sales role I found that most outbound calls never reached a decision-maker because automated gatekeeper systems intercepted them. The dashboard in leadership's hands showed a weak conversion rate, which looked like a performance problem. Breaking the funnel into stages showed the real problem was at the very first step. This project rebuilds that way of looking at a funnel on illustrative data, so the method is visible.

## What it shows

- **KPIs** for the selected period: dials, interception rate, qualification rate, handoffs and dial-to-handoff conversion.
- **Funnel by stage:** dials, reached a decision-maker, qualified, requirement captured, handed to delivery. The stage with the largest percentage loss is highlighted automatically.
- **Weekly interception trend** over 12 weeks, with the week the process fix shipped marked.
- **Before and after table** comparing the six weeks before the fix with the six weeks after.
- **Period toggle:** all 12 weeks, before the fix, or after the fix. The funnel, KPIs and trend update together.

## Metric definitions

| Metric | Definition |
|---|---|
| Interception rate | Dials that did not reach a decision-maker, divided by total dials |
| Qualification rate | Qualified leads divided by decision-makers reached |
| Dial to handoff | Handoffs to delivery divided by total dials |
| Biggest loss | The stage with the lowest conversion from the stage before it |

## What I would check next

- Whether the drop in interception holds across segments (company size, industry, region) or only in some.
- Whether leads reached after the fix are lower quality, which would show up in qualification rate and handoff rate.
- Whether the change came from the fix or from a change in the mix of accounts called.
- Whether twelve weeks is enough to rule out normal week-to-week variation.

## Limitations

- The data is synthetic, so the figures illustrate the method and do not prove anything.
- A before/after comparison does not establish that the fix caused the change. A proper test would need a control group.
- Stage definitions are simplified.

## Tech

A single HTML file with inline CSS and JavaScript. No dependencies, no build step, no network requests. Open `index.html` in any browser.

## Author

S. Abishek Karthikeyan | [LinkedIn](https://www.linkedin.com/in/s-abishek-karthikeyan-8020b622b) | [Other project: Post-Trade Review](https://github.com/Abishek20-02/Nubra-post-trade-review)
