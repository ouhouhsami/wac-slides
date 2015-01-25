---
layout: slide
title: 
---

### Data uniformity issues

* Data structure/format
* Editing shared data

### Small helper/solution

{% highlight js %}
var data = [
  { x: 100, duration: 400 },
  // ...
];

// 1. create the timeline
// ...

// 2. create the layer
var segmentLayer = segment()
  .params(/*some params*/)
  .data(data)
  // start accessor
  .start((d, v = null) => { 
    if (v === null) { return d.x; }
    d.x = v;
  });

// 3. add the layer to the timeline
// 4. draw the graph
{% endhighlight %}