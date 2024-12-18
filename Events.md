- Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
	- React events are named using camelCase, rather than lowercase.
	- With JSX you pass a function as the event handler, rather than a string.
For HTML:
```HTML
<button onclick="activateLasers()">
  Activate Lasers
</button>
```

JSX:
```js
<button onClick={activateLasers}>
  Activate Lasers
</button>
```
- Note that in JSX we can use all events from Java Script just have to name it in camelCase, ex. onClick, onDblClick, onChange etc…
- To pass argument with the events we can use arrow function syntax, for example:
```JS
<button onClick={()=>activateLasers(parameters)}>
  Activate Lasers
</button>
```

#