---
layout: markdown_page
title: "Swag Shop Transactions"
---

## On this page
{:.no_toc}

- TOC
{:toc}



## Posting Swag Shop transactions in NetSuite
Transactions from the Swag Shop are remitted to the Comerica checking account daily and should be booked in NetSuite at the end of each month, per the guidelines below. Login credentials for Shopify and Avalara are located in 1Password.

1. In Shopify, download the transaction report in CSV format (found under Orders, then Export/index.html.md).
  * This report contains swag shop revenue and tax data to be recorded in NetSuite.
1. In Printfection, download the orders report (found under Reports, then Run a Report/index.html.md).
  * This report will be used to allocate transaction cost data between promotional, shipping, and merchandise.
1. In the Shopify transaction report, the amounts in column L reflect the total funds received from each order.
1. The total tax collected per transaction can be found in column K, with the supporting details found in columns BE-BH.
1. Create a journal entry in NetSuite under the GitLab Inc subsidiary, using the last day of the month as the entry date.
1. This journal entry has two parts- One to record the revenues and taxes, which are reported in Shopify, and the second part which includes shipping and merchandise cost information reported in Printfection.
  * Using the transaction report from Shopify, create line items for the revenue and various tax liabilities.
    * Carefully review your entries for tax liabilities to ensure they are accurately recorded under the appropriate GL accounts.
  * Using the orders report from Printfection, create line items for the costs of shipping and merchandise.
1. Click Save then proceed to final review of the entry.
1. The journal entry can be tested for accuracy by comparing the balances of the journal entry lines to the balances in the two reports.

## Importing Swag Shop data to Avalara

In [Shopify](https://www.shopify.com/login/index.html.md):
1. Click on "Orders" in the left-hand toolbar.
1. Select "Export" and the desired transaction history period.
1. Download the report in CSV format.
1. Copy the transaction data from the Shopify report to the [Avalara Tax Import template](https://drive.google.com/file/d/19_UBjfqKcnuOWDfHfRVfFRc5L35QF4Gf/view?usp=sharing/index.html.md) located in the Google Drive.
    * Note that the import will fail if the columns that are highlighted green are left blank. Also check to ensure that the state and local tax data is entered into the correct columns. This is required for tax compliance. 
1. Save file for the remaining steps below.

In [Avalara](https://admin-avatax.avalara.net/login.aspx?ReturnUrl=%2fAvaTax%2fTools%2fItemImportUpload.aspx/index.html.md):
1. Click on "Reports".
1. Select the "Import Data" option.
1. When prompted, choose the CSV import option.
1. Check the import status report to ensure all transactions are successfully imported.