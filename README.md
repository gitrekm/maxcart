# MaxCart
This repo contains MAxCart's projects description and implementation détails
## Introduction


The purpose of this project is to solve a business problem about  the abandonment cart to increase sales conversion and gain real-time insights for the e-commerce industry.

the main goals are:
* Analyze the business case and the given dataset
* identify the most suitable approach to solve the given business problems 
* implement/build and deploy the target architecture and data pipeline 
* Analyze the output conformity to the given business problems 
* Share the implementation details via blog posts and YT videos. 

What we will build?
* data pipeline for streaming and batch processing
* CI/CD chain to set up the infra and used managed services
* Data visualization dashboard for business users

What we will learn?
* How to choose the right option for data storage
* How to choose the right service/product for data processing to fit business requirement
* How to implement streaming and batch processing data pipelines
* How to implement machine learning models
* How to communicate final results 

## Business requirements
### 1. Business problem#1
retargeting customers with abandonment cart within 3 min maximum of the session expiration The use case basically is to increase sales conversion by reducing cart abandonment. the output. the retargeting format is to send a personalized email to the subscriber offering free shipping.

### 2. Business problem#2
Identifying products with the most sales attraction in the future in order to anticipate the supplyThe use case basically is to increase sales conversion by reducing cart abandonment. the output.

### 3. Business problem#3
Calculate Customer lifetime value

### 4. Business problem#4
visualize sales data per product within 30 to 45 seconds once the payment is done

## Technical requirements
### 1. set up thedata pipeline for streaming and batch processing

* Ingest sales data in realtime
* clean up the data / ensure data quality (missing values and negative ones)
* prepare the cleaned data to :
  - Business analysts for visualizations
  - data scientists and ML engineers to build ML models. ie: probability estimate of a sale for each product
  instant reaction to retarget customer with abandonment cart by making a new offer to the subscriber and reach it via email in the next 3 minutes (free coupon or free shipping offered)
* Archive historical data to be re-analyzed by data scientists for future ML models

### 2. set up the CI/CD chain

* automate infra and managed services creation and destruction

* setup continuous integration and continuous delivery chain

## Dataset
### 1. Description

This data contains behavior data for 5 months (Oct 2019 – Feb 2020) from a medium cosmetics online store.Each row in the file represents an event. All events are related to products and users. Each event is like many-to-many relation between products and users.Note: if this dataset is too small for you, you can try larger dataset from multi-category store.There are different types of events. See below.Semantics (or how to read it):User userid during session usersession added to shopping cart (property eventtype is equal cart) product productid of the brand of category code (category code) with price at event_time

### 2. Structure
event_timeThe time when the event happened at (in UTC).event_type
Events can be:
- view – a user viewed a product
- cart – a user added a product to shopping cart
- removefromcart – a user removed a product from the shopping cart
- purchase – a user purchased a product

Typical funnel: view => cart => purchase.

product_id: ID of a product
category_id: Product’s category ID
category_code: Product’s category taxonomy (code name) if it was possible to make it. Usually present for meaningful categories and skipped for different kinds of accessories.
brand: The downcased string of brand names. Can be missed.
price: price of a product.
user_id: Permanent user ID.
user_session: Temporary user’s session ID. Same for each user’s session. Is changed every time user comes back to the online store from a long pause.

## How to choose storage option
## streaming pipeline with Google Cloud Dataflow
## Batch processing pipeline with Dataproc
## How to uild ML model with BigQueryML
## Visuialization with Google DataStudio
