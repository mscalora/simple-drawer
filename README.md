# Simple Drawer
[![Build status][travis-badge]][travis-url] [![Bower dependencies][bowerdeps-badge]][bowerdeps-url] ![Version][bower-badge] ![Size][size-badge]

Simple off-screen drawer panel

## Installation & usage

Install simple-drawer with Bower

```sh
$ bower install simple-drawer --save
```

Import it into the `<head>` of your document

```html
<link rel="import" href="/bower_components/simple-drawer/simple-drawer.html">
```

Then use it in on your page, and toggle the `active` property to open/close it.

```html
<simple-drawer id="drawer"></simple-drawer>

<script>
  // Open drawer
  document.querySelector('#drawer').active = true;
</script>
```


### Polyfills for cross-browser support
Simple drawer relies on emerging standards, for full cross-browser support include the [Web Components Lite][webcomponents] polyfill.

```sh
bower i webcomponentsjs --save
```

```html
<script src="/bower_components/webcomponentsjs/web-components-lite.js"></script>
```

## Properties

Property         | Type    | Default   | Description                                                   
---------------- | ------- | --------- | -------------                                                  
`active`         | Boolean | `false`   | Whether the drawer is opened or closed
`position`       | String  | `'left'`  | Position of the drawer, can be left or right side of viewport 
`disabled`       | Boolean | `false`   | Whether drawer is disabled                                    
`noEscape`       | Boolean | `false`   | Stop drawer exiting on escape key press                                 
`noBlur` | Boolean | `false`   | Stop the drawer closing if it loses focus

Properties can either be set as attributes on the element, or imperitively with Javascript

```html
<simple-drawer position="left" no-escape></simple-drawer>

<script>
  document.querySelector('simple-drawer').position = 'left';
</script>                        
```

--

MIT © [Simpla](https://www.simpla.io) 

[webcomponents]: https://github.com/webcomponents/webcomponentsjs

[bower-badge]: https://img.shields.io/bower/v/simple-drawer.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-drawer.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-drawer.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-drawer
[bowerdeps-badge]: https://img.shields.io/gemnasium/SimpleElements/simple-drawer.svg
[bowerdeps-url]: https://gemnasium.com/bower/simple-drawer
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-drawer/master/simple-drawer.html?gzip=true&color=blue

