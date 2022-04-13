# Solver Smart Search
| Data Group       | Entity       |  Type          | Importance  | Description |
|:------------:|:-------------:|:------------:|:------------:|:------------:|
| products | product_id |  string  | mandatory | Unique product ID |
| products | product_name | string | mandatory | Unique product name |
| products | product_description | string | recommended | Detailed description of product |
| products | price | float  | optional | Regular price of product per unit of measure |
| products | currency | float  | optional | optional | optional | optional | Currency transactions are made in |
| products | price_before_vat | float | optional | Price of product before VAT |
| products | product_vat | float | optional | VAT on top of product price |
| products | loyalty_points | float  | optional | Loyalty point that can be achivied by purchasing the product |
| products | supplier_id | string | mandatory | Unique ID of supplier of product |
| products | supplier_name | string  | recommended | Unique name of supplier of product |
| products | brand_id | string  | mandatory | Unique ID of brand of product |
| products | brand_name | string  | recommended | Unique name of brand of product|
| products | category_id | string | mandatory | Unique ID of category product belongs|
| products | lawest_category_level | string| mandatory | recommended Category most common used|
| products | category_level_0 | string | mandatory | Highest category level |
| products | category_level_1 | string | mandatory | Category level |
| products | category_level_2 | string | mandatory | Category level |
| products | further_category_breakdown | string | mandatory | Deeper categorization |
| products | unit_measure | string | recommended | Measure unit for product |
| products | product_viber_name | string | mandatory | Unique product name for communication through online channels |
| products | product_sms_name | string | recommended | Unique product name for communication through sms |
| products | product_main_image | string | optional | URL to main product images |
| products | product_images | array of string | optional | Array of URLs to other product images |
| products | additional_product_data | string | optional | Additional, not predefined data |
