---
layout:     post
title:      filter objects in JavaScript
date:       2019-01-15
summary:    filtering objects like the Array.prototype.filter() method
categories: javascript
---

if you have to filter an object in JS by a possible property or value then this post is for you (actually, is for everyone :joy_cat:).

## why

objects in JavaScript doesn't have a method like Array.prototype.filter(), so a nice solution is to combine Object.keys() and Array.prototype.reduce() to provide a way to filter an object by property(ies) or value(s).

## ok, show me the code

thus, our goal is to filter an object by a property or value. Think of it as removing an evil pair of key-value or, in React context, avoiding to mutate a component's state (which is [recommended](https://reactjs.org/docs/react-component.html#setstate) by the React docs).

we can use the Object.keys() to get an array with the object's keys:

{% highlight js %}
const obj = {
  foo: 'bar',
  the: 'game' 
};

Object.keys(obj); // ['foo', 'the']
{% endhighlight %}

then we can iterate over that array of strings (object's keys) with the Array.prototype.reduce() method to apply an exclusion criteria and return the filtered object.

Array.prototype.reduce() syntax is described below - unused params were omitted.

{% highlight js %}
/**
  - acc: accumulated value
  - curr: current element being iterated
  - initial: initial value to acc arg
*/
array.reduce((acc, curr) => {
  // criteria
}, initial);
{% endhighlight %}

so, we can filter an object by a value:

{% highlight js %}
const obj = {
  foo: 'bar',
  the: 'game' 
};

// removing the key with the 'bar' value
const filtered = Object.keys(obj).reduce((acc, curr) => {
  // curr is an object's key
  if (obj[curr] !== 'bar')
    acc[curr] = obj[curr];

  // forwards to the next iteration
  return acc;
}, {} );

console.log(filtered); // {the: "game"}
{% endhighlight %}

or by index:

{% highlight js %}
// removing the key 'foo'
const filtered = Object.keys(obj).reduce((acc, curr) => {

  if (curr !== 'foo')
    acc[curr] = obj[curr];

  return acc;
}, {} );

console.log(filtered); // {the: "game"}
{% endhighlight %}

that's it.

---

Useful links:
* [Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

* [Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

---

goodbye!