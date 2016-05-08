#Lesson 7: Styling boxes
CSS and HTML is all about boxes — in this lesson we'll look at getting boxes to behave themselves, and do some fun stuff to the look of our web page.
##Box model
As mentioned in a previous lesson, all elements are laid out using an algorithm called the [box model](https://developer.mozilla.org/en-US/Learn/CSS/Introduction_to_CSS/Box_model).

Let's have some fun with our boxes. We'll add some styling to our <code>&lt;div&gt;</code> elements and <code>&lt;header&gt;</code> to pad them out a bit. Add the declarations one at a time so you can see what the effect is:

<pre>div, header {
  width: 70%;
  margin: 20px;
  padding: 20px;
  border: 2px solid black;
}</pre>

##Other things to try

Change your margin declaration to the following:

<pre>margin: 20px auto;</pre>

The space at the top of the boxes looks a bit silly. Try this:

<pre>h1, h2 {
 margin: 0 
}</pre>

You can add rounded corners pretty easily:

<pre>border-radius: 20px;</pre>

Your image might will look better with a border around it. We can center it too:

<pre>img {
  display: block;
  margin: 0 auto;
  border: 2px solid black
}</pre>

##Backgrounds and other effects

Let's add some other stuff to our boxes to make them more fun:

<pre>background-color: yellow;</pre>

<pre>background-image: url(http://1-background.com/images/vellum/vellum-pink-seamless-tile2.jpg);</pre>

<pre>background-image: url(http://findicons.com/files/icons/2315/default_icon/256/media_drum_kit.png);
background-repeat: no-repeat;
background-position: right top;</pre>

<pre>background-image: linear-gradient(to bottom right, yellow, green);</pre>

<pre>background: url(http://findicons.com/files/icons/2315/default_icon/256/media_drum_kit.png) no-repeat right top,
url(http://1-background.com/images/vellum/vellum-pink-seamless-tile2.jpg);</pre>

Why not try a text shadow or a box shadow? Can you remember how to do them from earlier in the course? Can you look it up?

You can find more ideas at [Advanced box effects](https://developer.mozilla.org/en-US/Learn/CSS/Styling_boxes/Advanced_box_effects).