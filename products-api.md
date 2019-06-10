# Retargeting Product Update API

Retargeting Product Update API methods allows you to manage product details (price, stock, name, image, etc).

## Get product details

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);
 
/** Check Product details by ID. **/
print_r($client->products->get(
    ['productId' => '155477']
));
```

### Response (product with variations)

```json
{
    "version": "1.0",
    "status": 200,
    "message": "OK",
    "data": {
        "realid": "155477",
        "price": 100,
        "promo": 0,
        "stock": [{
            "code": "m",
            "explicit": ["m"],
            "stock": 0
        }, {
            "code": "l",
            "explicit": ["l"],
            "stock": 0
        }, {
            "code": "s",
            "explicit": ["s"],
            "stock": 1
        }]
    }
}
```

### Response (product without variations)

```json
{
    "version": "1.0",
    "status": 200,
    "message": "OK",
    "data": {
        "realid": "155477",
        "price": 100,
        "promo": 0,
        "stock": [{
            "code": null,
            "explicit": null,
            "stock": 1
        }]
    }
}
```

### Response - Product not found

```json
{
    "version": "1.0",
    "status": "400",
    "message": "Bad Request",
    "error": "Invalid Product ID"
}
```

---

## Update product details (price, promo, stock, name, image) - Product without variations

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'image' => 'https://picsum.photos/200/300',
    'name' => 'New Product Name',
    'price' => 500,
    'promo' => 0,
    'stock' => true
]));
```

## Update product details (price, promo, stock, name, image) - Product with variations

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'image' => 'https://picsum.photos/200/300',
    'name' => 'New Product Name',
    'price' => 500,
    'promo' => 0,
    'stock' =>[
		's' => true,
		'm' => false,
		'l' => true 
		]
]));
```

## Update product Stock - Product with variations

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'stock' =>[
		's' => true,
		'm' => false,
		'l' => true 
		]
]));
```

## Update product Stock - Product without variations

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'stock' => false
]));
```

## Update product Name

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'name' => 'New Product Name'
]));
```

## Update product Image

```php
<?php
 
require_once "api/Retargeting_REST_API_Client.php";
 
// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("xxxxxxxxxxxxxxx");
 
// set response format to JSON
$client->setResponseFormat("json");
 
// not decode the string
$client->setDecoding(false);

print_r($client->products->update([
    'productId' => '155477',
    'image' => 'https://picsum.photos/200/300'
]));
```

## Response

```json
{
    "version":"1.0",
    "status":200,
    "message":"OK",
    "data":{
        "success":true,
        "message":
        "Product updated."
    }
}
```
