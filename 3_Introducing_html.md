#Lesson 3: Introducing HTML
Let's start getting deep into some HTML. Here we'll learn the basic essentials of HTML, and then start writing our own web page.

Note: Start thing about what you'd like your web page to be about!

##HTML basics
HTML is the language we use to structure our web page content — the text, images, and other items we are consuming when go to a web page. If a web page were like a house, HTML would be like the bricks, concrete foundations and other materials that make up the structure of the house.

For a webpage to be effective, it needs a good structure of context — text is particularly important. If a webpage only consisted of images, for example, you would have a number of problems:

* Search engines like Google index webpages based on the keywords they contain in their text, and put them in search rankings accordingly. With no text, your page would not findable on search engines.
* People with visual impairments (e.g. blind, very short sighted) often use a piece of software called a screenreader, to literally read web pages out to them. With not text, they would not be able to make any sense of your web page.

HTML is made up of elements — generally speaking, an element gives a job, or a role, to a piece of text. This is not always exactly the case — some elements do other things, like embed images in web page. But we wanted to start simple.

Let's look at an example:

<code>&lt;p&gt;This is a paragraph.&lt;/p&gt;</code>

The important bits are:

* <code>&lt;p&gt;</code>: This is the opening tag of the element. This signifies where the element starts.
* <code>This is a paragraph.</code>: This is the text that will be affected by the element. In this case, the text is being turned into a paragraph.
* <code>&lt;/p&gt;</code>: This is the closing tag of the element. This signifies where the element ends.
* The whole lot together is called an element.

##Anatomy of an HTML document
Let's look at the HTML provided by Thimble:

<pre>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1"&gt;
  &lt;title&gt;Made with Thimble&lt;/title&gt;
  &lt;link rel="stylesheet" href="style.css"&gt;
&lt;/head&gt;
&lt;body&gt;

  &lt;h1&gt;Welcome to Thimble&lt;/h1&gt;

  &lt;p&gt;Make something &lt;strong&gt;amazing&lt;/strong&gt; with the web!&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>

The important parts of the HTML structure are:

* The doctype (<code>&lt;!DOCTYPE html&gt;</code>): This needs to be here; let's just leave it at that for now.
* The html element (<code>&lt;html&gt;&lt;/html&gt;</code>): This is the container for the entire HTML page
* The head (<code>&lt;head&gt;&lt;/head&gt;</code>): This contains metadata — information about the page, which won't appear in the actual web page content. For example, a link to some CSS to style the page, the title of the web page, etc.
* The body (<code>&lt;body&gt;&lt;/body&gt;</code>): This is the container for the actual content of your web page, the stuff that you'll actually see on the page. 

##Adding our basic body structure
Let's add the following body structure to our web page — this needs to go in between <code>&lt;body&gt;</code> and <code>&lt;/body&gt;</code>:

<pre>&lt;header&gt;

&lt;/header&gt;

&lt;div&gt;
  
&lt;/div&gt;

&lt;div&gt;
  
&lt;/div&gt;</pre>

This will eventually be a page header, plus two columns of content. Delete what was there before.

Note: Don't get header confused with head — they are two different things.

##Writing basic text

In the rest of this lesson we'll create a basic text structure for your web page.

###Headings

Web pages contain heading hierarchies, just like a book does. You'll have a main title, section titles, sub-section titles, etc.

We need three headings on our page, one inside our <code>&lt;header&gt;&lt;/header&gt;</code> element:

<pre>&lt;h1&gt;Playing the drums&lt;/h1&gt;</pre>

And one inside each of our <code>&lt;div&gt;&lt;/div&gt;</code> elements.

<pre>&lt;h2&gt;Getting started with drums&lt;/h2&gt;</pre>

<pre>&lt;h2&gt;Drum equipment to buy&lt;/h2&gt;</pre>

###Paragraphs

We've already seen a paragraph, earlier on. Add a 1-2 underneath each h2 heading.

<pre>&lt;p&gt;This website is dedicated to giving your the information
 you need to start playing the drums.&lt;/p&gt;</pre>

###Lists
You can use list markup to mark up a list:

<pre>&lt;ul&gt;
  &lt;li&gt;This is&lt;/li&gt;
  &lt;li&gt;an unordered&lt;/li&gt;
  &lt;li&gt;list&lt;/li&gt;
&lt;/ul&gt;

&lt;ol&gt;
  &lt;li&gt;This is&lt;/li&gt;
  &lt;li&gt;an ordered&lt;/li&gt;
  &lt;li&gt;list&lt;/li&gt;
&lt;/ol&gt;</pre>

Try adding a list to your page.


###Emphasis

You can also emphasise words in different ways:

<pre>&lt;p&gt;Mastering the drums takes &lt;em&gt;a lot&lt;/em&gt; of practice.&lt;/p&gt;</pre>

<pre>&lt;p&gt;The first simple rock beat you'll learn is called
 an &lt;strong&gt;eighth beat&lt;/strong&gt;.&lt;/p&gt;</pre>
 
 Again, try this out on your page.