***Basics of HTML, CSS & JS***

**Text**

When creating a web page, you add tags(known as markup) to the contents of thepage. These tags provide extra meaningand allow browsers to show users theappropriate structure for the page.

1. **Headings**

*HTML has six "levels" of headings:*

<h1> is used for main headings <h2> is used for subheadings If there are further sections under the subheadings then the <h3> element is used, and so on...
Browsers display the contents of

headings at different sizes. The contents of an <h1> element is the largest, and the contents of an <h6> element is the smallest. The exact size at which each browser shows the headings can vary slightly. Users can also adjust the size of text in their browser. You will see how to control the size of text, its color, and the fonts used when we come to look at CSS.

2. **paragraphs**

<p> To create a paragraph, surround the words that make up the paragraph with an opening <p> tag and closing  </p> tag. By default, a browser will show each paragraph on a new line with some space between it and any subsequent paragraphs.

3. **Bold & It alic**

<b> : 
By enclosing words in the tags <b> and </b> we can make characters appear bold. The <b> element also represents a section of text that would be presented in a visually different way (for example key words in a paragraph) although the use of the <b> element does not imply any additional meaning.

<i>: 
By enclosing words in the tags <i> and </i> we can make characters appear italic. The <i> element also represents a section of text that would be said in a different way from surrounding content — such as technical terms, names of ships, foreign words, thoughts, or other terms that would usually be italicized.

4. **Superscript & Subscript**

<sup>
The <sup> element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power

<sub>
The <sub> element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H20.

5. **Line Breaks & Horizontal Rules**

<br /> :
As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag <br />.

<hr />:
To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the <hr /> tag.

6. **St rong & Emph asis**

<strong>:
The use of the <strong> element indicates that its content has strong importance. For example, the words contained in this element might be said with strong emphasis. By default, browsers will show the contents of a <strong> element in bold.

<em>:
The <em> element indicates emphasis that subtly changes the meaning of a sentence. By default browsers will show the contents of an <em> element in italic.

7. **Quotations**

<blockquote>:
The <blockquote> element is used for longer quotes that take
up an entire paragraph. Note how the <p> element is still used inside the <blockquote>
element. Browsers tend to indent the contents of the <blockquote> element, however you should not use this element just to indent a piece of text — rather you should achieve this effect using CSS.

<q>:
The <q> element is used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the <q> element, however
Internet Explorer does not — therefore many people avoid using the <q> element. 

8. **Abbreviations & Acronyms**

<abbr>:
If you use an abbreviation or an acronym, then the <abbr> element can be used. A title attribute on the opening tag is used to specify the full term.

9. **Citations & Definitions**

<cite>:
When you are referencing a piece of work such as a book, film or research paper, the <cite> element can be used to indicate where the citation is from. In HTML5, <cite> should not really be used for a person's name — but it was allowed i  HTML 4, so most people are likely to continue to use it.

<dfn>:
The first time you explain some new terminology (perhaps an academic concept or some jargon) in a document, it is known as the defining instance of it.

10. **Auth or Details**

<address>:
The <address> element has quite a specific use: to contain contact details for the author of the page. It can contain a physical address, but it does not have to. For example, it may also contain a phone number or email address.

11. **Ch anges to Content**

<ins> & <del>:
The <ins> element can be used to show content that has been inserted into a document, while the <del> element can show text that has been deleted from it.

<s>:
The <s> element indicates something that is no longer accurate or relevant (but that should not be deleted). Visually the content of an <s> element will usually be displayed with a line through the center.


***IntroducingCSS***

**Understanding CSS: Thinking Insi de the Box**

*The key to understanding how CSS works is to imagine that there is an invisible box around every HTML element.*

*CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented.*

**CSS Associates Style rules with HT ML elements**

CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.

**CSS Properties Affect How El ements Are Dis played**

CSS declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

***Usi ng External CSS***

<link>:
The <link> element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the <head> element. It should use three attributes:

1. href :
This specifies the path to the CSS file (which is often placed in a folder called css or styles).

2. type : 
This attribute specifies the type of document being linked to. The value should be text/css.

3. rel : 
This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file. 


***Usi ng Internal***

.<style>
You can also include CSS rules within an HTML page by placing them inside a <style> element, which usually sits inside the <head> element of the page. The <style> element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/ css.

When building a site with more than one page, you should use an external CSS style sheet. This:

1.Allows all pages to use the same style rules (rather than repeating them in each page).
2. Keeps the content separate from how the page looks.
3. Means you can change the styles used across all pages by altering just one file (rather than each individual page). 


***BASIC JAVASCRIPT INSTRUCTIONS***

A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.

**COMMENTS**

You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.

**WHAT IS A VARIABLE?**

A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variables.

*A variable is a good name for this concept because the data stored in a variable can change (or vary) each time a script runs.*

**DATA TYPES**

JavaScript distinguishes between numbers, strings, and true or false values known as Booleans.

Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one).


***DECISIONS & LOOPS***

**comparison operators javascript**

Comparison operators are used in logical statements to determine equality or difference between variables or values. 

**Logical Operators**

Logical operators are used to determine the logic between variables or values.

**Conditional (Ternary) Operator**

JavaScript also contains a conditional operator that assigns a value to a variable based on some condition.



**JavaScript if else and else if**

Conditional Statements
Very often when you write code, you want to perform different actions for different decisions.

You can use conditional statements in your code to do this.

In JavaScript we have the following conditional statements:

1. Use if to specify a block of code to be executed, if a specified condition is true
2. Use else to specify a block of code to be executed, if the same condition is false
3. Use else if to specify a new condition to test, if the first condition is false
4. Use switch to specify many alternative blocks of code to be executed

*Use the if statement to specify a block of JavaScript code to be executed if a condition is true.*

*Use the else statement to specify a block of code to be executed if the condition is false.*

*Use the else if statement to specify a new condition if the first condition is false.*


**the end**



