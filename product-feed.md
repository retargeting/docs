# Product Feed

In order for Retargeting to display only products available in stock you need to create a JSON feed that returns some informations about products.

```json
{
    "id": "231",
    "name": "French Cuff Cotton Twill Oxford",
    "image": "https://example.com/media/m/s/msj000t_1.jpg",
    "price": 190,
    "promo": 0,
    "inventory": {
        "variations": false,
        "stock": true
    }
}
```


## Feed file examples

*In order to make the file smaller it is not necessary to send products with no stock*  

```json
{
	"data": [{
		"id": "231",
		"name": "French Cuff Cotton Twill Oxford",
		"image": "https://example.com/media/m/s/msj000t_1.jpg",
		"price": 190,
		"promo": 0,
		"inventory": {
			"variations": false,
			"stock": true
		}
	}, {
		"id": "232",
		"name": "French Cuff Cotton Twill Oxford",
		"image": "https://example.com/media/m/s/msj000t_1.jpg",
		"price": 190,
		"promo": 150,
		"inventory": {
			"variations": false,
			"stock": true
		}
	}, {
		"id": "233",
		"name": "French Cuff Cotton Twill Oxford",
		"image": "https://example.com/media/m/s/msj000t_1.jpg",
		"price": 130,
		"promo": 0,
		"inventory": {
			"variations": false,
			"stock": true
		}
	}, {
		"id": "234",
		"name": "Slim fit Dobby Oxford Shirt",
		"image": "https://example.com/media/m/s/msj003t_1.jpg",
		"price": 175,
		"promo": 0,
		"inventory": {
			"variations": false,
			"stock": true
		}
	}, {
		"id": "235",
		"name": "Slim fit Dobby Oxford Shirt",
		"image": "https://example.com/media/m/s/msj003t_1.jpg",
		"price": 195,
		"promo": 0,
		"inventory": {
			"variations": false,
			"stock": true
		}

	}],
	"current_page": 1,
	"last_page": 6,
	"next_page": "https://example.com/retargetingfeed/products?page=6",
	"prev_page": "https://example.com/retargetingfeed/products?page=1"
}
```
