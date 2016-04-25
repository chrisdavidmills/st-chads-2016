#Lesson 4: Links and images
Before we move on to CSS, we'll explore two of the most important features of HTML — links and images. Think about why they are so important for a moment:

* Links are what makes the Web <em>A WEB</em>. Being able to link resources together and jump to completely different things with a single click is such an incredibly powerful concept; the Web wouldn't work without links.
* Images (and other media) are what makes the Web look nice and interesting. The Web would be really boring without images. 

##Images
Images are inserted into pages using the <code>&lt;img&gt;</code> element. Let's look at an example:

<pre>&lt;img src="myimage.png" alt="This is my image"&gt;</pre>

Some things to note here:

* This element has attributes — extra bits of information about the element, stored in name value pairs. Each new attribute has to have a space before it, and follow the pattern name="value".
* This is an empty element — it is just one tag — it doesn't have content or a closing tag.
* It is also called a <em>replaced element</em> — this is because the content you see as a result is not the text in the element — it is replaced by something else (in this case, an image.)

The <code>&lt;img&gt;</code> element seen above has two attributes:

* <code>src</code>: This contains the path to the image you want to embed.
* <code>alt</code>: This contains some text to describe the content of the image.

###Paths
The path we talked about above points to the image you want to embed — what does this mean? Say you have a folder with this structure:

<pre>website
   |
   index.html
   |
   style.css
   |
   images
     |
      — myimage.png
</pre>

If we wanted to embed the image in an <code>&lt;img&gt;</code> element inside the index.html file, we'd need to use the path <code>images/myimage.png</code>. If the HTML file was in a folder too, for example: 

<pre>website
   |
   pages
   | |
   |  —index.html
   |
   style.css
   |
   images
     |
      — myimage.png
</pre>

Then we'd need to use the path <code>../images/myimage.png</code> — two dots means "walk up the tree one level".

These are called relative paths. You can also use an absolute path to an image, for example

<code>http://dailypicksandflicks.com/wp-content/uploads/2013/04/Bring-Me-Another-Smurf-Baby.jpg</code> 

###Image types
There are many different types of image file; not all of them can be embedded on web sites. For example, <code>.psd</code> files are just for working in Photoshop, and are not suitable for the Web. If you try to access one of these through a web browser, it will probably try to download the file, and then pass it to Photoshop to open.

Common image file types used on the Web include:

* <code>.png</code>
* <code>.jpg</code>
* <code>.gif</code>

###Let's embed an image
1. Copy the <code>&lt;img&gt;</code> code example above, and embed it in your page. Let's put one somewhere underneath each <code>&lt;h2&gt;</code>.
2. Go to Google image search (or equivalent.)
3. Find an image you like
4. Right click on the image and select "View image"
5. Copy the web address of the image out of the address bar of your browser.
6. Paste it inside the double quotes of the <code>src</code> attribute. <code>src="PUT IT HERE"</code>.

###Altering your image size
You can add a <code>width=""</code> attribute to alter the size of your image, if it is too big to fit on the page. Let's try this now.



###Alt text
You might be thinking "why do we need the alt text"? It is so that there is a text alternative available if the image can't be shown, or seen:

* If you spell the image path wrong, the alt text will shown instead.
* Blind people use apps called screenreaders to read out web pages to them. If the image has alt text, they can get a description of the image.

Add some alt text your image now.


##Links
Now let's try adding some links to our page. A link is created by wrapping some text in an <code>&lt;a&gt;</code> element, and giving it an <code>href</code> attribute that points to the web page you want to link to:

<pre>&lt;a href="http://www.sabian.com/en/home"&gt;Sabian cymbals&lt;a&gt;</pre>

Like image paths, link paths can be relative or absolute. We'll just stick to absolute links in this course.

The main things to worry about with a link are:

* Making sure the web address is correct. If it isn't, you'll get one of those dreaded 404 errors.
* Making sure the link text (the text inside the element) makes sense in context, as well as out of content. This is important for accessibility, and search engine optimization.

 