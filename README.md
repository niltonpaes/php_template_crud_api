# PHP Rest API Template - CRUD

This is a template for a PHP Rest API that provides CRUD operations in PHP and MySQL.

## Some hightlights:

* Use of PDO extension to connect to MySQL (config/database.php)
  * connect
  * execute DML commands
  * retrieve data
* Pagination
* JSON manipulation

## Live application:

### Read all products
call: https://niltonpaes.website/php_templates/php_template_crud_api/product/read.php

return:
```
{
    "records": [
        {
            "id": "42",
            "name": "Nike Shoes for Men",
            "description": "Nike Shoes",
            "price": "12999",
            "category_id": "3",
            "category_name": "Motors"
        },
        {
            "id": "31",
            "name": "Amanda Waller Shirt",
            "description": "New awesome shirt!",
            "price": "333",
            "category_id": "1",
            "category_name": "Fashion"
        }
	]
}
```



### Create product
call (post): https://niltonpaes.website/php_templates/php_template_crud_api/product/create.php

body:
```
{
    "name" : "New product 1",
    "price" : "100",
    "description" : "Description new product 1.",
    "category_id" : 2,
    "created" : "2018-01-01 00:00:00"
}
```
return:
```
{
    "message": "Product was created."
}
```



### Read one product
call (get): https://niltonpaes.website/php_templates/php_template_crud_api/product/read_one.php?id=31

return:
```
{
    "id": "31",
    "name": "Amanda Waller Shirt",
    "description": "New awesome shirt!",
    "price": "333",
    "category_id": "1",
    "category_name": "Fashion"
}
```



### Update product
call (post): https://niltonpaes.website/php_templates/php_template_crud_api/product/update.php

body:
```
{
    "id": "31",
    "name": "Amanda Waller Shirt NEW",
    "price": "333",
    "description": "New awesome shirt!",  
    "category_id": "1",
    "created" : "2018-01-01 00:00:00"
}
```
return:
```
{
    "message": "Product was updated."
}
```



### Delete product
call (post): https://niltonpaes.website/php_templates/php_template_crud_api/product/delete.php

body:
```
{
    "id" : "43"
}
```
return:
```
{
    "message": "Product was deleted."
}
```



### Search products
call (get): https://niltonpaes.website/php_templates/php_template_crud_api/product/search.php?s=shirt

return:
```
{
    "records": [
        {
            "id": "31",
            "name": "Amanda Waller Shirt NEW",
            "description": "New awesome shirt!",
            "price": "333",
            "category_id": "1",
            "category_name": "Fashion"
        },
        {
            "id": "6",
            "name": "Bench Shirt",
            "description": "The best shirt!",
            "price": "29",
            "category_id": "1",
            "category_name": "Fashion"
        }
    ]
}
```

## Reference
Codeofaninja Tutorials - codeofaninja.com
