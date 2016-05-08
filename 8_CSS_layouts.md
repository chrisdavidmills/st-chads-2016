#Lesson 8: CSS layouts
So far we have looked at how to style our text and boxes, but how do we deal with getting things to move around the screen to where you want them? This is called CSS layout, and in this lesson we'll look at the basics.

We've already done a little bit of layout work when we centered our boxes in side their parent elements; here we'll take it further.
##Floating
There are many ways to layout web pages, but one of the best supported and most common layout tools is CSS floats. This was originally created to allow web developers to float text around images in a magazine layout style, but these days it is more common to use it to create multi column layouts.

Let's turn our site into a 2 column layout.

###Updating your HTML

First, add some class names to your <code>&lt;div&gt;</code> elements in your HTML. Something like the following:

<pre>&lt;div class="main"&gt;

&lt;div class="equip"&gt;</pre>

Next, below the last <code>&lt;/div&gt;</code> tag (and above the <code>&lt;/body&gt;</code>), add a <code>&lt;footer&gt;</code>, like the following: 

<pre>&lt;footer&gt;
  Site created by Chris Mills
&lt;/footer&gt;</pre>

###Adding layout CSS
We are going to create a 2 column layout — we need to make the two <code>&lt;div&gt;</code> elements narrow enough so that they will fit side by side.

By default, block level elements are 100% of the width of their parents. Let's set each element to have 45% width:

<pre>.main {
  width: 45%;
}

.equip {
  width: 45%;
}</pre>

Let's also set the padding we put on the <code>&lt;div&gt;</code>s in the previous lesson to 2%.

<pre>padding: 2%;</pre>

So what total width have we got, for both <code>&lt;div&gt;</code>s and their padding?

Next, we need to float one of the <code>&lt;div&gt;</code>s to the left, and one to the right.

<pre>.main {
  width: 45%;
  float: left;
}

.equip {
  width: 45%;
  float: right;
}</pre>

So, we still have a problem — our <code>&lt;footer&gt;</code> is flying up underneath the shortest column! This is because when you float an element, everything floats around it. When you want the floating to stop, you have to turn it off, and this is done with the <code>clear</code> property:

<pre>footer {
  clear: both;
}</pre>

###Other considerations

It might look better if we made the header and footer as wide as the two columns:

<pre>header, footer {
   width: 96%;
}</pre>

You might want to add a bit more content if one of the columns is a lot shorter than the other.

One more problem is the image, which at certain widths will overflow its column. This can be fixed by setting the following on the image:

<pre>max-width: 100%;</pre>


##Positioning

Positioning is another common technique used to do layout tasks on elements.

You set different types of positioning on elements using the <pre>position</pre> property. The default value is <code>static</code>, which means that the elements will just sit in their normal position.

Let's play with the different values:

* <code>relative</code>
* <code>absolute</code>
* <code>fixed</code>

When we've set the <code>position</code> property, we can then alter the position of the element using the following properties:

* <code>top</code>
* <code>right</code>
* <code>bottom</code>
* <code>left</code>

###Positioning example

Let's implement something simple to show you what can be done with positioning. A tabbed interface is a nice example, so let's create one.

First of all, create a new project in Thimble.

Next, put the following HTML inside the body of the <code>index.html</code> file:

<pre>&lt;ul&gt;
  &lt;li&gt;&lt;a href="#t1"&gt;Tab 1&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#t2"&gt;Tab 2&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="#t3"&gt;Tab 3&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;section&gt;

  &lt;article id="t1"&gt;

    &lt;h2&gt;The first tab&lt;/h2&gt;

    &lt;p&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque turpis nibh, porttitor nec venenatis eu, pulvinar in augue. Vestibulum et orci scelerisque, vulputate tellus quis, lobortis dui. Vivamus varius libero at ipsum mattis efficitur ut nec nisl. Nullam eget tincidunt metus. Donec ultrices, urna maximus consequat aliquet, dui neque eleifend lorem, a auctor libero turpis at sem. Aliquam ut porttitor urna. Nulla facilisi.&lt;/p&gt;

  &lt;/article&gt;

  &lt;article id="t2"&gt;

    &lt;h2&gt;The second tab&lt;/h2&gt;

    &lt;p&gt;This tab hasn't got any Lorem Ipsum in it. But the content isn't very exciting all the same.&lt;/p&gt;

  &lt;/article&gt;

  &lt;article id="t3"&gt;

    &lt;h2&gt;The third tab&lt;/h2&gt;

    &lt;p&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque turpis nibh, porttitor nec venenatis eu, pulvinar in augue. And now an ordered list: how exciting!&lt;/p&gt;

    &lt;ol&gt;
      &lt;li&gt;dui neque eleifend lorem, a auctor libero turpis at sem.&lt;/li&gt;
      &lt;li&gt;Aliquam ut porttitor urna.&lt;/li&gt;
      &lt;li&gt;Nulla facilisi&lt;/li&gt;
    &lt;/ol&gt;

  &lt;/article&gt;

&lt;/section&gt;</pre>

How let's style the page. Switch over to your CSS file, and add the following to it:

<pre>body {
  width: 450px;
  height: 400px;
  margin: 0 auto;
}</pre>

Next, we'll add these rules and declarations one by one, to see how they work; these are for styling the tabs at the top of the UI content panes:

<pre>ul {
  padding-left: 0;
}

li {
  display: inline;
  float: left;
  list-style-type: none;
  width: 150px;
}

li a {
  display: inline-block;
  text-decoration: none;
  width: 100%;
  line-height: 3;
  background-color: red;
  color: black;
  text-align: center;
}

li a:focus, li a:hover {
  background-color: #a60000;
  color: white;
}

.active {
  background-color: #a60000;
  color: white;
}</pre>

Finally, for the CSS, we'll style the actual UI content panes. Again, let's add these bits one by one, to help us understand how they work:

<pre>section {
  clear: both;
  color: white;
  position: relative;
  height: 352px;
}

article {
  background-color: #a60000;
  position: absolute;
  padding: 10px;
  height: 352px;
  top: 0;
  left: 0;
}

#t1 {
  z-index: 1;
}

article:target {
  z-index: 2;
}</pre>

Try your example now — to do so, you'll have to publish your page using the "Publish" button, and go to the web address.

One thing is wrong — it would be really nice to have the active tab (the one whose coresponding content is being shown) staying the same color as the content pane. To do this reliably, we'll need to use some JavaScript; first, change the first tab HTML:

<pre>&lt;li&gt;&lt;a href="#t1"&gt;Tab 1&lt;/a&gt;&lt;/li&gt;</pre>

to this:

<pre>&lt;li&gt;&lt;a href="#t1" class="active"&gt;Tab 1&lt;/a&gt;&lt;/li&gt;</pre>


Now add the following just before the closing body tag (<code>&lt;/body&gt;</code>).

<pre>&lt;script&gt;

var tabs = document.querySelectorAll('ul li a');

for(i = 0; i < tabs.length; i++) {
  var tab = tabs[i];
  setTab(tab);
}

function setTab(tab) {
  tab.onclick = function() {
    for(i = 0; i < tabs.length; i++) {
      if(tabs[i].getAttribute('class')) {
        tabs[i].removeAttribute('class');
      }
    }

    tab.setAttribute('class', 'active');
  }
}

&lt;/script&gt;</pre>