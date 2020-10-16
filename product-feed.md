# Product Feed

In order for Retargeting to display only products available in stock you need to create a CSV feed that returns some informations about products.

## Requirements

This feed must be accesible on your website (eg. https://www.mywebsite.com/feed.csv)

## Recommendations

If possible update this feed every 2h-4h or even create it realtime when retargeting will access the link.

## CSV Header

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category,"extra data"
```

|Field|Required|Description|
|---	|---	|---	|
|product id| YES | The product id. Should be the same id used for sendProduct and saveOrder functions.|
|product name| YES | The product name.|
|product url| YES |The full product url. Ex. https://mywebsite.com/my-product.|
|image url| YES | The full image url for base image. Ex. https://mywebsite.com/media/my-product-image.jpg|
|stock| YES|The product stock quantity. If you don't have the stock quantity, you can use 1 or 0.|
|price| YES |The full product price with 2 decimals. Ex. 75.34.|
|sale price| YES |The sale price with 2 decimals. Ex. 32.29. If product has no sale price, use the full price.|
|brand| NO | Product Manufacturer.|
|category| YES |Product main category|
|extra data|YES| Aditional data in JSON format.|

### Extra data field

The following product details should be included in the extra data field.

|Field|Description|
|---	|---	|
|margin| The product margin. If you don't want to add this information, send as null |
|media_gallery| An array with all product images.|
|categories| The full path category tree. Each category should be separated with \| |
|variations| If product has variations like colour, size, all product variations goes here as an array of objects. Each variation object must have the following keys: `id`, `price`, `sale price`, `stock`, `margin`.|
|in_supplier_stock| Set `true` or `false` if product is in supplier stock. For products with variations you need to specify the `in_supplier_stock` parameter for each variation. |


### Extra data field example

Here's a valid example of `extra data` field.

```json
{
    "categories": "Men | Shirts",
    "media gallery": [
        "https://demo.store/media/catalog/product/m/s/msj006t.jpg",
        "https://demo.store/media/catalog/product/m/s/msj006a.jpg",
        "https://demo.store/media/catalog/product/m/s/msj006b_2.jpg",
        "https://demo.store/media/catalog/product/s/w/swatch_msj006c-khaki.png",
        "https://demo.store/media/catalog/product/s/w/swatch_msj006c-royal-blue.png",
        "https://demo.store/media/catalog/product/s/w/swatch_msj006c-charcoal.png",
        "https://demo.store/media/catalog/product/s/w/swatch_msj006c-red.png"
    ],
    "variations": [
        {
            "id": "White-S",
            "price": "190.00",
            "sale price": "190.00",
            "stock": 0,
            "margin": null,
            "in_supplier_stock": true
        },
        {
            "id": "White-M",
            "price": "190.00",
            "sale price": "190.00",
            "stock": 25,
            "margin": null,
            "in_supplier_stock": true
        },
        {
            "id": "White-L",
            "price": "190.00",
            "sale price": "190.00",
            "stock": 24,
            "margin": null,
            "in_supplier_stock": false
        },
        // ...
    ],
    "margin": null
}
```

## CSV Format Specifications

* Delimiter: , 
* Enclosure: "

## Example

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category,extra data
337,"Aviator Sunglasses,https://demo.store/aviator-sunglasses.html,https://demo.store/media/catalog/product/a/c/ace000a_1.jpg,7,295.00,295.00,,Eyewear,"{""categories"":""Eyewear"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg""],""variations"":[],""in_supplier_stock"": true,""margin"":null}"
338,"Jackie O Round Sunglasses",https://demo.store/jackie-o-round-sunglasses.html,https://demo.store/media/catalog/product/a/c/ace001_1.jpg,19,295.00,295.00,,Eyewear,"{""categories"":""Eyewear"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg""],""variations"":[],""in_supplier_stock"": false,""margin"":null}"
339,"Retro Chic Eyeglasses",https://demo.store/retro-chic-eyeglasses.html,https://demo.store/media/catalog/product/a/c/ace002a_1.jpg,25,295.00,295.00,,Eyewear,"{""categories"":""Eyewear"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg""],""variations"":[],""in_supplier_stock"": true,""margin"":null}"
370,"Isla Crossbody Handbag",https://demo.store/isla-crossbody-handbag.html,https://demo.store/media/catalog/product/a/b/abl000_4.jpg,13,290.00,290.00,,Bags & Luggage,"{""categories"":""Bags & Luggage"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg""],""variations"":[],""in_supplier_stock"": true,""margin"":null}"
371,"Florentine Satchel Handbag",https://demo.store/florentine-satchel-handbag.html,https://demo.store/media/catalog/product/a/b/abl001_1.jpg,0,625.00,625.00,,Bags & Luggage,"{""categories"":""Bags & Luggage"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg""],""variations"":[],""in_supplier_stock"": true,""margin"":null}"
372,"Flatiron Tablet Sleeve",https://demo.store/leather-tablet-sleeve.html,https://demo.store/media/catalog/product/a/b/abl002b_1.jpg,23,150.00,150.00,,Bags & Luggage,"{""categories"":""Bags & Luggage"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002a_1.jpg""],""variations"":[],""in_supplier_stock"": false,""margin"":null}"
373,"Broad St. Flapover Briefcase",https://demo.store/flapover-briefcase.html,https://demo.store/media/catalog/product/a/b/abl003b_1.jpg,24,570.00,400.00,,VIP,"{""categories"":""VIP"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003b_1.jpg""],""variations"":[],""in_supplier_stock"": false,""margin"":null}"
374,"Houston Travel Wallet",https://demo.store/rolls-travel-wallet.html,https://demo.store/media/catalog/product/a/b/abl004a_1.jpg,18,210.00,150.00,,VIP,"{""categories"":""VIP"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004b_1.jpg""],""variations"":[],""in_supplier_stock"": false,""margin"":null}"
375,"Roller Suitcase",https://demo.store/roller-suitcase.html,https://demo.store/media/catalog/product/a/b/abl005a_1.jpg,15,650.00,650.00,,Bags & Luggage,"{""categories"":""Bags & Luggage"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl005a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl005b_1.jpg""],""variations"":[],""in_supplier_stock"": false,""margin"":null}"
378,"Body Wash with Lemon Flower Extract and Aloe Vera",https://demo.store/body-wash-with-lemon-flower-extract-and-aloe-vera.html,https://demo.store/media/catalog/product/h/d/hdb000_1.jpg,13,28.00,26.04,,Bed & Bath,"{""categories"":""Bed & Bath"",""media gallery"":[""https://demo.store/media/catalog/product/a/c/ace000a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace000b_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002a_1.jpg"",""https://demo.store/media/catalog/product/a/c/ace002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl002a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl003b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl004b_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl005a_1.jpg"",""https://demo.store/media/catalog/product/a/b/abl005b_1.jpg""],""variations"":[],""in_supplier_stock"": true,""margin"":null}"
```
