#Lesson 9: Decorations and fun stuff
In this lesson I'll show you a couple more fun things, and talk about next steps if you want to learn more.

##transitions/animations
You can animate things on the page using CSS, using transitions and animations. Today we'll just look at transitions.

first you need to set up an element to transition when it is hovered over with the mouse:

<pre>header p {
  transition: all 2s;
}</pre>

<code>all</code> is what properties you want to transition, <code>2s</code> is the length of time of the transition.

Then you set up what you want to happen after the transition:

<pre>header:hover p {
  background-color: blue;
}</pre>

For example.

you can try transitioning any property you want, for example:

<pre>border-radius: 50px; 
color: white;
font-size: 200%;
opacity: 0;</pre>

You could also try some transforms — ways of changing the way the element appears on the page. Try these:

<pre>transform: rotate(180deg);
transform: rotateX(180deg);
transform: skew(20deg,10deg);
transform: translate(50px,100px);</pre>

Note: We are selecting the parent element to hover, not the actual element we are interested in, so that the animation will keep happening whenever the parent element is hovered over. This stops the animation from going funny when the animated element moves away from the mouse cursor, e.g. by a rotation.

Note: You can use * to select all elements on the page, e.g. you could do:

<pre>* p {
  transition: all 2s;
}

*:hover p {
  background-color: blue;
}</pre>

##A little bit of JavaScript

JavaScript is the third language that powers websites. This is much more complicated than HTML or CSS, which is why I've not tried to teach you much of it in this course.

* First, go to the FILES column and press the green plus (+) button. Choose JavaScript from the options box.

* This will create a file called script-1.js, which contains some instructions. We need to follow these instructions.

* When you've done it right, you'll get a popup box appearing on your screen. Press OK to dismiss this!

* Now you can delete all the stuff inside the .js file.

* Next, try pasting one of the below scripts inside the .js file, and seeing what they do

<pre>var elements = document.querySelectorAll('*');
for(i = 0; i < elements.length-1; i++) {
  elements[i].onclick = tricky;
}

function tricky(e) {
  e.target.style.opacity = 0;
}</pre>

for this one, try changing <code>opacity = 0;</code> to something like

<pre>background = 'blue';
fontFamily = 'monospace';</pre>

<hr>

<p>Here's another fun and rather silly example to try out:</p>

<pre>var btn = document.createElement('button');
btn.textContent = 'Click me!!';
document.body.appendChild(btn);

btn.onclick = function() {
  var para = document.createElement('p');
  para.textContent = 'I am a new paragraph';
  document.body.appendChild(para);
  para.onclick = function() {
    var answer = prompt("Enter new text");
    this.textContent = answer;
  }
}</pre>


##Resources

To end, let's give you some resources to learn more!

* [MDN Learning Area](https://developer.mozilla.org/en-US/Learn)
	* [HTML](https://developer.mozilla.org/en-US/Learn/HTML)
	* [CSS](https://developer.mozilla.org/en-US/Learn/CSS)
	* [JavaScript](https://developer.mozilla.org/en-US/Learn/JavaScript)
* [Codecademy](https://www.codecademy.com/)
* [code.org](https://code.org/)
	



