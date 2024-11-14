# Magento 2 GST India
The __Magento 2 GST India Extension__ is designed specifically for Indian merchants to streamline GST calculations, automate tax management, and ensure accurate invoicing as per the latest Indian tax regulations. 
This extension enhances Magento 2 stores by automating GST calculations for Indian businesses, ensuring accurate tax implementation, seamless invoicing and efficient operations.
## How It Works+
The __Magento 2 GST Extension__ integrates GST compliance seamlessly into your Magento 2 store. It automatically calculates GST based on product type, tax slabs, and customer location, updating the tax rates at checkout and on invoices. 
This saves time and eliminates the need for manual tax calculations, offering a smooth experience for customers and merchants alike.
## Key Features
- __Automated GST Application Based on Business Origin:__ Automatically calculates and applies SGST, CGST, IGST, or UTGST based on the business origin and the customer’s location within India’s states and union territories.
- __Flexible Price Settings:__ Define product prices as inclusive or exclusive of GST in the catalog to accurately calculate tax amounts on purchases.
- __Digital Signature Integration:__ Upload a digital signature image and add signature text to be included in order invoice PDFs, enhancing document authenticity.
- __GST on Shipping Charges:__ Extend GST calculations to shipping fees, with an option to apply GST inclusively or exclusively on shipping.
- __Customizable Category and Product-Specific GST Settings:__ Configure GST rates for specific categories or individual products with dropdown options, offering greater flexibility.
- __Threshold-Based GST Rates:__ Set a minimum product price for applying the default GST rate. For products below this price, a separate GST rate can be configured, allowing dynamic tax adjustments.
- __HSN Code Integration:__ Enter HSN codes for products to ensure accurate tax categorization and compliance.
- __Automated GST Calculation in Cart:__ GST is calculated automatically and applied to the cart subtotal based on the customer’s destination address, applicable tax slab, and the business origin.
- __Detailed GST Breakdown in Order Documents:__ Provides a comprehensive view of GST details in order-related documents such as the order view, invoice, credit memo, new order email, shipment PDFs, and the My Account section.
- __Backend Order Creation with GST:__ GST is seamlessly applied during backend order creation, ensuring consistent tax calculations.
- __Comprehensive GST Reports:__ Access and export all GST order details via a dedicated GST Orders Report tab under Reports, simplifying compliance tracking.
- __Enhanced Invoice Details:__ Key information such as GSTIN, CIN, PAN, state code, HSN code, itemised GST breakdown, and digital signature are included in invoice PDFs, ensuring compliance and clarity.
## GST Tax Calculation Based on HSN Code
The extension calculates GST based on the Harmonized System of Nomenclature (HSN) code associated with each product. Each product is assigned an HSN code that determines its tax rate, ensuring compliance with India's tax structure.
- __Automated HSN Code Handling__ – Assigns and calculates GST based on HSN code.
- __Accurate Taxation__ – Calculates CGST, SGST, and IGST depending on transaction type.
## Easy Intra- and Inter-State Tax Compliance
Indian tax regulations specify different rates for intra-state and inter-state transactions. This extension ensures accurate tax calculation and applies CGST and SGST for intra-state, and IGST for inter-state transactions, without requiring any manual configuration.
- __CGST and SGST for Intra-State__ – Automatically splits the GST for local sales.
- __IGST for Inter-State__ – Accurately applies IGST for sales across state borders.
## GST-Compliant Invoices
Invoicing is an essential aspect of GST compliance. This extension generates GST-compliant invoices automatically, displaying GST details such as CGST, SGST, IGST, HSN codes, and total GST collected. This helps in avoiding any discrepancies in tax records.
- __Automated GST Invoice Generation__ – No manual editing needed for GST-compliant invoices.
- __Displays Tax Details Clearly__ – Clear breakdown of CGST, SGST, and IGST for transparency.
## Detailed GST Reports
For business owners, maintaining GST records and generating reports is simplified with the GST reports feature. The extension provides detailed reports on GST collections, making it easy to track, audit, and file GST returns.
- __Comprehensive Reports__ – Track CGST, SGST, and IGST collections over any period.
- __Easy Auditing__ – Simplifies the process of tax filing and auditing.
## Additional Configuration Options
The extension offers customizable settings to modify tax rates, GST number validation, and address-based rules to ensure alignment with the latest tax laws.
- __Adjustable Tax Slabs__ – Configure tax slabs based on product types or business needs.
- __Address-Based Tax Rules__ – Apply GST accurately depending on the customer’s billing and shipping address.
## Extension Installation
To install the GST Extension in your Magento 2 store follow the following steps:
### Step 1: 
Extract the zip folder and upload our extension to the root of your Magento 2 directory via FTP.
### Step 2:
Login to your SSH and run below commands step by step:
- php bin/magento setup:upgrade
- For Magento version 2.0.x to 2.1.x - php bin/magento setup:static-content:deploy
- For Magento version 2.2.x & above - php bin/magento setup:static-content:deploy –f
- php bin/magento cache:flush
__Note:__ For Magento versions 2.2.4 or earlier, please follow these steps:
__Navigate to:__ Magento_Root\vendor\temando\module-shipping-m2\etc\events.xml
__Locate the following code:__
```
<event name="sales_quote_address_save_after">
<observer name="temando_persist_checkout_fields" instance="Temando\Shipping\Observer\SaveCheckoutFieldsObserver"/>
</event>
```
Replace it with:
```
<!--<event name="sales_quote_address_save_after">
    <observer name="temando_persist_checkout_fields" instance="Temando\Shipping\Observer\SaveCheckoutFieldsObserver"/>
</event>-->
```
### Step 3: Verify Installation
After completing the setup, navigate to the Admin Panel and confirm the extension is enabled under Stores > Configuration.

## How to Set Up the Magento 2 GST Extension
Before enabling and configuring the extension, ensure the following settings are updated in your Magento 2 store:
- __Set Default Country for GST:__
Go to ```Stores > Configuration``` and under ```General > General > Country``` Options, set the Default Country to India. This ensures GST settings are applied for India.
- __Set Default Tax Destination:__ 
Navigate to ```Stores > Configuration > Sales > Tax``` and under Default Tax Destination Calculation, set the Default Country to India and the State to * (All States).
- __Configure Tax Classes:__ 
Head to ```Stores > Configuration > Sales > Tax > Tax Classes``` and set both Tax Class for Shipping and Default Tax Class for Product to "None." Ensure the Use System Value checkbox is selected for both Catalog Prices and Shipping Prices under Calculation Settings.
- __Select GST Calculation Method:__ 
Go to ```Stores > Configuration > Sales > Tax``` and under Calculation Settings, choose whether GST will be calculated based on the Shipping Address or Billing Address.
- __Set Subtotal Display Settings:__ 
Under ```Stores > Configuration > Sales > Tax > Tax Classes```, select your preferred options for Shopping Cart Display Settings and Orders, Invoices, Credit Memos Display Settings for how the Subtotal will appear in the shopping cart and other documents.
- __Ensure System Values for Other Settings:__ 
Double-check that the Use System Value checkbox is selected for all other options to maintain default configurations.
### Step1: Enable the extension & configure
For configuring the GST India extension, log in to Magento 2 and navigate to Stores > Configuration where you’ll find settings to manage the extension:
!
