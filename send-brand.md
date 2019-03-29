# sendBrand Function

This function must be called every time a visitor lands on a producer/brand page. In this case, the brand page is the page where the brand details are listed, or the page that lists the products belonging to that particular brand.

## sendBrand Function Parameters

|    **Parameter**    |    **Type**    |    **Required**    |    **Description**    |
|---|---|---|---|
|  id  |  Number or text  |  Required  |  The brand item identifier.  |
|	name	|	Text	|	Required	|	The brand name	|

## Examples

### function call with all parameters and callback function set

```js
var _ra = _ra || {};

_ra.sendBrandInfo = {
    "id": 50,
    "name": "Lee Cooper"
};

if (_ra.ready !== undefined) {
    _ra.sendBrand(_ra.sendBrandInfo);
}
```

