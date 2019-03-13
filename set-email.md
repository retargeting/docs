# setEmail Function

This function needs to be called each time a guest registers, logs in or fills in the email address in a form on the website (e.g. Contact or Newsletter Form).

## setEmail Function Parameters

| name | type | required | detail |
|---|---|---|---|
| email | text | true | Visitor email address. Ex. john.doe@example.com |
| name | text | false | Visitor name. Ex. John Doe |
| phone | text | false | Visitor phone number. |
| city | text | false | Visitor city. |
| sex | numeric | false | This parameter is numeric and has two possible values: 0 = woman and 1 = man |
| birthday | text | false | Visitor birthday in format DD-MM-YYYY |
| callback_function | function | false | with this parameter you can define a function that will be executed after setEmail's behaviour is finished. |

---

## Examples

### function call with all parameters and callback function set

```js
_ra.setEmail({
    "email": "johndoe@example.com",
    "name": "John Doe",
    "phone": "0777222000",
    "city": "London",
    "sex": 1,
    "birthday": "29-08-1989"
}, function() {
    console.log("setEmail information have been sent");
});
```

---

### function call with only the required parameter

```js
// function call with only the required parameter

_ra.setEmail({
    "email": "johndoe@example.com"
});
```

