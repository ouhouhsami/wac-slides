---
layout: slide
title:
---

<section markdown="1" class="contrast">
<h2 class="contrast">The components</h2>

<img src="/assets/img/layers.png" class="fullscreen-img" >

_...so far..._

</section>

<section markdown="1">
### Segment

<div class="wac-demo reset" id="wac-simple-segment"></div>
<script src="/assets/js/wac-simple-segment.js" type="text/javascript"></script>

{% highlight js %}
var data = [
  { start: 100, duration: 400, color: '#de456f' },
  // ...
];

// 1. create the timeline
var graph = timeline()
  .width(900)
  .height(140)
  .xDomain([0, 1000]);

// 2. create the layer
var segmentLayer = segment()
  .params({
    interactions: { editable: true },
    opacity: 0.6,
    handlerOpacity: 0.8
  })
  .data(data);

// 3. add the layer to the timeline
graph.add(segmentLayer);
// 4. draw the graph
d3.select('#timeline').call(graph.draw);

{% endhighlight %}
</section>


<section markdown="1">
### Waveform

<div class="wac-demo reset" id="wac-simple-waveform"></div>
<script src="/assets/js/wac-simple-waveform.js" type="text/javascript"></script>

{% highlight js %}
// 1. create the timeline
var graph = timeline()
  .width(w)
  .height(h)
  .xDomain([0, buffer.duration]);

// 2. create the waveform layer
var waveformLayer = waveform()
  .data(buffer.getChannelData(0).buffer)
  .sampleRate(buffer.sampleRate)
  .duration(buffer.duration);

// 3. add the layer to the graph
graph.add(waveformLayer);
// 4. draw the graph
d3.select('#timeline').call(graph.draw);
{% endhighlight %}
</section>


<section markdown="1">
### Marker

<div class="wac-demo reset" id="wac-simple-marker"></div>
<script src="/assets/js/wac-simple-marker.js" type="text/javascript"></script>

{% highlight js %}
var data = [
  { x: 100 },
  // ...
];

// 1. create the timeline
var graph = timeline() // config skipped

// 2.1 create the editable markers layer
var markerLayer = marker()
  .params({ interactions: { editable: true } })
  .data(data)

// 2.2 create the cursor layer
var cursorLayer = marker()
  .params({ displayHandle: false })

// 3. add the layers to the timeline
graph.add(markerLayer);
graph.add(cursorLayer);
// 4. draw the graph
d3.select('#timeline').call(graph.draw);
{% endhighlight %}
</section>


<section markdown="1">
### Breakpoint

<div class="wac-demo reset" id="wac-simple-breakpoint"></div>
<script src="/assets/js/wac-simple-breakpoint.js" type="text/javascript"></script>

{% highlight js %}
var data = [
  { cx: 100, cy: 0.5, r: 5 },
  // ...
];

// 1. create the timeline
var graph = timeline() // config skipped

// 2. create the layer
var breakpointLayer = breakpoint()
  .data(data)
  .color('steelblue');

// 3. add the layer to the timeline
graph.add(breakpointLayer);
// 4. draw the graph
d3.select('#timeline').call(graph.draw);
{% endhighlight %}
</section>


<section markdown="1">
### Label

<div class="wac-demo reset" id="wac-simple-label"></div>
<script src="/assets/js/wac-simple-label.js" type="text/javascript"></script>

{% highlight js %}
var data = [
  { x: 100, width: 100, text:'my label', align: 'center' },
  // ...
];

// 1. create the timeline
var graph = timeline() // config skipped

// 2. create the layer
var labelLayer = label()
  .data(data)
  .bgColor('transparent');

// 3. add the layer to the timeline
graph.add(labelLayer);
// 4. draw the graph
d3.select('#timeline').call(graph.draw);
{% endhighlight %}
</section>


<aside class="notes" markdown="1">


* Segment
* Waveform
* Marker
* Breakpoint
* Label

</aside>
