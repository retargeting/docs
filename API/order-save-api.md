#REST API: order/save
Push an order to Retargeting.

#Resource URLs
**JSON**: https://retargeting.biz/api/1.0/order/save.json

**Serial**: https://retargeting.biz/api/1.0/order/save.serial

#Parameters
|    **Parameter**    |    **Type**    |    **Required**    |    **Description**    |
|---|---|---|---|
|  order_no  |  Number or text  |  Required  |  Unique number of the order recorded  |
|  lastname  |  Text  |  Required  |  name of the buyer |
|  firstname  |  Text  |  Required  |  buyer surname  |
|  email  |  Email  |  Required  |  buyer e-mail address  |
|  phone  |  Text  |  Required  |  phone number of the buyer  |
|  state  |  Text  |  Required  |  district address  |
|  city  |  Text  |  Required  |  city address  |
|  adress  |  Text  |  Required  |  buyer address  |
|  discount  |  Number/0  |  Required  |  the amount / value by which the total amount was reduced. Note that we are not talking about the discount value (e.g. 10%), but the money amount (e.g. 5$ discount for a 100$ order). If there is no discount applied on the order, send value 0.  |
|  discount_code  |  Text  |  Required  |  the discount code used when placing the order.  |
|  shipping  |  Number or text  |  Required  |  value / amount paid for the shipping (shipping fee). If there is no shipping charge, send value 0.  |
|  fees  |  Number or text  |  Required  |  value/amount paid for the fees. If there is no fees charge, send value 0.  |
|  rebates  |  Number or text  |  Required  |  value/amount paid for the rebates. If there is no rebates charge, send value 0.  |
|  total  |  Number or text  |  Required  |  amount / total amount of payment for the order sent. Note that this the total amount the buyer actually pays, the amount obtained after applying any discount and/or shipping fee.  |

Products ordered are contained in the second parameter of the function, which is Array type. Details for each product are added in Array through an object that has the following properties: id, quantity, price, variation_code

|    **Parameter**    |    **Type**    |    **Required**    |    **Description**    |
|---|---|---|---|
|  products.id  |  Text  |  Required  |  product ID  |
|  products.quantity  |  Text  |  Required  |  quantity ordered  |
|  products.price  |  Text  |  Required  |   unit price of the product (per piece)  |
|  products.variation_code  |  Text  |  Required  |  variation code of sent product – for variation code format and other details see variations addToCart functions and setVariation. If the product does not have variation will send a empty string (no character string "")  |
|	callback_function 	|	Function	|	Optional	|	With this parameter you can define a function that runs itself after the action's parent function executes.	|

#Request Example

``` javascript
// 1. to receive a JSON response

require_once "api/Retargeting_REST_API_Client.php";

// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("REST_API_KEY");

// set response format to JSON
$client->setResponseFormat("json");

// set to not decode the string
$client->setDecoding(false);

// send order save request
$response = $client->order->save(
    array(
        "order_no" => "235",
        "lastname" => "Doe",
        "firstname" => "John",
        "email" => "johndoe@mail.com",
        "phone" => "0722444444",
        "state" => "United Kingdom",
        "city" => "Londone",
        "address" => "Tottenham Street, no. 11",
        "discount_code" => ["EEE30PR"],
        "discount" => 50,
        "shipping" => 10,
        "rebates" => 0,
        "fees" => 0,
        "total" => 3800
    ),
    array(
        array('id' => 307, 'quantity' => 5, 'price' => 500, 'variation_code' => ""),
        array('id' => 105, 'quantity' => 1, 'price' => 150, 'variation_code' => "42-B"),
        array('id' => 105, 'quantity' => 2, 'price' => 150, 'variation_code' => "42-W"),
        array('id' => 48, 'quantity' => 10, 'price' => 85, 'variation_code' => "M")
    )
);


// 2. to receive a serialized response

require_once "api/Retargeting_REST_API_Client.php";

// use your REST API KEY from Retargeting Admin Panel
$client = new Retargeting_REST_API_Client("REST_API_KEY");

// set response format to serialize
$client->setResponseFormat("serial");

// set to not unserialize the string
$client->setDecoding(false);

// send order save request
$response = $client->order->save(
    array(
        "order_no" => "235",
        "lastname" => "Doe",
        "firstname" => "John",
        "email" => "johndoe@mail.com",
        "phone" => "0722444444",
        "state" => "United Kingdom",
        "city" => "London",
        "address" => "Tottenham Street, no. 2",
        "discount_code" => ["EEE30PR"],
        "discount" => 50,
        "shipping" => 10,
        "rebates" => 0,
        "fees" => 0,
        "total" => 3800
    ),
    array(
        array('id' => 307, 'quantity' => 5, 'price' => 500, 'variation_code' => ""),
        array('id' => 105, 'quantity' => 1, 'price' => 150, 'variation_code' => "42-B"),
        array('id' => 105, 'quantity' => 2, 'price' => 150, 'variation_code' => "42-W"),
        array('id' => 48, 'quantity' => 10, 'price' => 85, 'variation_code' => "M")
    )
);
```

#Response Example

``` javascript
// JSON response example - valid request with order saved

{
    "version": "1.0",
    "status": 200,
    "message": "OK",
    "data": {
        "success": true
    }
}

// JSON response example - valid request with error message

{
    "version": "1.0",
    "status": 200,
    "message": "OK",
    "data": {
        "error": "Order number exists"
    }
}

// JSON response example - invalid request (error)

{
    "version": "1.0",
    "status": "401",
    "message": "Unauthorized",
    "error": "Invalid Authentication Data"
}
```