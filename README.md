####Cautionary Tale
Everything you can do in jQuery is written with regular ([sometimes jokingly called "vanilla"](http://vanilla-js.com/))

[jQuery API documentation](http://api.jquery.com/).

### How Can We Include jQuery?
* CDN
* Install
* jQuery JS File
* Chrome Plugin Injection (e.g. Firequery)

### The Selector

Tired of typing out `getElementsByTagName`? Substitute it with `$("")`!

Wow. Think of all of the seconds we get back in life. Of course, jQuery will need to be installed in your environment to get this working!

## First grab the jQuery object
There are a number of ways to "grab" selectors from the DOM, notice the similarity to css:    
  - By id `$("#kale");`
  - By class `$(".top-bar");`
  - By element `$("h1");`

  [Methods for Selection](https://www.w3schools.com/jquery/jquery_ref_selectors.asp)

#### Assigning a jQuery object to a variable
You can assign any element you select with jQuery to a variable and then call jQuery methods on it.

```js
var kale = $('#kale')
kale.hide();
```
#### Pro-tip: Don't mix with Vanilla JS

```js
var vanilla = document.getElementById("kale")
vanilla.hide();
// => Uncaught TypeError: vanilla.hide is not a function(…)
```

### Hiding an element

`$("#white-powder").hide();`

[`hide()` documentation](http://api.jquery.com/hide/)

### Showing an element

`$("#white-powder").show();`

[`show()` documentation](http://api.jquery.com/show/)

### GET FANCY! FADE OUT!

`$("#neil-gaiman").fadeOut();`

[`fadeOut()` documentation](http://api.jquery.com/fadeOut/)

### Changing the styling of element(s)

`$("h1").css("color", "teal");`

[`css()` documentation](http://api.jquery.com/css/)

or maybe:
```
$(".top-bar").addClass("new_class");
```

### Remove an element and then append it somewhere else

```
var wormhole = $('#wormhole').remove();
$('.resources').append(wormhole);
```
Remove is different from hide, remove takes it out of the DOM

[`remove()` documentation](http://api.jquery.com/remove/)

[`append()` documentation](http://api.jquery.com/append/)


## Parents and Children
```
$("#resources").children();
```

```
$("#resources").parent();
```

[Methods for Traversing](https://www.w3schools.com/jquery/jquery_ref_traversing.asp)
### Append something new to list from form field, reset field
```
$("#thing-button").click(function() {
  var newThing = $("#thing-name").val();
  $("ul").append("<li>" + newThing + "</li>");
  $("#thing-name").val("");
});
```

### Adding an Event Listener vs. Triggering an Event
