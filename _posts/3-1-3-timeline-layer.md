---
layout: slide
title: 
---

<section markdown="1">
# Timeline

* ensures time axis consitency
* centralises events
  * event delegation
  * event broadcasting
  * compnents consuming
* orchestrates layers
	* vertical layout
  * zooming
  * time-scale

<aside class="notes" markdown="1">
</aside>

</section>

<section markdown="1">
# Layer

* centralises all common layer logic
  * initialisation
  * scales
  * events
  * selecting
  * editing
  * zoom
* components inherits from it and overrides when needed
* components implement their own drag/edit/upate/draw strategies

<aside class="notes" markdown="1">
</aside>

</section>