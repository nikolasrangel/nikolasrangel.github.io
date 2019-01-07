---
layout:     post
title:      removing an element and avoiding mutation
date:       2019-01-07
summary:    "JS code snippet: Array.prototype.filter() to avoid mutation"
categories: javascript
---

searching in your code where a specific array is mutated is not a nice thing. so, let's avoid it.

## why

[slemgrim.com](https://slemgrim.com/mutate-or-not-to-mutate) has a good definition:

> changing properties of objects is mutation. Mutation is a side effect by definition. Everyone of us learned that we should avoid side effects at all cost. We don’t have to look into the implementation of a function if it doesn’t have any side effects. Our code gets easier to reason about and will be more predictable and more testable.

## ok, show me the code

using the Array.prototype.filter() we test an array with a specific function so then we can get the element that it is being processed and its index.

the array filter's syntax with the args that will be used in our example:

{% highlight js %}
const arr = array.filter(function(element, index));
{% endhighlight %}

so, removing a target element from an array and avoiding mutation is very simple:

### if you know the target's index

{% highlight js %}
const new = arr.filter((elem, index) => index !== targetIndex);
{% endhighlight %}

### if you know the target's value

{% highlight js %}
const new = arr.filter(elem => elem !== target);
{% endhighlight %}

---

tks and see u