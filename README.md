# Cost of Failed Transactions Analysis

## Project Overview

Transaction failures are more than unsuccessful payment attempts. When they occur at scale, they can affect business revenue, customer experience and operational efficiency.

This project investigates the patterns and financial implications of failed transactions using PostgreSQL for data preparation and analysis and Microsoft Power BI for interactive visualisation.

The objective was to understand the distribution of failed transactions across payment methods, countries, business sectors and customer categories, while identifying areas that deserve further investigation and potential business intervention.

## Business Questions

The analysis was guided by the following questions:

1. What proportion of transactions fail, and what is the overall scale of the problem?
2. Which payment methods and business sectors record the highest failure rates?
3. How are failed transactions distributed across the countries represented in the dataset?
4. What does the transaction performance trend reveal over time?
5. What is the financial significance of failed transactions?
6. Which areas should management prioritise for further investigation and improvement?

## Tools and Technologies

- **PostgreSQL:** Database creation, data cleaning, validation, querying and exploratory analysis.
- **Microsoft Power BI:** Data modelling, KPI development, interactive dashboards and business reporting.
- **SQL:** Aggregations, conditional calculations, date-based analysis and data-quality checks.

## Data Preparation

The project involved three staging datasets:

- `stg_transactions`
- `stg_customers`
- `stg_exchange_rates`

The imported datasets contained:

| Dataset | Records |
|---|---:|
| Transactions | 62,684 |
| Customers | 64,343 |
| Exchange rates | 46,490 |

Data-quality checks included the investigation of missing and zero exchange-rate values and other inconsistencies that could affect the reliability of the analysis.

Missing rates and zero rates were treated as separate data-quality conditions.

## Key Findings

### 1. Overall Transaction Performance

- Overall transaction failure rate: approximately 63%.
- Total transaction count displayed: approximately 63K.
- Failed transaction count displayed: approximately 40K.
- Total customers displayed: approximately 64K.
- Inactive customers displayed: approximately 62K.

### 2. Payment Method Performance

The highest recorded failure rates were:

| Payment method | Failure rate |
|---|---:|
| Pay With Wallet | 99% |
| E-naira | 97% |
| Account | 87% |
| Alternative Channels | 84% |
| Card | 77% |

Bank Transfer recorded the lowest displayed failure rate at 23%.

### 3. Geographical Performance

The country visual showed Uganda with the highest displayed transaction and failed-transaction volumes, followed by Kenya.

The SQL investigation also identified Kenya as contributing approximately 93% of the failed-fee value examined.

### 4. Sector Performance

Agric Produce recorded the highest displayed sector failure rate at 73.15%, followed by Banks and Ofis at 66.42% and Crypto at 66.16%.

PSPs recorded the lowest displayed failure rate at 33.33%.

### 5. January 2024 Investigation

The earlier SQL analysis identified January 2024 as an exceptional period, with an approximately 97% failure rate and more than $745,000 in failed-fee value.

Further investigation is required to establish the underlying causes and whether the spike was temporary or part of a continuing trend.

## Financial Impact

The SQL investigation reported approximately $2.85 million in fees associated with failed transactions, against approximately $3.15 million in total fees.

The analysis highlights the importance of distinguishing total failed-associated financial value from the portion that could realistically be recovered.

A recovery opportunity should be estimated using the addressable financial value associated with an identifiable problem and a defensible improvement assumption.

## Business Recommendations

Based on the observed patterns, the following areas deserve further investigation:

1. Investigate payment channels with exceptionally high failure rates, particularly Pay With Wallet and E-naira.
2. Examine geographical financial exposure, with attention to Kenya and Uganda.
3. Investigate sectors with comparatively high failure rates, particularly Agric Produce, Banks and Ofis, and Crypto.
4. Strengthen transaction monitoring to identify unusual changes in failure rates.
5. Investigate inactive customer patterns and their relationship with transaction performance.
6. Develop a measurable recovery strategy focused on the largest identifiable and addressable source of failure.

## Power BI Dashboard

The project includes two interactive reporting pages:

**Page 1: Cost of Failed Transactions – Executive Report**

Provides an overview of transaction performance, failure rate, transaction counts, financial measures, monthly trends, geographical distribution and payment-method performance.

**Page 2: Sector and Customer Analysis**

Explores customer activity, sector-level failure rates, customer distribution and revenue performance by transaction status.

The dashboards include filters for country, payment type, sector, transaction status and customer status.

## Limitations and Further Investigation

The available analysis identifies where transaction failures are concentrated but does not independently establish their technical or behavioural causes.

Gateway outages, routing issues, provider errors, insufficient funds, incorrect payment details and abandoned transactions require supporting evidence from failure-reason and provider-level data.

The January 2024 spike also requires further investigation to establish its cause and duration.

The financial recovery opportunity has not been presented as a guaranteed amount because the addressable value and realistic improvement rate require additional validation.

## Project Outcome

This project demonstrates the application of SQL and business intelligence tools to a financial transaction problem.

It strengthened my practical experience in database preparation, data-quality assessment, analytical querying, KPI development, dashboard design and translating data findings into business recommendations.

**The central takeaway:** identifying failed transactions is only the beginning. Understanding their distribution, financial implications and potential causes is what makes the analysis valuable to business decision-making.

---

**Author:** Abiodun Ibirogba  
**Tools:** PostgreSQL | SQL | Microsoft Power BI
