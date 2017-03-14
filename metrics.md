## clickTrack

Triggers a clickTrack. There are multiple ways to pass that (see below).

Parameter | Type | Description
--- | --- | ---
`element` | *string* | *(Optional)* Element that triggers the clicktrack. If passed, it will bind to the element automatically.
`clicked` | *string* | Name of the triggered metric.
`callback` | *string | function* | Function to be executed after the clickTrack is registered.

```javascript
t1234.clickTrack('1234_test');
```

```javascript
t1234.clickTrack(null, '1234_test2');
```

```javascript
t1234.clickTrack('li.tileStack', '1234_test3');
```

```javascript
t1234.clickTrack(null, '1234_test4', 't1234.callback');
```

```javascript
t1234.clickTrack(null, '1234_test5', t1234.callback);
```

```javascript
t1234.clickTrack(null, '1234_test6', function () {
    console.info('dynamic callback');
});
```

```javascript
t1234.clickTrack('1234_test7', function () {
    console.info('dynamic callback');
});
```

---

## addRef

Adds a ref value to an url.

Parameter | Type | Description
--- | --- | ---
`condition` | *string* | Condition being waited to be met
`callback` | *function* | Code to be executed when the condition is met

```javascript
t1234.waitForCondition('flag=true', function () {
	//logic
});
```

---

## directInject

Triggers a direct inject with a specified value.
IMPORTANT: Only once per page.

Parameter | Type | Description
--- | --- | ---
`condition` | *string* | Condition being waited to be met
`callback` | *function* | Code to be executed when the condition is met

```javascript
t1234.waitForCondition('flag=true', function () {
	//logic
});
```