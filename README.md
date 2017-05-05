# Simple Drawer
[![Build status][travis-badge]][travis-url] ![Version][bower-badge] ![Size][size-badge] [![Published][webcomponents-badge]][webcomponents-url]

Simple-drawer is a performant, lightweight, style-agnostic off-screen drawer panel element

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="simple-drawer.html">
    <style>
      body {
        font-family: sans-serif;
        color: #303c46
      }

      simple-drawer {
        padding: 20px 45px;
        font-family: sans-serif;
      }

      simple-drawer h1 {
        font-size: 24px;
        font-weight: 400;
        border-bottom: 1px solid lightGrey;
        padding-bottom: 10px;
      }

      simple-drawer a {
        display: inline-block;
        text-decoration: none;
        text-align: left;
        margin: 10px 0;
        color: deepskyblue;
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<button id="button">Open drawer</button>

<simple-drawer id="drawer">
  <h1>My Drawer</h1>
  <a href="#">Menu item</a>
</simple-drawer>

<script>
  var button = document.querySelector('#button'),
      drawer = document.querySelector('#drawer');

  button.addEventListener('click', function(e) {
    drawer.active = true;
  });
</script>
```

## Installation & usage

Install simple-drawer with Bower (Yarn support coming soon)

```sh
$ bower install simple-drawer --save
```

Import it into the `<head>` of your document

```html
<link rel="import" href="/bower_components/simple-drawer/simple-drawer.html">
```

Then use it in on your page, and toggle the `active` property to open/close it.

```html
<simple-drawer id="drawer">
  <!-- Drawer contents -->
</simple-drawer>

<script>
  document.querySelector('simple-drawer').active = true;
</script>
```


#### Cross-browser support

Simple drawer relies on emerging standards, for full cross-browser support include the [Web Components Lite][webcomponents] polyfill.

```html
<script src="https://unpkg.com/webcomponents.js@^0.7.24/webcomponents-lite.min.js"></script>
```

## Properties

Property         | Type    | Default   | Description                                                   
---------------- | ------- | --------- | -------------                                                  
`active`         | Boolean | `false`   | Whether the drawer is opened or closed
`position`       | String  | `'left'`  | Position of the drawer, can be left or right side of viewport 
`disabled`       | Boolean | `false`   | Whether drawer is disabled                                    
`noEscape`       | Boolean | `false`   | Stop drawer exiting on escape key press                                 
`noBlur`         | Boolean | `false`   | Stop the drawer closing if it loses focus
`noChildClicks`  | Boolean | `false`   | Stop the drawer closing when children get focus (eg: clicking links)

Properties can be set as attributes on the element or with Javascript, camelCased properties are serialized to kebab-cased attributes

```html
<simple-drawer position="left" no-escape></simple-drawer>

<script>
  document.querySelector('simple-drawer').active = true;
</script>                        
```

***

MIT © [Simpla](https://www.simpla.io) 

[webcomponents]: https://github.com/webcomponents/webcomponentsjs

[bower-badge]: https://img.shields.io/bower/v/simple-drawer.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-drawer.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-drawer.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-drawer
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-drawer/master/simple-drawer.html?gzip=true
[webcomponents-badge]: https://img.shields.io/badge/webcomponents.org-published-blue.svg
[webcomponents-url]: https://www.webcomponents.org/element/SimpleElements/simple-drawer

