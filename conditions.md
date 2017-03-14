## waitForElement

Waits for an element to be available on the page and then runs a callback function.

Parameter | Type | Description
--- | --- | ---
`element` | *string* | Element selector being waited for
`callback` | *function* | Code to be executed when the element is available

```javascript
t1234.waitForElement('#sideBar', function () {
	//logic
});
```

---

## waitForCondition

Waits for a condition to be met and then runs a callback function.

Parameter | Type | Description
--- | --- | ---
`condition` | *string* | Condition being waited to be met
`callback` | *function* | Code to be executed when the condition is met

```javascript
t1234.waitForCondition('flag=true', function () {
	//logic
});
```