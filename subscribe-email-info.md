# subcscribeEmailInfo Function

This function needs to be called each time a guest registers, logs in or fills in the email address in a form on the website (e.g. Contact or Newsletter Form, Order Details), to inform Retargeting if user want to receive marketing emails.

If you have a checkbox for opt in/opt out, you can trigger this function when user change the status.

## subcscribeEmailInfo Function Parameters

| name | type | required | detail |
|---|---|---|---|
| email | text | true | Email address. Ex. john.doe@example.com |
| status | bool | true | OptIn/Opt out status in boolean format. Ex. true |

---

## Example

```js
var ra = ra || {};
 
_ra.subscribeEmailInfo = {
    email: 'johndoe@example.com',
    status: true
};
 
if (_ra.ready !== undefined) {
    _ra.subscribeEmail(_ra.subscribeEmailInfo);
}
```
