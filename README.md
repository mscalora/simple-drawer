# Simple Drawer
[![Build status][travis-badge]][travis-url] [![Bower dependencies][bowerdeps-badge]] [bowerdeps-url]![Version][bower-badge]

Simple, toggleable off-screen drawer panel

## Installation & usage

Install simple-drawer with Bower

```sh
$ bower install simple-drawer --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-drawer/simple-drawer.html">
```

Then use it in your project, and call `open()` on it to show it.

```html
<simple-drawer id="drawer"></simple-drawer>

<script>
  // Open drawer
  document.querySelector('#drawer').open();
</script>
```

Note for cross-browser support you should also include the [Web Components Polyfill][webcomponents].

## Options

Property         | Type    | Default   | Description                                                   
---------------- | ------- | --------- | -------------                                                  
`position`       | String  | `'left'`  | Position of the drawer, can be left or right side of viewport 
`disabled`       | Boolean | `false`   | Whether drawer is disabled                                    
`noEscape`       | Boolean | `false`   | Stop drawer exiting on escape                                 
`noOutsideClick` | Boolean | `false`   | Stop drawer exiting on outside click                          

## Methods

Method     | Description       
---------- | -----------       
`open()`   | Open the drawer   
`close()`  | Close the drawer  
`toggle()` | Toggle the drawer 

--

MIT © [Simpla](https://www.simpla.io) 

[webcomponents]: https://github.com/webcomponents/webcomponentsjs

[bower-badge]: https://img.shields.io/bower/v/simple-drawer.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-drawer.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-drawer.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-drawer
[bowerdeps-badge]: https://img.shields.io/gemnasium/SimpleElements/simple-drawer.svg
[bowerdeps-url]: https://gemnasium.com/bower/simple-drawer
