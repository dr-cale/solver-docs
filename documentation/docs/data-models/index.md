# Data Models Overview


!!! notes
    <p><span> <b>Transactions note</b>: Transaction group data for Campaigning Studio is mandatory only if <b>Personalized Campaigns</b> are included</span></p>
    <p><span><b>Leaflets note</b>: Value of discount_price column should be lower than value of price (regulat price) column</span></p>

| Data Group       | Entity       |  Type          | CUSTOMER STUDIO | PRODUCT STUDIO | CAMPAIGNING | SEARCH TOUCHPOINT | Description |
|:------------:|:-------------:|:------------:|:------------:|:------------:|:------------:|:------------:|:------------:|
| transactions | invoice_id | string  | mandatory | mandatory | mandatory | mandatory | Unique invoice ID |
| transactions | invoice_type | string  | recommended | recommended | recommended | recommended | Status of the invoice finalized/cancelled/amended |
| transactions | purchase_datetime | datetime | mandatory | mandatory | mandatory | mandatory | Timestamp of the invoice |
| transactions | customer_id | string | mandatory | mandatory | mandatory | mandatory | Unique customer ID if available (loyalty card or similar) |
| transactions | product_id | string | mandatory | mandatory | mandatory | mandatory | Unique product ID |
| transactions | store_id |  string  | recommended | recommended | mandatory | mandatory | Unique ID of store where purchase happen|
| transactions | price | float  | mandatory | mandatory | mandatory | mandatory | Price paid (either for a single item or of that product or all if more than one) |
| transactions | currency | float  | optional | optional | optional | optional | Currency transactions are made in |
| transactions | quantity | float | mandatory | mandatory | mandatory | mandatory | Purchased quantity |
| transactions | price_before_vat | float  | optional | optional | optional | optional | Price of product before VAT |
| transactions | product_vat | floa t| optional | optional | optional | optional | VAT on top of product price |
| transactions | discount_amount | float | optional | optional | optional | recommended | Discount on product price |
| transactions | loyalty_points | float | recommended | recommended | optional | recommended | Points earned by purchasing product |
| products | product_id |  string  | mandatory | mandatory | mandatory | mandatory | Unique product ID |
| products | product_name | string | recommended | recommended | recommended | recommended | Unique product name |
[ products | product_description | string | recommended | recommended | recommended | recommended | Detailed description of product |
| products | price | float  | mandatory | mandatory | mandatory | mandatory | Regular price of product per unit of measure |
| products | price_before_vat | float  | optional | optional | optional | optional | Price of product before VAT |
| products | product_vat | float | optional | optional | optional | optional | VAT on top of product price |
| products | loyalty_points | float  | optional | optional | optional | optional | Loyalty point that can be achivied by purchasing the product |
| products | supplier_id | string | recommended | recommended | recommended | recommended | Unique ID of supplier of product |
| products | supplier_name | string  | recommended | recommended | recommended | recommended | Unique name of supplier of product |
| products | brand_id | string  | recommended | recommended | recommended | recommended | Unique ID of brand of product |
| products | brand_name | string  | recommended | recommended | recommended | recommended | Unique name of brand of product|
| products | category_id | string | recommended | recommended | recommended | recommended | Unique ID of category product belongs|
| products | lawest_category_level | string | recommended | recommended | recommended | recommended | Category most common used|
| products | category_level_0 | string | recommended | recommended | recommended | recommended | Highest category level |
| products | category_level_1 | string | recommended | recommended | recommended | recommended | Category level |
| products | category_level_2 | string | recommended | recommended | recommended | recommended | Category level |
| products | category_level_3 | string | recommended | recommended | recommended | recommended | Category level |
| products | category_level_4 | string | recommended | recommended | recommended | recommended | Category level |
| products | category_level_5 | string | recommended | recommended | recommended | recommended | Category level |
| products | further_category_breakdown | string | recommended | recommended | recommended | recommended | Deeper categorization |
| products | unit_measure | string | recommended | recommended | recommended | recommended | Measure unit for product |
| products | product_viber_name | string | recommended | recommended | mandatory | recommended | Unique product name for communication through online channels |
| products | product_sms_name | string | recommended | recommended | mandatory | recommended | Unique product name for communication through sms |
| products | product_main_image | string | recommended | recommended | mandatory | recommended | URL to main product images |
| products | product_images | array of string | recommended | recommended | recommended | recommended | Array of URLs to other product images |
| products | additional_product_data | string | optional | recommended | recommended | recommended | Additional, not predefined data |
| customers | customer_id |  string  | mandatory | mandatory | mandatory | mandatory | Unique customer ID or loyalty card id |
| customers | phone_number |  string  | recommended | recommended | mandatory | recommended | Phone number to communicate to customer |
| customers | email |  string  | recommended | recommended | mandatory | recommended | Email to communicate to customer |
| customers | gender |  string  | mrecommendedandatory | recommended | recommended | recommended | Gender of customer |
| customers | age |  string  | recommended | recommended | recommended | recommended | Age of customer |
| customers | city |  string  | recommended | recommended | recommended | recommended | City where customer open card or agree to live in |
| customers | customer_since |  string  | recommended | recommended | recommended | recommended | First appereance of customer |
| customers | zip_code |  string  | recommended | recommended | recommended | recommended | Zip code for customer's location |
| customers | email_consent |  string  | optional | optional | mandatory | mandatory | Flag if customer want to receive emails |
| customers | sms_consent |  string  | optional | optional | mandatory | mandatory | Flag if customer want to receive sms |
| customers | viber_consent |  string  | optional | optional | mandatory | mandatory | Flag if customer want to receive viber |
| customers | whatsapp_consent |  string  | optional | optional | mandatory | optional | Flag if customer want to receive whatsapp |
| customers | additional_customer_data |  string  | optional | optional | optional | optional | Additional data related to customer |
| stores | store_id |  string  | mandatory | mandatory | mandatory | mandatory | Unique store ID |
| stores | store_name |  string  | recommended | recommended | recommended | recommended | Name of store |
| stores | store_type |  string  | recommended | recommended | recommended | recommended | Type of store if there are different types |
| stores | coordinates |  string  | optional | optional | optional | optional | Coordinates of store |
| stores | address |  string  | recommended | recommended | recommended | recommended | Age of customer |
| stores | city |  string  | recommended | recommended | recommended | recommended | City where store is located |
| stores | region |  string  | optional | optional | optional | optional | Region where store is located |
| stores | country |  string  | optional | optional | optional | optional | Country where store is located |
| stores | zip_code |  string  | optional | optional | optional | optional | Zip code where store is located |
| stores | store_size |  string  | optional | optional | optional | optional | Store size |
| leaflets | product_id |  string  | mandatory | mandatory | mandatory | mandatory | Unique product ID |
| leaflets | product_name | string | mandatory | mandatory | mandatory | mandatory | Unique product name |
[ leaflets | product_description | string | recommended | recommended | recommended | recommended | Detailed description of product |
| products | price | float  | mandatory | mandatory | mandatory | mandatory | Regular price of product per unit of measure |
| products | discount_price | float  | mandatory | mandatory | mandatory | mandatory | Discounted price of product per unit of measure |
| products | price_before_vat | float  | optional | optional | optional | optional | Price of product before VAT |
| products | product_vat | float | optional | optional | optional | optional | VAT on top of product price |
| products | loyalty_points | float  | optional | optional | optional | optional | Loyalty point that can be achivied by purchasing the product |
| leaflets | supplier_id | string | recommended | recommended | recommended | recommended | Unique ID of supplier of product |
| leaflets | supplier_name | string  | recommended | recommended | recommended | recommended | Unique name of supplier of product |
| leaflets | brand_id | string  | recommended | recommended | recommended | recommended | Unique ID of brand of product |
| leaflets | brand_name | string  | recommended | recommended | recommended | recommended | Unique name of brand of product|
| leaflets | category_id | string | recommended | recommended | recommended | recommended | Unique ID of category product belongs|
| leaflets | lawest_category_level | string | recommended | recommended | recommended | recommended | Category most common used|
| leaflets | category_level_0 | string | recommended | recommended | recommended | recommended | Highest category level |
| leaflets | category_level_1 | string | optional | optional | optional | optional | Category level |
| leaflets | category_level_2 | string | optional | optional | optional | optional | Category level |
| leaflets | category_level_3 | string | optional | optional | optional | optional | Category level |
| leaflets | category_level_4 | string | optional | optional | optional | optional | Category level |
| leaflets | category_level_5 | string | optional | optional | optional | optional | Category level |
| leaflets | unit_measure | string | recommended | recommended | recommended | recommended | Measure unit for product |
| leaflets | additional_product_data | string | optional | optional | optional | optional | Additional, not predefined data |
