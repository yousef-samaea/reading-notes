#Problem Domain, Objects, and the DOM

**WHAT IS AN OBJECT?**

Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.

*Programmers use a lot of name/value pairs:*

• HTML uses attribute names and values.

• CSS uses property names and values.

In JavaScript:
• Variables have a name and you can assign them a value of a string, number, or Boolean.

• Arrays have a name and a group of values. (Each item in an array is a name/value pair because it
has an index number and a value.)

• Named functions have a name and value that is a set of statements to run if the function is called.

• Objects consist of a set of name/value pairs (but the names are referred to as keys).

***DOCUMENT OBJECT MODEL***

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.


*MAKING A MODEL OF THE HTML PAGE*

When the browser loads a web page, it creates a model of the page in memory.

The DOM specifies the way in which the browser should structure this model using a DOM tree.

The DOM is called an object model because the model (the DOM tree) is made of objects.

Each object represents a different part of the page loaded in the browser window.

**THE DOM TREE IS A MODEL OF A WEB PAGE**

As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes.

Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in the browser.

*ATTRIBUTE NODES*

The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree.

*TEXT NODES*

Once you have accessed an element node, you can then reach the text within that element. This is stored in its own text node.

**What is the DOM?**

The DOM is a W3C (World Wide Web Consortium) standard.

The DOM defines a standard for accessing documents:

"The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document."

The W3C DOM standard is separated into 3 different parts:

Core DOM - standard model for all document types

XML DOM - standard model for XML documents

HTML DOM - standard model for HTML documents

**What is the HTML DOM?**

The HTML DOM is a standard object model and programming interface for HTML. It defines:

The HTML elements as objects

The properties of all HTML elements

The methods to access all HTML elements

The events for all HTML elements

*The DOM Programming Interface*

The HTML DOM can be accessed with JavaScript (and with other programming languages).

In the DOM, all HTML elements are defined as objects.

The programming interface is the properties and methods of each object.

A property is a value that you can get or set (like changing the content of an HTML element).

A method is an action you can do (like add or deleting an HTML element).

*The HTML DOM Document Object*

The document object represents your web page.

If you want to access any element in an HTML page, you always start with accessing the document object.

Below are some examples of how you can use the document object to access and manipulate HTML.

*Finding HTML Elements*

1. Finding HTML elements by id
2. Finding HTML elements by tag name
3. Finding HTML elements by class name
3. Finding HTML elements by CSS selectors
4. Finding HTML elements by HTML object collections

The HTML DOM allows JavaScript to change the style of HTML elements.

Changing HTML Style To change the style of an HTML element, use this syntax:

document.getElementById(id).style.property = new style

**summare**

The browser represents the page using a DOM tree. DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.

You can select element nodes by their id or cl ass attributes, by tag name, or using CSS selector syntax.

Whenever a DOM query can return more than onenode, it will always return a Nadel i st.

From an element node, you can access and update its content using properties such as textContent and i nnerHTML or using DOM manipulation techniques.

An element node can contain multiple text nodes and child elements that are siblings of each other.

In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).

Browsers offer tools for viewing the DOM tree .






