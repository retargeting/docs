# Product Feed

In order for Retargeting to display only products available in stock you need to create a JSON feed that returns some informations about products.

```json
{
    "id": "231",
    "name": "French Cuff Cotton Twill Oxford",
    "url": "https://demo.store/men/shirts/french-cuff-cotton-twill-oxford",
    "image": "https://demo.store/media/catalog/product",
    "price": 190,
    "promo": 0,
    "brand": null,
    "category": [
	{
	    "id": "15",
	    "name": "Shirts",
	    "parent": 5,
	    "url": "https://demo.store/men/shirts.html",
	    "breadcrumb": [
		{
		    "id": "5",
		    "name": "Men",
		    "parent": false,
		    "url": "https://demo.store/men.html"
		}
	    ]
	}
    ],
    "inventory": {
	"variations": false,
	"stock": true
    }
}
```


## Example

*In order to make the file smaller it is not necessary to send products with no stock*  

```json
{
    "data": [
        {
            "id": "231",
            "name": "French Cuff Cotton Twill Oxford",
            "url": "https://demo.store/men/shirts/french-cuff-cotton-twill-oxford",
            "image": "https://demo.store/media/catalog/product",
            "price": 190,
            "promo": 0,
            "brand": null,
            "category": [
                {
                    "id": "15",
                    "name": "Shirts",
                    "parent": 5,
                    "url": "https://demo.store/men/shirts.html",
                    "breadcrumb": [
                        {
                            "id": "5",
                            "name": "Men",
                            "parent": false,
                            "url": "https://demo.store/men.html"
                        }
                    ]
                }
            ],
            "inventory": {
                "variations": false,
                "stock": true
            }
        },
        {
            "id": "232",
            "name": "French Cuff Cotton Twill Oxford",
            "url": "https://demo.store/men/shirts/french-cuff-cotton-twill-oxford",
            "image": "https://demo.store/media/catalog/product",
            "price": 190,
            "promo": 0,
            "brand": null,
            "category": [
                {
                    "id": "15",
                    "name": "Shirts",
                    "parent": 5,
                    "url": "https://demo.store/men/shirts.html",
                    "breadcrumb": [
                        {
                            "id": "5",
                            "name": "Men",
                            "parent": false,
                            "url": "https://demo.store/men.html"
                        }
                    ]
                }
            ],
            "inventory": {
                "variations": false,
                "stock": true
            }
        },
        {
            "id": "233",
            "name": "French Cuff Cotton Twill Oxford",
            "url": "https://demo.store/men/shirts/french-cuff-cotton-twill-oxford",
            "image": "https://demo.store/media/catalog/product",
            "price": 190,
            "promo": 0,
            "brand": null,
            "category": [
                {
                    "id": "15",
                    "name": "Shirts",
                    "parent": 5,
                    "url": "https://demo.store/men/shirts.html",
                    "breadcrumb": [
                        {
                            "id": "5",
                            "name": "Men",
                            "parent": false,
                            "url": "https://demo.store/men.html"
                        }
                    ]
                }
            ],
            "inventory": {
                "variations": false,
                "stock": false
            }
        },
        {
            "id": "234",
            "name": "Slim fit Dobby Oxford Shirt",
            "url": "https://demo.store/men/shirts/slim-fit-dobby-oxford-shirt",
            "image": "https://demo.store/media/catalog/product",
            "price": 175,
            "promo": 0,
            "brand": null,
            "category": [
                {
                    "id": "15",
                    "name": "Shirts",
                    "parent": 5,
                    "url": "https://demo.store/men/shirts.html",
                    "breadcrumb": [
                        {
                            "id": "5",
                            "name": "Men",
                            "parent": false,
                            "url": "https://demo.store/men.html"
                        }
                    ]
                }
            ],
            "inventory": {
                "variations": false,
                "stock": true
            }
        },
        {
            "id": "235",
            "name": "Slim fit Dobby Oxford Shirt",
            "url": "https://demo.store/men/shirts/slim-fit-dobby-oxford-shirt",
            "image": "https://demo.store/media/catalog/product",
            "price": 175,
            "promo": 0,
            "brand": null,
            "category": [
                {
                    "id": "15",
                    "name": "Shirts",
                    "parent": 5,
                    "url": "https://demo.store/men/shirts.html",
                    "breadcrumb": [
                        {
                            "id": "5",
                            "name": "Men",
                            "parent": false,
                            "url": "https://demo.store/men.html"
                        }
                    ]
                }
            ],
            "inventory": {
                "variations": false,
                "stock": false
            }
        }
    ],
    "current_page": 1,
    "last_page": 119,
    "next_page": "https://demo.store/retargeting/products?page=2",
    "prev_page": "https://demo.store/retargeting/products?page=1"
}

```
