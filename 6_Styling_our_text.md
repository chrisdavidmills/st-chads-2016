#Lesson 6: Styling our text
In this lesson we will get our text looking right. Start by opening up your Thimble project.
##Basic text styling
Go to your style.css file. At the moment there is only a single rule in there, which gives the body contents a new font.

First, change <code>body</code> to <code>html</code> — it is better to set global instructions on the <code>&lt;html&gt;</code>, in general.

Now, put <code>font-size: 10px</code> inside the first rule as well. See how this affects the page!

Next, we'll set some better sizes on our different element types, something like this:

<pre>h1 {
  font-size: 4rem;
}

h2 {
  font-size: 3.2rem;
}

p, li {
  font-size: 1.6rem;
}</pre>

We can do better here. Let's give the paragraphs and list items some <code>line-height</code>, to make the text more legible. Add the following to the <code>p, li</code> rule:

<pre>line-height: 1.5</pre>

There are many other text-related properties we could use; you could also perhaps experiment with a couple more:

* <code>text-transform: uppercase</code>: Turns all text to uppercase.
* <code>letter-spacing: 0.5px</code>: Adds space between letters.
* <code>word-spacing: 0.2rem</code>: Adds space between words.

Try centering your main heading too, by adding this declaration to it:

<pre>text-align: center;</pre>


##Color
We met colour in the previous article:

<pre>color: red;</pre>

Let's try adding some colour to our text — nothing too light and unreadbale now!

You can also set color in a number of other ways:

<pre>color: #ff0000;
color: rgb(255,0,0);
color: rgba(255,0,0,1);
color: hsl(0,100%,50%);</pre>


##Fonts
Last, let's make our page a bit more exciting with some different fonts. It is the <code>font-family</code> property we saw earlier that handles this.

There are only a few fonts that will definitely work on all computers, e.g. arial, verdana, 'Times new roman' (the default), georgia, 'Courier new'.

Try using a few of these in the <code>html</code> rule, and then let's set a different font on the <code>&lt;h1&gt;</code> and <code>&lt;h2&gt;</code> elements. Having a different font on the headings, and on the rest of the text, is fairly common.

There is a way to set custom fonts on your page — web fonts. Implementing the code all yourself is quite challenging, so we'll use the [Google Fonts](https://www.google.com/fonts) service.

1. Go to Google Fonts
2. Select a couple of fonts, one for your headings, and one for the rest of your text.
3. Click "Use" in the bottom right hand corner
4. Add the code in section 3. to the head of your HTML document, before the existing <code>&lt;link&gt;</code> element.
5. Section 4 gives you the <code>font-family</code> declarations you need to use these fonts in your CSS. Apply your header font to your <code>h1,h2</code> rule, and your body font to your <code>html</code> rule.