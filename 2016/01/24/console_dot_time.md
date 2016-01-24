# console.time()

Until yesterday when I wanted to measure how much time a JavaScript function
spent in the browser, I would define a variable:

```js
var startTime = (new Date).getTime();
```

at the beginning of the function, and then something like:

```js
console.log('the function took', (new Date).getTime() - startTime, 'ms');
```

at the end.

Yesterday I used an easier way to do the same thing. I started with:

```js
console.time('myTimer');
```

And ended with:

```js
console.timeEnd('myTimer');
```

I used that in Firefox, and the
[MDN page](https://developer.mozilla.org/en-US/docs/Web/API/Console/time) warns
that it is non-standard. I saw it work in Chrome, and the MDN page says it is
supported in IE11.

Also I saw a [retweet](https://twitter.com/consolelog/status/689594121523109888)
by [Mathias Bynens](https://twitter.com/mathias) this week saying the console
was getting a standard and those methods are mentioned in the
[current document](https://console.spec.whatwg.org/#timing).
