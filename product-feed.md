# Product Feed

In order for Retargeting to display only products available in stock you need to create a CSV feed that returns some informations about products.

## Requirements

This feed must be accesible on your website (eg. https://www.mywebsite.com/feed.csv)

## Recommendations

If possible update this feed every 2h-4h or even create it realtime when retargeting will access the link.

## CSV Header

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category
```


## Example

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category
337,"Aviator Sunglasses",https://demo.store/aviator-sunglasses.html,https://127.0.0.1:8881/media/catalog/product/a/c/ace000a_1.jpg,7,295.00,295.00,,Eyewear
338,"Jackie O Round Sunglasses",https://demo.store/jackie-o-round-sunglasses.html,https://demo.store/media/catalog/product/a/c/ace001_1.jpg,19,295.00,295.00,,Eyewear
339,"Retro Chic Eyeglasses",https://demo.store/retro-chic-eyeglasses.html,https://demo.store/media/catalog/product/a/c/ace002a_1.jpg,25,295.00,295.00,,Eyewear
370,"Isla Crossbody Handbag",https://demo.store/isla-crossbody-handbag.html,https://demo.store/media/catalog/product/a/b/abl000_4.jpg,13,290.00,290.00,,"Bags & Luggage"
371,"Florentine Satchel Handbag",https://demo.store/florentine-satchel-handbag.html,https://demo.store/media/catalog/product/a/b/abl001_1.jpg,-35,625.00,625.00,,"Bags & Luggage"
372,"Flatiron Tablet Sleeve",https://demo.store/leather-tablet-sleeve.html,https://demo.store/media/catalog/product/a/b/abl002b_1.jpg,23,150.00,150.00,,"Bags & Luggage"
373,"Broad St. Flapover Briefcase",https://demo.store/flapover-briefcase.html,https://demo.store/media/catalog/product/a/b/abl003b_1.jpg,24,570.00,570.00,,VIP
374,"Houston Travel Wallet",https://demo.store/rolls-travel-wallet.html,https://demo.store/media/catalog/product/a/b/abl004a_1.jpg,18,210.00,210.00,,VIP
375,"Roller Suitcase",https://demo.store/roller-suitcase.html,https://demo.store/media/catalog/product/a/b/abl005a_1.jpg,15,650.00,650.00,,"Bags & Luggage"
378,"Body Wash with Lemon Flower Extract and Aloe Vera",https://demo.store/body-wash-with-lemon-flower-extract-and-aloe-vera.html,https://demo.store/media/catalog/product/h/d/hdb000_1.jpg,13,28.00,28.00,,"Bed & Bath"
```
