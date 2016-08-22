# jQuery
## $(document).ready()

Add a script element at the top of your page. Your browser will run any JavaScript inside a script element, including jQuery.

Inside your script element, add this code:
`$(document).ready(function() {` to your script. Then close it on the following line (still inside your script element) with: `});`. The important thing to know is that code you put inside this function will run as soon as your browser has loaded your page. This is important because without your document ready function, your code may run before your HTML is rendered, which would cause bugs.

```javascript
<script>
  $(document).ready(function() {

  });
</script>
```

> The HTML the code is working with

```
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

## Target elements

### by Selectors
* All jQuery functions start with a `$`, usually referred to as a `dollar sign operator`, or as `bling`.
* jQuery often selects an HTML element with a `selector`, then does something to that element.
* For example, let's make all of your button elements bounce. Just add this code inside your document ready function:

```javascript
$("button").addClass("animated bounce");
```

Need:

* jQuery library
* Animate.css library - for the animated bounce class

### by Class
* let's target your div elements with the class well by using the `$(".well")` selector.
* just like with CSS declarations, you type a `.` before the class's name.
* use jQuery's `.addClass()` function to add the classes `animated` and `shake`.

```javascript
$(".text-primary").addClass("animated shake");
```

For example, you could make all the elements with the class text-primary shake by adding the following to your document ready function:

### by ID
* target elements by their id attributes.
* First target your button element with the id target3 by using the `$("#target3")` selector.
* just like with CSS declarations, you type a `#` before the id's name.
* use jQuery's `.addClass()` function to add the classes `animated` and `fadeOut`.

```javascript
$("#target6").addClass("animated fadeOut").
```

Here's how you'd make the button element with the id target6 fade out.

### Target parent element
Every HTML element has a parent element from which it inherits properties.

For example, your jQuery Playground `h3` element has the parent element of `<div class="container-fluid">`, which itself has the parent body.

jQuery has a function called `.parent()` that allows you to access the parent of whichever element you've selected.

Here's an example of how you would use the `.parent()` function if you wanted to give the parent element of the left-well element a background color of blue:

```javascript
$("#left-well").parent().css("background-color", "blue")
```

### Target children of an element
Many HTML elements have children which inherit their properties from their parent HTML elements.

For example, every HTML element is a child of your body element, and your "jQuery Playground" h3 element is a child of your `<div class="container-fluid">` element.

jQuery has a function called `.children()` that allows you to access the children of whichever element you've selected.

Here's an example of how you would use the `.children()` function to give the children of your left-well element the color of blue:

```javascript
$("#left-well").children().css("color", "blue")
```

### Target specific child
You've seen why id attributes are so convenient for targeting with jQuery selectors. But you won't always have such neat ids to work with.

Fortunately, jQuery has some other tricks for targeting the right elements.

jQuery uses CSS Selectors to target elements. `target:nth-child(n)` css selector allows you to select all the nth elements with the target class or element type.

Here's how you would give the third element in each well the bounce class:
```javascript
$(".target:nth-child(3)").addClass("animated bounce");
```

### Target even numbered elements
You can also target all the even-numbered elements.

Here's how you would target all the odd-numbered elements with class target and give them classes:

```javascript
$(".target:odd").addClass("animated shake");
```

Note that jQuery is zero-indexed, meaning that, counter-intuitively, :odd selects the second element, fourth element, and so on.
### Target body
jQuery can target the body element as well

Here's how we would make the entire body fade out:

```javascript
$("body").addClass("animated fadeOut");
```

## Remove Classes
In the same way you can add classes to an element with jQuery's `addClass()` function, you can remove them with jQuery's `removeClass()` function.

```javascript
$("#target2").removeClass("btn-default");
```

## Change CSS
* We can also change the CSS of an HTML element directly with jQuery.
* jQuery has a function called `.css()` that allows you to change the CSS of an element.

This is slightly different from a normal CSS declaration, because the CSS property and its value are in quotes, and separated with a comma instead of a colon. Here's how we would change its color to blue:

```javascript
$("#target1").css("color", "blue");
```

## Disable Element
* change the non-CSS properties of HTML elements with jQuery. For example, you can disable buttons. When you disable a button, it will become grayed-out and can no longer be clicked.
* jQuery has a function called `.prop()` that allows you to adjust the properties of elements.

Here's how you would disable all buttons:

```javascript
$("button").prop("disabled", true);
```

## Change Text
Using jQuery, you can **change the text between the start and end tags of an element**. You can even change **HTML markup**.

jQuery has a function called `.html()` that lets you add HTML tags and text within an element. **Any content** previously within the element will be **completely replaced** with the content you provide using this function.

Here's how you would rewrite and emphasize the text of our heading:

```javascript
$("h3").html("<em>jQuery Playground</em>");
```

jQuery also has a similar function called `.text()` that **only alters text** without adding tags. In other words, this function will not evaluate any HTML tags passed to it, but will instead treat it as the text you want to replace the existing content with.

```javascript
$("h3").text("jQuery Playground");
```

## Remove Element
Now let's remove an HTML element from your page using jQuery.

jQuery has a function called `.remove()` that will remove an HTML element entirely

```javascript
$("#target4").remove();
```

## Move Elements
* jQuery has a function called `appendTo()` that allows you to select HTML elements and append them to another element.

For example, if we wanted to move target4 from our right well to our left well, we would use:

```javascript
$("#target4").appendTo("#left-well");
```

## Clone Element
In addition to moving elements, you can also copy them from one place to another.

* jQuery has a function called `clone()` that makes a copy of an element.

For example, if we wanted to copy target2 from our left-well to our right-well, we would use:

```javascript
$("#target2").clone().appendTo("#right-well");
```

Did you notice this involves sticking two jQuery functions together? This is called **function chaining** and it's a convenient way to get things done with jQuery.
