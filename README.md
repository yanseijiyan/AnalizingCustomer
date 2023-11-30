## Context:
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

 ## Data Description:

  1.InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.

  2.StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.

  3.Description: Product (item) name. Nominal.

  4.Quantity: The quantities of each product (item) per transaction. Numeric. InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.

  5.UnitPrice: Unit price. Numeric, Product price per unit in sterling.

  6.CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

  7.Country: Country name. Nominal, the name of the country where each customer resides.

## Problem statement
It is a business critical requirement to understand the value derived from a customer. RFM is a method used for analyzing customer value.


## Approach:

1. Perform a preliminary data inspection and Data cleaning

  ・ Check for missing data and formulate apt strategy to treat them.

  ・ Are there any duplicate data records? Remove them if present.

  ・ Perform Descriptive analytics on the given data.

2. Cohort Analysis: A cohort is a group of subjects who share a defining characteristic. We can observe how a cohort behaves across time and compare it to other cohorts.

  ・ Create month cohorts and analyse active customers for each cohort.

  ・ Also Analyse the retention rate of customers. Comment.

3. Build a RFM model – Recency Frequency and Monetary based on their behaviour.
   
  ・ Calculate RFM metrics.

    **i.** Recency as the time in no. of days since last transaction

    **ii.** Frequency as count of purchases done

    **iii**. Monetary value as total amount spend

  ・ Build RFM Segments.

    **i.** Give Recency Frequency and Monetary scores individually by dividing them in to quartiles.

    **ii.** Combine three ratings to get a RFM segment (as strings)

    **iii.** Get the RFM score by adding up the three ratings.

  ・ Analyse the RFM Segments by summarizing them and comment on the findings.

4. Create clusters using k means clustering algorithm.

  ・ Prepare the data for the algorithm.

   ** i.** If the data is Un Symmetrically distributed, manage the skewness with appropriate transformation.

    **ii.** Standardize / scale the data.

  ・ Decide the optimum number of clusters to be formed

  ・ Analyse these clusters and comment on the results.

5. Create a dashboard in tableau by choosing appropriate chart types and metrics useful for the business. The dashboard must entail the following:

  ・ Country-wise analysis to demonstrate Average spend. Use a bar chart show monthly figures.

  ・ Bar graph of top 15 products which are mostly ordered by the users to show the number of products sold.

  ・ Bar graph to show the count of orders Vs. hours throughout the day. What are the peak hours per your chart?

  ・ Plot the distribution of RFM values using histogram and frequency-charts.

  ・ Plot error(cost) vs no of clusters selected

  ・ Visualize to compare the RFM values of the clusters using heatma
