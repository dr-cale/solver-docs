
title: Solver AI Suite
template: theme/main.html

# Welcome to Solver AI Suite

For full API documentation visit [API Docs](https://api.thingsolver.com){#api-thingsolver-url target=_blank}.


## Overview


## Items

!!! note

    Column <b>product_id</b> must be unique, as well as <b>alternative_id</b> if provided. 
    <p></p>
    Column <b>discount_price</b> must be lower than <b>regular_price</b>, if provided.

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
| brand | string  | false || | 
| discount_price | float  | false | | 
| points_collected | float  | false | | 
| regular_price | float  | true | | 



## Leaflet

| Entity       |  Type          | Mandatory | Description | What to discuss |
|:------------:|:-------------:|:------------:|:------------:|:------------:|
| leaflet_id | string  | false | | |
| leaflet_name | string | false | | |
| campaign_start_date | string | false | | da li ostaviti campaign_start_date ili effective_start_date i effective_end_date |
| campaign_end_date | string | false | | |
| product_id |  string  | true | | |
| alternative_id | string  | false | | |
| product_name | string | true | | |
| brand_id | string| false | | |
| supplier_id | string | false | | |
| supplier | string  | false | | |
| category_id | string | false | | |
| status | string | false | | |
| unit_measure | string | false | | |
| season_product | boolean| false | | |
| lowest_category_name | string | false | | |
| hierarchy_path | string  | false | | |
| node_depth | string  | false | | |
| category_level_0 | string  | false | | |
| category_level_1 | string  | false | | |
| category_level_2 | string  | false | | |
| category_level_3 | string  | false | | |
| category_level_4 | string  | false | | |
| category_level_5 | string  | false | | |
| brand | string  | false | | |
| discount_price | float  | false | | |
| points_collected | float  | false | | |
| regular_price | float  | true | | |


## Transactions

| Entity       |  Type          | Mandatory | Description | What to discuss |
|:------------:|:-------------:|:------------:| :------------:|:------------:|
| invoice_number | string  | true | | Change to invoice_id|
| invoice_type | string  | true | | New field |
| purchase_date | datetime | true | | invoice_datetime, da li da bude Datetime ili string: odluka Datetime |
| customer_id | string | true | | |
| product_id |  string  | true | Must match with product tables | |
| product_name | string | false | | |
| store_id |  string  | false | | |
| price | float  | true | | |
| quantity | float | true | | |
| price_before_vat | float  | false | | |
| product_vat | float| false | | |
| supplier_id | string | false | | |
| supplier | string  | false | | |
| brand_id | string  | false | | Brand should be taken from product table. Changes on metrics should be applied  |
| brand | string  | false | | Brand should be taken from product table. Changes on metrics should be applied  |
| category_id | string | false | | Brand should be taken from product table.  |
| unit_measure | string | false | | |
| lowest_category_name | string | false | | Category name should be taken from product table |
| category_level_0 | string  | false | | Category name should be taken from product table |
| category_level_1 | string  | false | | Category name should be taken from product table |
| category_level_2 | string  | false | | Category name should be taken from product table |
| category_level_3 | string  | false | | Category name should be taken from product table |
| category_level_4 | string  | false | | Category name should be taken from product table |
| category_level_5 | string  | false | | Category name should be taken from product table |


## Customers

| Entity       |  Type          | Mandatory | Description | What to discuss |
|:------------:|:-------------:|:------------:|:------------:|:------------:|
| customer_id | string | true | | |
| phone_number |  string  | false | | |
| email |  string  | false | | |
| birth_date | date  | false | | |
| age | int | false | | |
| gender | string  | false | | |
| zip_code | string | false | | |
| driver_licence| boolean | false | | |
| pet_owner| boolean | false | | |
| parent| boolean | false |  | |



## Clicks


| Entity       |  Type          | Mandatory | What to discuss |
|:------------:|:-------------:|:------------:| :------------:|
