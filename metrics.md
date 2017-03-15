## clickTrack

Triggers a clickTrack. There are multiple ways to do that (see below).

Parameter | Type | Description
--- | --- | ---
`element` | *string* | *(Optional)* Element that triggers the clicktrack. If passed, it will bind to the element automatically.
`clicked` | *string* | Name of the triggered metric.
`callback` | *string or function* | Function to be executed after the clickTrack is registered.

If an element is passed as the first argument, *tntLib* automatically fills `t1234.clickedElement` with its *jQuery object* whenever a click is triggered, allowing the usage of the parameter inside the callbacks.

```javascript
t1234.clickTrack('1234_test');
```

```javascript
t1234.clickTrack('li.tileStack', '1234_test2');
```

```javascript
t1234.clickTrack('1234_test3', 't1234.callback');
```

```javascript
t1234.clickTrack('1234_test4', t1234.callback);
```

```javascript
t1234.clickTrack('1234_test5', function () {
    console.info('dynamic callback');
});
```

```javascript
t1234.clickTrack('li.tileStack', '1234_test6', function () {
    console.info(t1234.clickedElement); // returns the clicked $('li.tileStack') object
});
```

---

## addRef

Adds a ref value to an url. There are multiple ways to do that (see below).

Parameter | Type | Description
--- | --- | ---
`condition` | *string* | Condition being waited to be met
`callback` | *function* | Code to be executed when the condition is met

```javascript
t1234.addRef('.mhLogo', '66666_ref1');
```

```javascript
t1234.addRef('.catTitle img', 'src', '66666_ref2');
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
t66666.directInject('12312');
```