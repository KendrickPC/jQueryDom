### Complete the following steps in the following file:

1. When the DOM is ready, console.log the message “Let’s get ready to party with jQuery!”
[jQuery Dom Content Loaded](https://api.jquery.com/ready/)
```js
$(document).ready(function() {
  console.log("Let's get ready to party with jQuery);
})
```

2. Give all images inside of an article tag the class of image-center (this class is defined inside of the style tag in the head).
```js
// Inside function (already declared):
$("article img").addClass("image-center");
```

3. Remove the last paragraph in the article.
```js
const test = $("article p").last().remove();
console.log(test); // Check for inner text:
```

4. Set the font size of the title to be a random pixel size from 0 to 100.
```js
const randomNum = Math.floor(Math.random() * 101);
console.log(randomNum);
$("#title").css("font-size", randomNum);
```

5. Add an item to the list; it can say whatever you want.
```js
$("ol").append("<li>Puppies are cute</li>")
```

6. Scratch that; the list is silly. Empty the aside and put a paragraph in it apologizing for the list’s existence.
```js
$("aside").children().remove();
$("aside").append("Sorry for the existence of the list.")
```

7. When you change the numbers in the three inputs on the bottom, the background color of the body should change to match whatever the three values in the inputs are.
[Get form field value](https://stackoverflow.com/questions/11654449/jquery-get-form-field-value)
```js
$(".form-control").on("change", function() {
  const red = $(".form-control").eq(0).val();
  // console.log("red: " + red);
  const blue = $(".form-control").eq(1).val();
  // console.log("blue: " + blue);
  const green = $(".form-control").eq(2).val();
  // console.log("green: " + green);
  $("body").css("background-color", `rgb(${red}, ${blue}, ${green})`);
})
```

8. Add an event listener so that when you click on the image, it is removed from the DOM.

```js
$("img").on("click", function() {
  $("img").remove();
})

// using evt.target is more specific, as we won't remove ALL images, just the click target:
$("img").on("click", function(evt) {
  // $("img").remove();
  $(evt.target).remove();
})
```