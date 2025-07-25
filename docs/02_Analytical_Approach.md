# 2. The Analytical Approach

This document explains the methodology behind the Discount Strategy Simulator. The entire tool is built on a "Baseline vs. Scenario" framework, allowing for a direct comparison between a default forecast and a user-defined hypothetical situation.

## The "Actual" - A Baseline Forecast

A crucial aspect of this model is that the "Actual" figures do not represent real-time performance. Instead, they represent a **Baseline Forecast** for the selected period (e.g., 2017). This forecast is generated by taking the actual, historical performance from the prior year (2016) and projecting it forward.

*   **Why use a forecast?** This approach creates a stable, unchanging benchmark. It allows a user to ask, "Compared to our default business-as-usual forecast, what is the *additional* impact of this specific promotional strategy?" This isolates the effect of the promotion itself.

## The "Scenario" - A User-Defined Simulation

The "SCENARIOS" and "FILTERS" panels on the right are the control center for the simulation. A user builds a scenario by defining three key components:

1.  **Product Selection:** The user chooses one or multiple products from the dropdown menu. These are the only products that will have the discount applied in the scenario calculation.
2.  **Discounting Change:** The user adjusts a slider to set the discount percentage (e.g., -8%). This directly impacts the selling price of the selected products in the scenario.
3.  **Demand Change:** The user adjusts a second slider to model the expected "demand elasticity" (e.g., +16%). This simulates the anticipated increase in sales quantity that will result from the price reduction. This is a critical assumption that the user can test.

## The Output - Measuring the Impact

Once the user defines a scenario, the dashboard's DAX engine recalculates all "Scenario" metrics in real-time. The visuals are designed to answer specific business questions:

*   **KPI Cards (`Actual vs Scenario Sales`, `Profit Margin`):** These answer the primary question: "What is the final, bottom-line impact of our proposed scenario?" They provide the total projected profit and the resulting profit margin, directly compared to the baseline forecast.
*   **Cumulative Charts (`Actual vs Scenario Profits`):** This answers, "How does the value of this promotion accumulate over time?" It provides a much richer story than a single number, showing if the strategy generates consistent gains or is volatile.
*   **Difference Charts (`Potential Daily Profit Change`):** This answers, "What is the day-to-day risk and volatility of this strategy?" It shows the daily profit variance, highlighting the consistency of the scenario's impact.

This framework transforms the dashboard from a simple report into a dynamic modeling tool for strategic decision-making.

