# jQuery.pixLayout
pixLayout — is a jQuery plugin for per-pixel layout

## About pixLayout

While websites layouting an exact resemblance with model is required. Sometimes this is required by customer, sometimes by superior, and sometimes you want strictly fit the design, but moreover, sometimes per-pixel equivalence is a necessary thing. 

pixLayout was created to facilitate maximally the work of the pixel layout designer and measuring distances and margins.

pixLayout is a picture-layer, which can be managed by the panel at the top right corner of the document window, hotkeys, or just by moving it with the mouse. At any time, the panel can be hidden or completely liquidate the whole html and css of the plugin.

For dynamic layout adjusting is very convenient to use the Developer Tools in Chrome or FireBug in Firefox.

## Pixlayout advantages over other similar plug-ins and add-ons

1. *Not only works in one browser.* As pixLayout is a javascript-code it's enough to include it to head and it will work in all supported browsers. After the end of layout you can merely disconnect the plugin.
2. *Functionality.* Plugin provides all necessary functions and settings for convenient picture-layer control.
3. *Crossbrowsering  and crossversioning.* pixLayout works in browsers chrome5+, opera 11+, firefox 3,6+, IE 7+, as well as on all versions of jQuery beginning from the 1.3.2.
4. *All in one file.* In contrast to many plugins, which include besides js-code, and even style files, and frequently  pictures, pixLayout consists of a single file in which all the components are already embedded.
5. *Free of charge and permanent project development.* Plugin is spreaded absolutely free under license GPL 2 and constantly evolves. 

## How to start?
```html
<script src="path_to_jquery/jquery.js"></script>
<script src="jquery.pixlayout.js"></script>
<script>
  $(function(){
    $.pixlayout("path_to_picture/picture.ext");
  });
</script>
```

## Some parameters transmission and context example
```javascript
$(function(){
  $.pixlayout({
    src: "/img/layout.jpg",
    opacity: 0.8,
    top: 50,
    center: true,
    clip: true,
    show: true
  }, ".wrapper");
});
```

## Parameters
| Parameter | Type | Possible values | Description |
|----|----|----|----|
| src | string | way to the picture-layer | way to the picture-layer |
| opacity | float | 0.0 - 1.0 | opacity |
| step | integer | from 1 to infinity | step moving image in pixels |
| top, left, right | integer | from 1 to infinity | indention in pixels |
| zindex | integer | from 1 to infinity | picture-layer location on the axis z |
| clip | boolean | true / false | panel fixed or not |
| center | boolean | true / false | picture in the center or not |
| fixed | boolean | true / false | picture in the center or not |
| show | boolean | true / false | show the picture when loading or not |

## Context
You can specify any element on the page as the context and the picture-layer will add to the end of this element. By default, such an element is body. 

Context is specified as the second parameter.

*Example:*
`$.pixlayout("img/picture.png", "div.wrapper");`

## Displacement
* buttons: 'left', 'right', 'up', 'down'
* buttons: w,a,s,d, when the picture is visible
* navigation buttons

## Operations
* Destroy (remove all html and css code pixLayout from the page) - the `x` in the upper right corner
* Secure the panel - the icon in the upper right corner of the panel
* Quick reference: the question mark in the upper right corner of the panel
* To roll up settings - arrow 'up' downwards of the panel
* Show/hide the picture - the center button of the navigation bar or `shift+e`
