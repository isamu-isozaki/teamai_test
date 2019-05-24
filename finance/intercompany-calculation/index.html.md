---
layout: markdown_page
title: "Intercompany Calculation"
---


## Intercompany Calculation

1. Open Intercompany Calculation Sheet from Google Drive.
1. Add a new tab for the current month calculation. 
1. Copy the contents of the previous month’s tab to the current month and change the date in cell B2.
1. Access NetSuite and open the income statement (found under the Reports and Financial tabs/index.html.md).
1. Filter the income statement to the current month then further refine it by the desired subsidiary and set the column display to Subsidiary.
    * Note: The format of the income statement in NetSuite should look similar to that of the income statement in the Intercompany Calculation Sheet.
1. Starting with the GitLab Inc. consolidated entity, copy the income statement data from NetSuite to the corresponding income statement in the Intercompany Calculation Sheet.
    * The balance under GitLab.com department should be combined with the Marketing department when transferring data to the Intercompany Calculation Sheet.
    * The GitHost balance should be reported under the No Department column.
1. Repeat step 6 for the GitLab Inc (non-consolidated/index.html.md) and GitLab LTD subsidiaries. There is no need to perform this for GitLab BV as this balance will autofill. 
    * For GitLab LTD, you’ll need to convert the income statement from GBP to USD:
        * Start by the running the consolidated income statement in NetSuite and changing the column display filter to Subsidiary.
        * Then take net income from the GitLab LTD column and divide this balance by the net income found in the GitLab LTD income statement. The resulting GBP-USD exchange rate should be used to convert the income statement. 
1. Review the data for accuracy and verify that the formulas in the spreadsheet are up-to-date.
1. After reviewing, there should be no variances in column AL.
1. Update the balance in cell O100 so that the balance in cell R106 autocorrects to zero.
1. Update the exchange rate in cells O1110-O112 and cell O118 with this month’s rate*.
    * This exchange rate (USD to EUR/index.html.md) can be found in NetSuite under the Lists tab, then under the Accounting and Consolidated Exchange Rates subtabs.
1. Now, it’s time to create the intercompany vendor bills and customer invoices.
1. This can be tricky, so be sure to follow the workflow found in the Intercompany Calculation Sheet, starting under cell Q110 (the cells in column R reflect the exact names given in NetSuite, which is relevant for this exercise/index.html.md).
    * There will be two invoices and two bills issued between GitLab BV and GitLab Inc.
    * There will be one invoice and one bill issued between GitLab BV and GitLab LTD.
1. The amounts in cells N113 and N119 will be used to create the intercompany transactions between GitLab BV and GitLab Inc.
1. For increased speed and accuracy, start by finding an invoice (or bill/index.html.md) from the previous month, then use the Make Copy feature in NetSuite to create a duplicate.
    * This will allow you to review the data you are transferring, while comparing it to the previous month for additional guidance.
1. Complete the GitLab BV-GitLab Inc intercompany transactions by repeating step 15 for all of the required bills and invoices.
1. Next comes the GitLab BV-GitLab LTD transactions, which differ slightly from the GitLab BV-GitLab Inc transactions.
1. In NetSuite, download the GitLab LTD income statement in GBP.
1. Take the total overhead stated in GBP and add 6%. 
    * This will be reported in the invoice from GitLab BV to GitLab LTD.
1. Once again, repeat step 15 for the GitLab BV-GitLab LTD transactions.
1. When the transactions are complete, you can check your work by verifying that the affected Revenue and COGS accounts offset each other.
