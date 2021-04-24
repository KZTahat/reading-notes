# Introductory HTML and JavaScript
## Structure 
The use of headings and subheadings in any document often reflects a hierarchy of information. For example, a document might start with a large heading, followed by an introduction or the most important information. This might be expanded upon under subheadings lower down on the page. When using a word processor to create a document, we separate out the text to give it structure. Each topic might have a new paragraph, and each section can have a heading to describe what it covers.On the right, you can see a 
simple document in Microsoft Word. The different styles for the document, such as different levels of heading, are shown in the drop down box. If you regularly use Word, you might have also used the formatting toolbar or palette to do this. To describe the structure of a web page, we add code to the words we want to appear on the page. You can see the HTML code for this page below. We start to look at it in more detail on the next page.

```
<html>
<body>
 <h1>This is the Main Heading</h1>
 <p>This text might be an introduction to the rest of 
 the page. And if the page is a long one it might 
 be split up into several sub-headings.<p>
 <h2>This is a Sub-Heading</h2>
 <p>Many long articles have sub-headings so to help 
 you follow the structure of what is being written. 
 There may even be sub-sub-headings (or lower-level 
 headings).</p>
 <h2>Another Sub-Heading</h2>
 <p>Here you can see another sub-heading.</p>
</body>
</html>
```

## Extra Markup
Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included).When we come to look at CSS and its box model, the use of a DOCTYPE can also help the browser to render a page correctly. Because XHTML was written in XML, you will sometimes see pages that use the XHTML strict DOCTYPE start with the optional XML declaration. Where this is used, it should be the first thing in a document. There must be nothing before it, not even a space.
- _Comments in **HTML**_
  If you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters:
  ```
  <!-- comment goes here -->
  ```
  It is a good idea to add comments to our code because, no matter how familiar we are with the page at the time of writing it, when we come back to it later (or if someone else needs to look at the code), comments will make it much easier to understand.Although comments are not visible to users in the main browser window, they can be viewed by anyone who looks at the source code behind the page. On a long page we will often see comments used to indicate where sections of the page start or end, and to pass on notes to help anyone who is looking at the code understand it. Comments can also be used around blocks of code to stop that code from being displayed in the browser.
  
- _**ID** attribute*_:
  Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page. Its value should start with a letter or an underscore (not a number or any other character).It is important that no two elements on the same page have the same value for their idattributes (otherwise the value is no longer unique).

  As we will see when you come to look at CSS in the next section, giving an element a unique identity allows us to style it differently than any other instance of the same element on the page. For example, we might want to assign one paragraph within the page (perhaps a paragraph containing a pull quote) a different style than all of the other paragraphs. If we go on to learn about JavaScript, id attributes can be used to allow the script to work with that particular element.The id attribute is known as a **global attribute** because it can be used on any element.
  
- _**CLASS** attribute_:
  Every HTML element can also carry a class attribute. Sometimes, rather than uniquely identifying one element within a document, we will want a way to identify several elements as being different from the other elements on the page. For example, we might have some paragraphs of text that contain information that is more important than others and want to distinguish these elements, or we might want to differentiate between links that point to other pages on our own site and links that point to external sites. To do this we can use the class attribute. Its value should describe the class it belongs to. The class attribute on any element can share the same value.
  
- _**DIV** Element_ 
  he <div> element allows you to group a set of elements together in one block-level box.For example, you might create a <div> element to contain all of the elements for the header of your site (the logo and the navigation), or you might create a <div> element to contain comments from visitors.
 ```
 <div id="header">
<img src="images/logo.gif" alt="Anish Kapoor" />
<ul>
 <li><a href="index.html">Home</a></li>
 <li><a href="biography.html">Biography</a></li>
 <li><a href="works.html">Works</a></li>
 <li><a href="contact.html">Contact</a></li>
</ul>
</div><!-- end of header -->
 ```
  In a browser, the contents of the **div** element will start on a new line, but other than this it will make no difference to the presentation of the page. Using an id or class attribute on the <div> element, however, means that you can create CSS style rules to indicate how much space the <div> element should occupy on the screen and change the appearance of all the elements contained within it.It can also make it easier to follow your code if you have used <div> elements to hold each section of the page.
  
- 
  
  
  
  
  
