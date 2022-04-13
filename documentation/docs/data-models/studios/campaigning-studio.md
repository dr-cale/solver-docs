# Campaigning Studio - Data Models

## Customers

!!! note
    <p>Column <b>customer_id</b> must be unique, as well as <b>alternative_id</b> if provided. </p>
    <p>Column <b>phone_number</b> is mandatory for Viber, WhatsApp and SMS campaigns.</p>
    <p>Column <b>email</b> is mandatory for email campaigns</p>

| Entity       |  Type          | Mandatory | Description | 
|:------------:|:-------------:|:------------:|:------------:|
| customer_id | string | true | |
| first_name | string | false | |
| last_name | string | false | |
| phone_number |  string  | false | |
| email |  string  | false | |
| birth_date | date  | false | |
| age | int | false | |
| gender | string  | false | |
| zip_code | string | false | |
| driver_licence| boolean | false | |
| pet_owner| boolean | false | |
| parent| boolean | false |  |

## Items

!!! note
    <p>Items table is not mandatory if campaign metrics and personalized campaigns are not included.</p>
    <p>Column <b>product_id</b> must be unique, as well as <b>alternative_id</b> if provided. </p>

| Entity       |  Type          | Mandatory | Description |
|:------------:|:-------------:|:------------:|:------------:|
| product_id |  string  | true | |
| alternative_id | string  | false | |
| product_name | string | true | |
| brand_id | string| false | |
| supplier_id | string | false | |
| supplier | string  | false | |
| category_id | string | false | |
| status | string | false | |
| unit_measure | string | false | |
| season_product | boolean| false | |
| lowest_category_name | string | false | |
| hierarchy_path | string  | false | |
| node_depth | string  | false | |
| category_level_0 | string  | false | |
| category_level_1 | string  | false | |
| category_level_2 | string  | false | |
| category_level_3 | string  | false | |
| category_level_4 | string  | false | |
| category_level_5 | string  | false | |
| brand | string  | false | |
| discount_price | float  | false | |
| points_collected | float  | false | |
| regular_price | float  | true | |


## Leaflet

!!! note
   <p> <span>Leaflet table is not mandatory if campaign metrics and personalized campaigns are not included. </span></p>
   <p> <span>Column <b>product_id</b> must be unique, as well as <b>alternative_id</b> if provided. </span></p>
   <p> <span>Column <b>discount_price</b> must be lower than <b>regular_price</b>, if provided. </span></p>

Leaflet data set is used to determine if products are currently used in campaign to attract customers for more conversions. 

| Entity       |  Type          | Mandatory | Description | What to discuss |
|:------------:|:-------------:|:------------:|:------------:|:------------:|
| leaflet_id | string  | false | |
| leaflet_name | string | false | |
| effective_start_date | string | false | |
| effective_end_date | string | false | | |
| product_id |  string  | true | |
| alternative_id | string  | false | |
| product_name | string | true | |
| brand_id | string| false | |
| supplier_id | string | false | |
| supplier | string  | false | |
| category_id | string | false | |
| status | string | false | |
| unit_measure | string | false | |
| season_product | boolean| false | |
| lowest_category_name | string | false | |
| hierarchy_path | string  | false | |
| node_depth | string  | false | |
| category_level_0 | string  | false | |
| category_level_1 | string  | false | |
| category_level_2 | string  | false | |
| category_level_3 | string  | false | |
| category_level_4 | string  | false | |
| category_level_5 | string  | false | |
| brand | string  | false | |
| discount_price | float  | false | |
| points_collected | float  | false | |
| regular_price | float  | true | |



## Transactions

!!! note
    <p><span>Transactions table is not mandatory if campaign metrics and personalized campaigns are not included. </span></p>
    <p><span>Column <b>product_id</b> must be unique, as well as <b>alternative_id</b> if provided. </span></p>
    <p><span>Column <b>discount_price</b> must be lower than <b>regular_price</b>, if provided. </span></p>

| Entity       |  Type          | Mandatory | Description |
|:------------:|:-------------:|:------------:| :------------:|
| invoice_id | string  | true | |
| invoice_type | string  | true | |
| purchase_date | datetime | true | |
| customer_id | string | true | | |
| product_id |  string  | true | |
| product_name | string | false | |
| store_id |  string  | false | |
| price | float  | true | |
| quantity | float | true | |
| price_before_vat | float  | false | |
| product_vat | float| false | |
| supplier_id | string | false | |
| supplier | string  | false | |
| brand_id | string  | false | |
| brand | string  | false | |
| category_id | string | false | |
| unit_measure | string | false | |
| lowest_category_name | string | false | |
| category_level_0 | string  | false | |
| category_level_1 | string  | false | | 
| category_level_2 | string  | false | |
| category_level_3 | string  | false | |
| category_level_4 | string  | false | | 
| category_level_5 | string  | false | |

## Clicks


| Entity       |  Type          | Mandatory |
|:------------:|:-------------:|:------------:|


