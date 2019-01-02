---
layout:     post
title:      async/await in JavaScript 
date:       2019-01-02
summary:    time to say goodbye to promise hell
categories: javascript
---

introduced in ES6, async/await is a form to work with promises in a more comfortable way.

## async functions

the keyword __async__ before a function declaration defines an asynchronous function, using an implicit promise to return its result.

so, creating an asynchronous function:

{% highlight js %}
async function foo() {
  return 'bar';
}
{% endhighlight %}

and displaying the result from the resolved promise:

{% highlight js %}
foo().then(result => console.log(result)); // 'bar'
{% endhighlight %}

## await

working only inside async functions, the keyword __await__ is used to pause the code execution and wait for a promise be resolved - that is fulfilled or rejected.

thus, we can handle promise results in a simple and synchronous way.

{% highlight js %}
// generic asynchronous function which returns a promise
function asyncOperation() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('bar');
    }, 1000);
  });
}

// async works with arrow function too
const foo = async () => {
  const result = await asyncOperation();

  console.log(result); // 'bar'
}
{% endhighlight %}

cool, right?

## error handling

if the promise is resolved with a fulfilled state, it means that the promise returns its resolved value. But if the promise is rejected, it throws an error.

so, we can catch the error using the try...catch statement:

{% highlight js %}
const getUser = async userName => {
  try {
    const user = await fetch(`/user/${userName}`);
    console.log('user:', user);
  } catch (err) {
    console.log('error getting user data', err);
  }
}
{% endhighlight %}

## summary

  * keyword __async__ ensures that a function will return a promise
  * keyword __await__ works only inside an async function and pause the code execution until a certain promise is resolved
  * try..catch statement is used for error handling


---
thanks and see you!