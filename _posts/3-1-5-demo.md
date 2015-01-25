---
layout: slide
title:
---

<link rel="stylesheet" type="text/css" href="/assets/css/wac-interactions-demo.css">

<div class="reset" id="wac-interactions-demo">
  <div class="avatar"></div>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco <a href="#" id="wac-interactions-add-segment">add segment</a> laboris nisi ut aliquip ex ea commodo
    consequat. Duis dolor in reprehenderit in voluptate velit esse
    cillum dolore eu
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse <a href="#" id="wac-interactions-remove-selected">remove selected</a>
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>
  <div class="timeline" id="wac-interactions-segments"></div>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>
  <div class="timeline" id="wac-interactions-breakpoints"></div>
  <div class="bottom">
    <div class="left"></div>
    <div class="right">
      <label>opacity<br />
        <input type="range" id="switch-opacity" min="0" max="1" default="0.5" step="0.01" />
      </label>
      <label>start<br />
        <input type="range" id="switch-start" min="0" max="100" default="50" step="1" />
      </label>
    </div>
  </div>
</div>

<script src="/assets/js/wac-interactions-demo.js"></script>

<aside class="notes" markdown="1">
* DOM interaction
* D3 interaction
* command line "programatic" interaction

snippets
~~~
{
  id: new Date().getTime(),
  start: Math.random() * 70,
  duration: Math.random() * 20 + 5,
  color: 'rgb('+ Math.ceil(Math.random() * 255) +', '+ Math.ceil(Math.random() * 255) +', '+ Math.ceil(Math.random() * 255) +')',
  opacity: Math.random() * 0.8 + 0.2
}
~~~
</aside>

