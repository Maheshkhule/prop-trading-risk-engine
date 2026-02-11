# prop-trading-risk-engine
Institutional Prop Trading Analytics &amp; Risk Management Suite.

1. Project Overview - 
            This repository contains an end-to-end Power BI business intelligence solution designed for Proprietary Trading Firms. The engine analyzes the performance and risk metrics of 100+ professional traders             across 25,000+ trade executions.

2. Core Features - 
             * Performance Tracking: Automated calculation of Profit Factor, Win Rate, and Total Net PnL.
             * Risk Oversight: Real-time monitoring of Daily Stop-Loss breaches and Maximum Drawdowns (MDD).
             * Edge Analysis: Categorization of performance by Market Session (Pre/Post Market) and Ticker Symbol.
             *Capital Allocation: Dynamic tracking of firm-wide buying power vs. realized exposure.

3. Technical Stack - 
             * Tool: Microsoft Power BI Desktop
             *Language: DAX (Data Analysis Expressions) for complex measures.
             *Data Modeling: Star Schema (1:N relationship between Master and Fact tables).
             *Data Prep: Power Query for time-intelligence and data cleaning.

4. Key DAX Formulas Used
            Code snippet
            // Example: Win % Calculation
           Win % = 
                DIVIDE(
                    CALCULATE(
                        COUNTROWS('trade_history'),
                        'trade_history'[Win Indicator] = 1
                    ),
                    COUNTROWS('trade_history'),
                    0
                )
