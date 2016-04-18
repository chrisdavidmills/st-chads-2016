#Lesson 2: Introducing our toolset
In this lesson we will look at the main tool we'll use in the course to write code and learn skills — Mozilla Thimble.

We'll also introduce the languages we'll be learning in this course: HTML (Hypertext Markup Language) and CSS (Cascading Stylesheets.)
##Getting familiar with your tool
There are quite a few online code editors to choose from, but we'll be using [Mozilla Thimble](https://thimble.mozilla.org/en-US/).

This is a webpage (some might call it a web application) that emulates a website and makes it easier to experiment with code — Thimble does some of the hard setup work so that you don't have to worry about it.

###A "normal" website
A normal website is made up of several files that sit in a folder on your computer, and work together to make up the whole website:

* HTML: One or more <code>.html</code> files contain the content for the web site: The words you see on the web page, etc. When you used [Xray goggles](https://goggles.mozilla.org/) in the last session, the data you were looking at when you clicked on the parts of the page is HTML data.
* CSS: One or more <code>.css</code> files contain code that styles the page — this code allows you to specify colours, sizes, borders, animations, layouts, etc.
* JavaScript: One or more <code>.js</code> files specify code that gives your webpages superpowers — JavaScript is a full programming language that basically allows you make your webpages do anything. We won't be teaching any JavaScript in this course, as it's a lot more complicated than HTML/CSS, and don't want to inflict it on total beginners.

Webpages also have other files involved, for example images or videos that get embedded in webpages, and other resources that you might want to make available, such as PDFs, word documents, etc.

When you make a website, you have to create all the files, put them in the right places, and then write lines of code that make the files talk to one another (e.g. to apply the CSS to the HTML, or embed images in the HTML.) This can be complicted to sort out, but Thimble does most of this organization for you (at least, the HTML and CSS files), making things easier.

###Logging in and starting a new project

1. The first step is to go to the [Mozilla Thimble](https://thimble.mozilla.org/en-US/) website, and login using the "Log In" link on the top right.

2. When successful, you should return to the homepage; now you'll see a "Welcome" message up at the top right.

3. Click on this and choose the "New Project" option. This will take you to the starting page of your project. Here we have several parts — the most impoartant ones are as follows:

	* Your project name. You can click on "Untitled project" to enter a new name for your project.
	* Files: We already have an HTML and a CSS file in our project already, which is basically all we need, but this is where we can create new files to go in our project. You can also click on each file to view its contents.
	Editor: This shows the currently selected file, and allows you to edit your code.
	Preview: This shows what your webpage currently looks like; the preview updates automatically as you change the code in the file.
	Publish: This allows you to publish your web page to the Web. When you press this button, you need to enter a project description and press the second Publish button, and it'll give you a web address when your finished site is published. Exciting! This is also how you save your project.
	
###Trying out some web code

Let's try out some HTML and CSS to round off the lesson.

<code>&lt;h1&gt;HTML elements look like this&lt;/h1&gt;</code>

CSS looks like this:

<pre>h1 {
  color: red;
}</pre>