#Lesson 5: CSS basics
CSS is used to style our HTML content — to make it look nice. If the HTML is like the bricks and foundations of a house, the CSS is like the paint, wallpaper, pictures and other decorations.
##CSS basics
A basic CSS rule looks like this:

<pre>p {
  color: red;
}</pre>

Let's try adding this to our code — in the "FILES" pane of the Thimble interface, click on the <code>style.css</code> file to switch to it.

Copy the above code and paste it at the bottom of the file. You should see all your paragraphs go red. So what happened? The above code has three parts:

* <code>p</code>: This is the selector; the bit that selects the element(s) to be styled by the rule.
* <code>color</code>: This is the property name — when we've selected the element(s) to style, we choose properties of the element(s) to change.
* <code>red</code>: The is the property value — the value we are changing the property to.

Each property/value pair is called a <strong>declaration</strong>; the declarations must be contained inside curly braces (<code>{ ... }</code>).

Each property must be separated from its value by a colon (<code>:</code>), and each declaration must be separated from the next by a semi-colon (<code>;</code>). 


### Playtime
At this point, you might want to create a new Thimble project for experiments.

Element selection:

* First, try changing the selector to the name of a different element, like <code>h1</code> or <code>li</code>, and see what happens.
* You can make one rule apply to several selectors by separating them with commas, for example <code>h1, h2</code>.
* You can select other things with different types of selectors:
	* Class selectors: select any element with a certain class attribute value, e.g. <code>.summary</code> would select <code>&lt;p class="summary"&gt;This is a summary&lt;/p&gt;</code>
	* Attribute selectors: select elements only if they have a certain attribute, e.g. <code>img[alt]</code> would select <code>&lt;a&gt;</code> elements only if they have an <code>alt</code> attribute.
	* Pseudo-classes: Select elements only if they are in a certain state, e.g. <code>p:hover</code> will select patagraphs only when they are being hovered over with the mouse pointer.
	* There are [loads of other selectors](https://developer.mozilla.org/en-US/Learn/CSS/Introduction_to_CSS/Selectors).
	
Different CSS properties to try:

* <code>background-color</code>: Sets a colour for the element's background, e.g. <code>background-color; red</code> or <code>background-color: blue</code>.
* <code>border</code>: Sets a thickness, style and colour for the element's border, e.g. <code>border: 2px solid black</code>.
* <code>padding</code>: Sets spacing around the content of the element, for example try <code>padding: 10px</code>.
* <code>margin</code>: Sets spacing around the outside of the element, for example try <code>margin: 10px</code>
* <code>font-size</code>: Sets the size of the text. Try <code>font-size: 30px</code>, or <code>font-size: 200%</code>.
* <code>width</code>: Sets the width of an element. Try <code>width: 300px</code>, or <code>width: 90%</code>
* <code>background-image</code>: Sets an image to appear in the background of the element. This can be a simple image, for example <code>background-image: url(path/to/my/image.png)</code> or a gradient, for example <code>background-image: linear-gradient(to right, red, black)</code>.
* <code>text-shadow</code>: Sets a shadow on the text, for example <code>text-shadow: 3px 3px 5px black</code>.
* <code>box-shadow</code>: Sets a shadow on the element, for example <code>box-shadow: 3px 3px 5px black</code>.
* <code>opacity:</code>: Allows you to make the element semi-transparent. Try <code>opacity: 0.5</code>.

There are [a lot more CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) to play with, if you feel like it.


	
	


