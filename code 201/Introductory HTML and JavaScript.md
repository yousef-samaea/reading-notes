Read: 01 - Introductory HTML and JavaScript
***Structure***
**How Pages Use Structure**

Think about the stories you read in a newspaper: for each story, there will be a headline, some text, and possibly some images. If the article is a long piece, there may be subheadings that split the story into separate sections or quotes from those involved. Structure helps readers understand the stories in the newspaper.

The structure is very similar when a news story is viewed online (although it may also feature audio or video . This is illustrated on the right with a copy of a newspaper alongside the corresponding article on its website.

Now think about a very different type of document — an insurance form. Insurance forms often have headings for different sections, and each section contains a list of questions with areas for you to fill in details or checkboxes to tick. Again, the structure is very similar online

**Structuring Word Documents**

The use of headings and subheadings in any document often reflects a hierarchy of information. For example, a document might start with a large heading, followed by an introduction or the most important information.

This might be expanded upon under subheadings lower down on the page. When using a word processor to create a document, we separate out the text to give it structure. Each topic might have a new paragraph, and each section can have a heading to describe what it covers.

**HTM L Describes the Structure of Pages**

In the browser window you can see a web page that features exactly
the same content as the Word document you met on the page 18. To
describe the structure of a web page, we add code to the words we want
to appear on the page.

You can see the HTML code for this page below. Don't worry about what
the code means yet. We start to look at it in more detail on the next
page. Note that the HTML code is in blue, and the text you see on screen
is in black.

**example**

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

*The HTML code (in blue) is made up of characters that live inside angled brackets — these are called HTML elements. Elements are usually made up of two tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags.*

Tags act like containers. They tell you something about the information that lies between their opening and closing tags.

*Attributes Tell Us More About El ements*

Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.

**Body, Head & Title**

<body>

You met the <body> element in the first example we created. Everything inside this element is shown inside the main browser window

<head>
Before the <body> element you will often see a <head> element. This contains information about the page (rather than information that is shown within the main part of the browser window that is highlighted in blue on the opposite page). You will usually find a <title> element inside the <head> element.

<title>
The contents of the <title> element are either shown in the top of the browser, above where you usually type in the URL of the page you want to visit, or on the tab for that page (if your browser uses tabs to allow you to view multiple pages at the same time).


**Creating a Web Page on a PC**

To create your first web page on a PC, start up Notepad. You can find this by going to: Start All Programs (or Programs) Accessories Notepad You might also like to download a free editor called Notepad++ from notepad-plus-plus.org. 

Type the code shown on the right.

Go to the File menu and select Save as... You will need to save the file somewhere you can remember. If you like, you could create a folder for any examples that you try out from this book. Save this file as first-test. html. Make sure that the Save as type drop down has All Files selected.

Start your web browser. Go to the File menu and select Open. Browse to the file that you just created, select it and click on the Open button. The result should look something like the screen shot to the left. If it doesn't look like this, find the file you just created on your computer and make sure that it has the file extension .html (if it is .txt then you need to go back to Notepad and save the file again, but this time put quote marks around the name "firsttest. html").

**Code in a Content Management Systemc**

If you are working with a content management system, blogging platform, or e-commerce application, you will probably log into a special administration section of the website to control it. The tools provided in the administration sections of these sites usually allow you to edit parts of the page rather than the entire page, which means you will rarely see the <html>, <head>, or <body> elements. Looking at the content
management system on the opposite page, you have a box that allows you to enter a title for the page, another box for the main article, a way to enter a publication date, and something to indicate which section of the site this page belongs in. 

***Extra Markup***

 *DO CTYPEs*

 Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included). We will therefore be including one in each example for the rest of the book.

*Id Attribute*

Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page. Its value should start with a letter or an underscore (not a number or any other character). It is important that no two elements on the same page have the same value for their id attributes (otherwise the value is no longer unique)

***HTML5 Layout***

**HTML5 is introducing a new set ofelements that help define the structure ofa page. Traditional HTML Layouts**

For a long time, web page authors used <div> elements to grouptogether related elements on the page (such as the elements that form aheader, an article, footer or sidebar). Authors used class or id attributesto indicate the role of the <div> element in the structure of the page.

**New Html 5 Layout Elements**

HTML5 introduces a new set of elements that allow you to divide up theparts of a page. The names of these elements indicate the kind of contentyou will find in them. They are still subject to change, but that has notstopped many web page authors using them already.

**Headers & Footers <header> <footer>**

The <header> and <footer> elements can be used for: ●● The main header or footer that appears at the top or
bottom of every page on the site. ●● A header or footer for an individual <article> or <section> within the page.

*Articles*

The <article> element acts as a container for any section of a page that could stand alone and potentially be syndicated.

***Process & Design***

**Who is the Site For?**

Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to understand who your target audience is.

*Why People Visit YOUR Website*

Now that you know who your visitors are, you need to consider why they are coming. While some people will simply chance across your website, most will visit for a specific reason.

**Site Maps**

Now that you know what needs to appear on your site, you can start to organize the information into sections or pages.





