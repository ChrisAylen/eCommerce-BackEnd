# Ecommerce Back End

![](https://img.shields.io/badge/license-MIT-blue.svg)
    
## Description
    
This backend is a RESTful API that allows users to create, read, update, and delete products, categories anf tags.

## Table of Contents 

* [Installation](#installation)

* [Usage](#usage)

* [API](#API)

* [Questions](#questions)

* [To Do](#ToDo)

## Installation
    
'npm i' to install the necessary dependencies.

Create a file named .env with the following contents:

```
DB_USER=''
DB_PW=''
DB_NAME='ecommerce_db'
HOST=''
DIALECT='mysql'
```

### Setting up the database

run schema.sql at a mySQL prompt to create the database and tables.
```
source ./db/schema.sql
```
Seed the database:
```
npm run seed
```

## API

The application surfaces a RestFul API that has the following endpoints:
```
/api/products
/api/products/:id
/api/categories
/api/categories/:id
/api/tags
/api/tags/:id
```

## Usage

### Products

#### Get ALL Products
```
curl --request GET \
  --url http://localhost:3001/api/products
  ```
  ```
  curl --request GET \
  --url http://localhost:3001/api/products/7
  ```
#### Get a Product by Id
```
curl --request GET \
  --url http://localhost:3001/api/products/[id]
```

#### Add a Product
```
curl --request POST \
  --url http://localhost:3001/api/products \
  --header 'Content-Type: application/json' \
  --data '{
      "product_name": "PingPongball",
      "price": 299.99,
      "stock": 6,
      "tagIds": [1,2,3,4,5]
}'
```
#### Update a Product
```
curl --request PUT \
  --url http://localhost:3001/api/products/[id] \
  --header 'Content-Type: application/json' \
  --data '{
      "product_name": "product name",
      "price": 300.00,
      "stock": 7,
      "tagIds": [1,2,3,4]
}'
```
#### Delete a Product
```
curl --request DELETE \
  --url http://localhost:3001/api/products/[id]
    
```

### Categories
#### Get ALL Categories
```
curl --request GET \
  --url http://localhost:3001/api/categories
```
#### Get a Category by ID
```
curl --request GET \
  --url http://localhost:3001/api/categories/[id]
```

#### Add a Category
```
curl --request POST \
  --url http://localhost:3001/api/categories \
  --header 'Content-Type: application/json' \
  --data '{
	"category_name": "category to add"
}'
```

#### Update a Category
```
curl --request PUT \
  --url http://localhost:3001/api/categories/[id] \
  --header 'Content-Type: application/json' \
  --data '{
		"category_name": "updated category name"
}'
```
#### Delete a Category
```
curl --request DELETE \
  --url http://localhost:3001/api/categories/[id]
```

### Tags
#### Get ALL Tags
```
curl --request GET \
  --url http://localhost:3001/api/tags
```
#### Get a Tag by ID
```
curl --request GET \

    --url http://localhost:3001/api/tags/[id]
```

#### Add a Tag
```
curl --request POST \
  --url http://localhost:3001/api/tags \
  --header 'Content-Type: application/json' \
  --data '{
			"tag_name": "tag to add"
}'
```

#### Update a Tag
```
curl --request PUT \
    --url http://localhost:3001/api/tags/[id] \
    --header 'Content-Type: application/json' \
    --data '{
                "tag_name": "updated tag name"
}'
```
#### Delete a Tag
```
curl --request DELETE \
    --url http://localhost:3001/api/tags/[id]
```

## License
    
This project is licenced under MIT

## Questions

[More of my work can be found here](https://github.com/ChrisAylen)

## ToDo