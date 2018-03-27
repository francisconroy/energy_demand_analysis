# Energy Demand Analysis
This tool can be used to process data in the format like that found at [Australian Govt Consumption data set](https://data.gov.au/dataset/electricity-consumption-benchmarks).

The intention for this data is to be able to estimate the cost of electricity on a TOU (time of use) metering scheme by determining an average demand in each of the seasons

## The dataset
The primary dataset used in the analysis is structured as follows:
### Overview
All data sets are for 25 victorian households
### Table A - questionnaire responses
* The questionnaire responses will be used to filter the respondents to establish a trend for a certain household type

### Table B - consumption data
* Consumption data is for 25 Australian households
* Units are Watt Hours WH
* Date range is from 1.04.2012 - 31.03.2014
* Field E_0000_WH refers to WH usage in the half hour commencing at 0000
* The type column shows the type of usage being:
  * general
  * controlled load (separately metered)
  * generation (grid feed-in)

## Planned outcomes
This analysis should produce some data which can be used to estimate daily electricity consumption for different household situations.

## Analysis strategy
1. Import data rows from questionnaire and consumption data
2. Add calculated column to each row which is total WH consumption for that day entry
3. Filter the consumption data set to exclude respondents which do NOT match the selected criteria
