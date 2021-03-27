# advanced web development
at this webpage I will tell you about what I have learnt today about html, css, and javascript.

**html**

**forms**

*a set of elements used to collect data from users.*

1. the search box is considered to be a form.

2. when signing up or reistering as a member of a website or shopping online users fills forms.

3. data is sent from forms to server as name/value pairs

**form controll**

*methods to collect data from user on the website:*

*adding text*

text input: for single line text such as email or names or phone number.

password input: like the single line text box but the entered character will appear as stars.

text area: to enter multi-line text such as comments and messages.

*making choices*

radio buttons: to let the user select only one option from a group of options
checkboxes: to let the user select or unselect any number of the givin options
drop-down boxes: to let a user choose an option from a drop-down menu.

upoadimg files: to let the user to upload files from his pc to the website

*submitting forms*

submit button: a button at the end of the form, used to submit data from the form to another web page.

image button: like the submit buttons but instead of the button there is an image of your choice.

**syntax:**

form controlls live inside <form> element:

<form action="url for the page that recieves data" method="get/post">form controlls live here</form>

use post method for: file uploading or input is very long or sending sensitive data or to change data from database.

use get method for: search boxes or short text input or retrieving data from the server. text input: <input type="text" name="the input name" maxlength="maximum number of character to enter" />
**password input:** <input type="password" name="the input name" maxlength="maximum number of character to enter" />

**text area:** <textarea name="the input name" cols="width of box" rows="height of box"></textarea>

**radio button:**<input type="radio" name="" value="value to be sent" /> put the option here

c**heckbox:**<input type="checkbox" name=" " value=" " checked="checked" /> put the option here the check attributes indicate that this option is selected by default.
drop down list box:

<select name="name of the input">
<option value=" ">put the option here</option>
<option value=" ">put the option here</option>
<option value=" ">put the option here</option>
</select>

**file input:** <input type="file" name="" />

**submit button:** <input type="submit" name=" " value="text on the button" />

**image button:** <input type="image" src="image path or url" width=" " height=" " />

**l**abel:** use the <label> element to describe the options or describe what to input.
fieldset: use the <fieldset> element to group related form controls with <legend> which contains a generic describtion for them.

***css***

**lists**

*bullet points styling*

1. unordred list: use the property list-style-type with none or disc or circle or square to specify the shape of the points.

2. ordered lists: use the property list-style-type with decimal or decimal-leading-zero or lower-alpha or upper-alpha or lower-roman or upper-roman to specify the pattern.

You can specify an image to replace the bullet point using list-style-image:url("path") property.

to let the marker appear inside or outside the block of text use list-style-position with inside or outside as a value

list shorthand: you can use list-style property with markers' style, image and position properties as values in any order.


**styling tables**

1. use the property empty-cells in <table> with show or hide or inherit to specify whether or not empty cells border be shown.

2. use the property border-spacing:horizontalSpacing virticalSpacing in <table> to specify distance between adjacent cells. horizontalSpacing and verticalSpacing are in numbers(usually px).

3. use the property border-collapse: collapse in <table> to let borders collapse into a single border where possible.

4. use the property border-collapse: separate in <table> to cancell border-collapse: collapse effect.

**styling forms**

**styling submit buttons** you can use most of the properties of tyling text input to style submit button such as font-size,color,background-color,border,border-radius,and the :hover pseudo-class to indicates whats happening when hover over the submit button.

**styling fieldsets & legends**you can set width,border,border-redius,padding,background-color for fieldset and you can set width,border,border-redius,padding,background-color,color,text-align,text-transform for the legend.

**Cursor styles**

use cursor property to control the shape of mouse cursor that should be displayed to users, by using one of the following values: auto,crosshair,default,pointer,move,text,wait,help,url(image path) where each value have a different shape for cursor.

**JavaScript**

*Events*

Events are actions that happen in the webpage (the browser or the user does it). the browser detects this events and it can be used to execute a JavaScript code (mostly using DOM to update the page).

*types of events:*

UI events: happens when the user do something with the browser interface: load, unload, error, resize, scroll.

keybord events:when the user use the keyboard: keypress, keydown(hold on a key), keyup(release a key).

mouse events: when a user interact with a mouse,trackpad,touchscreen: click,dblclick,mousedown(hold mouse button),mouseup(release mouse button),mousemove,mouseover(hover),mouseout(pointer get out of an element).

focus events: when an element is ready to be interacted it sayed to be in focus: focus/focusin(when element gain focus),blur/focusout(when element loses focus)

form events: when interacting with a form element: input(in textarea),change(changing an option),submit,reset,cut,copy,paste,select.

mutation events: when the DOM structure is changed by a script: DOMSubtreeModified,DOMNodelnserted,DOMNodeRemoved,OOMNodelnsertedlntoDocument,DOMNodeRemovedFromOocument

event handling: first select the element node that you then bind it with a suitable event then specify the code that will run when the event occure.

**ways of binding event to an element:**

1. html event handler: attributes in element tag with the same name of the desired event with a value of the function name.

2. traditional DOM event handlers: can attach only a single function to any event. elementNode.onevent = functionName;

3. DOM level 2 event listeners: allow one event to trigger multiple functions.
elementNode.addEventListener('event',functionName [, Boolean]);




