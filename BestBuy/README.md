# BestBuy API Playground

## Pre-requirements
To use BestBuy API Playground, the following items needed to be installed:
- Node.js v10.15.3
- npm v6.4.1

Follow the instructions on this [guide](https://github.com/bestbuy/api-playground/#getting-started) to install the API Playground.

Downloaded Postman from [Get Postman](https://www.getpostman.com/downloads/) and installed on my machine.

Installed *newman*, using the following command line:
> npm install -g newman

This will install newman to be executed anywhere in the machine.

## List of test cases

I created the a collection in Postman containing, at least, one request per Playground API. For each request, I created a simple test case in Javascript to check the HTTP status code.

The tests cases were divided by classes of API
- Products
	- Get all products
	- Get product by ID
	- Get all products, limit to 1 result
	- Get all products, skip to the 25,001th result
	- Get all products, sort by highest price (descending)
	- Get all products, sort by lowest price (ascending)
	- Get all products, but only show the name and price in the result
	- Get products of type HardGood
	- Get products less than or equal to $1.00
	- Get products that have 'star wars' in the name and are under $30
	- Get products that are either $0.99 or $1.99
	- Get products that have a shipping price of more than $10
	- Get products that are not HardGood or Software
	- Get products that are in category name "Coffee Pods"
	- Get products that are in category ID "abcat0106004" (TV Mounts)
	- Post a new Product
	- Delete a Product by ID
	- Update a Product by ID
- Stores
	- Get All Stores
	- Post new Store
	- Get Store by ID
	- Edit Store by ID
	- Delete Store by ID
- Services
	- Get All Services
	- Create new Service
	- Get Service by ID
	- Edit Service by ID
	- Delete Service by ID
- Categories
	- Get All Categories
	- Create new category
	- Get Category by ID
	- Edit Category by ID
	- Delete Category by ID
- Utilities
	- Get API Version
	- Health check
	
To run the tests, one must execute the following command line:
> newman run BestBuy.postman_collection.json

The test execution result will show a table in the following format:

|                  | executed|   failed|
|------------------|---------|---------|
|iterations        |        1|        0|
|requests          |       35|        0|
|test-scripts      |       35|        0|
|prerequest-scripts|        0|        0|
|assertions        |       35|        8|
|                                      |
|total run duration: 2.5s              |
|total data received: 169.46KB (approx)|
|av. response time: 46ms               |
|                                      |

## Comments
Another way of working with Postman would be to edit the *package.json* file to add the *newman* command to it as well as its depency, so one could use *npm run <scripts>* to execute the tests as part of the application package.

Another solution would be creating a Java project and add a reference to the [Karate Framework](https://github.com/intuit/karate#http-basic-authentication-example) to the Maven *pom.xml* file, and then write Gherkin-style test cases.