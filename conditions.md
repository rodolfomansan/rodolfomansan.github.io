## waitForElement

Waits for an element to be available on the page and then runs a callback function.

Parameter | Description
--- | ---
`element` | Element selector being waited for
`callback` | Code to be executed when the element is available

```javascript
t1234.waitForElement('#sideBar', function () {
	//logic
});
```