# Lists

*There are lots of occasions when we need to use lists. HTML provides us with three different types:*

1. Ordered lists are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.

2. Unordered lists are lists that begin with a bullet point (rather than characters that indicate order).

3. Definition lists are made up of a set of terms along with the definitions for each of those terms.

**Ordered Lists**

.<ol>: The ordered list is created with the <ol> element.

.<li>:
Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The li stands for list item.)

**Unordered lists**

.<ul>:
The unordered list is created with the <ul> element.

.<li>:
Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The li stands for list item.)

**Definition Lists**

.<dl>:
The definition list is created with the <dl> element and usually consists of a series of terms and their definitions. Inside the <dl> element you will usually see pairs of <dt> and <dd> elements.

.<dt>:
This is used to contain the term being defined (the definition term).

.<dd>:
This is used to contain the definition. Sometimes you might see a list where there are two terms used for the same definition or two different definitions for the same term.

**Nested lists**

You can put a second list inside an <li> element to create a sublist or nested list. Browsers display nested lists indented further than the parent list. In nested unordered lists, the browser will usually change the style of the bullet point too

***Summary***

1.There are three types of HTML lists: ordered, unordered, and definition.

2. Ordered lists use numbers.

3. Unordered lists use bullets.

4. Definition lists are used to define terminology.

5. Lists can be nested inside one another.

# Boxes

*At the beginning of this section on CSS, you saw how CSS treats each HTMLe lement as if it lives in its own box.*

You can set several properties that affect the appearance of these boxes. In this chapter you will see how to:

1. control the dimensions of your boxes

2. Create borders around boxes

3. Set margins and padding for boxes

4. Show and hide boxes

**box dimensions** : *width, height*

By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.

The most popular ways to specify the size of a box are to use pixels, percentages, or ems. Traditionally, pixels have been the most popular method because they allow designers to accurately control their size.

When you use percentages, the size of the box is relative to the size of the browser window or, if the box is encased within another box, it is a percentage of the size of the containing box.

When you use ems, the size of the box is based on the size of text within it. Designers have recently started to use percentages and ems more for measurements as they try to create designs that are flexible across devices which have different-sized screens.

In the example on the right, you can see that a containing <div> element is used which is 300 pixels wide by 300 pixels high. Inside of this is a paragraph that is 75% of the width and height of the containing element. This means that the size of the paragraph is 225 pixels wide by 225 pixels high.

**Limiting Width** : *min-width, max-width*

Some page designs expand and shrink to fit the size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.

**limiting Height** : *min-height, max-height*

In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it. This is achieved using the min-height and max-height properties.

The example on this page demonstrates these properties in action. It also shows you what happens when the content of the box takes up more space than the size specified for the box.

If the box is not big enough to hold the content, and the content expands outside the box it can look very messy. To control what happens when there is not enough space for the content of a box, you can use the overflow property, which is discussed on the next page.

**Overflowing Content** : *overflow*

*The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:*

1. hidden : This property simply hides any extra content that does not fit in the box

2. scroll :  This property adds a scrollbar to the box so that users can scroll to see the missing content. On the left, you can see two boxes whose contents expand beyond their set dimensions. The first example has the overflow property with a value of hidden. The second example has the overflow property with a value of scroll.

**Article Width** : *border-width*

The border-width property is used to control the width of a border. The value of this property can either be given in pixels or using one of the following values:

thin,medium,thick

**Border Style** : *border-style*

*You can control the style of a border using the border-style property. This property can take the following values:*

1. *solid* a single solid line

2. *dotte*d a series of square dots (if your border is 2px wide, then the dots are 2px squared with a 2px gap between each dot)

3. *dashed* a series of short lines

4. *double* two solid lines (the value of the border-width property creates the sum of the two lines)

5. *groove* appears to be carved into the page

6. *ridge* appears to stick out from the page

7. *inset* appears embedded into the page

8. *outset* looks like it is coming out of the screen

**Shorthand** : *border*

The border property allows you to specify the width, style and color of a border in one property (and the values should be coded in that specific order).

# BASIC JAVASCRIPT INSTRUCTIONS

**ARRAYS**

An array is a special type of variable. It doesn't just store one value; it stores a list of values.

You should consider using an array whenever you are working with a list or a set of values that are related to each other.

Arrays are especially helpful when you do not know how many items a list will contain because, when you create the array, you do not need to specify how many values it will hold.

**CREATING AN ARRAY**

*You create an array and give it a name just like you would any other variable (using the var keyword followed by the name of the array).*

The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. The values in the array do not need to be the same data type, so you can store a string, a number and a Boolean all in the same array.

**VALUES IN ARRAYS**

*Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one)*

*NUMBERING ITEMS IN AN ARRAY* Each item in an array is automatically given a number called an index. This can be used to access specific items in the array.

*ACCESSING ITEMS IN AN ARRAY* To retrieve the third item on the list, the array name is specified along with the index number in square brackets.

*NUMBER OF ITEMS IN AN ARRAY* Each array has a property called length, which holds the number of items in the array.

# JavaScript if else and else if

**Conditional Statements**

Very often when you write code, you want to perform different actions for different decisions.

You can use conditional statements in your code to do this.

In JavaScript we have the following conditional statements:

Use if to specify a block of code to be executed, if a specified condition is true 

Use else to specify a block of code to be executed, if the same condition is false

Use else if to specify a new condition to test, if the first condition is false

Use switch to specify many alternative blocks of code to be executed

***switch statement***

*Use the switch statement to select one of many code blocks to be executed.*

his is how it works:

1. The switch expression is evaluated once.

2. The value of the expression is compared with the values of each case.

3. If there is a match, the associated block of code is executed .

4. If there is no match, the default code block is executed.

*USING SWITCH STATEMENTS*

In this example, the purpose of the switch statement is to present the user with a different message depending on which level they are at. The message is stored in a variable called msg.

The variable called l eve 1 contains a number indicating which level the user is on. This is then used as the switch value. (The switch value could also be an expression.)

**TYPE COERCION & WEAK TYPING**

If you use a data type JavaScript did not expect, it tries to make sense of the operation rather than report an error.

JavaScript can convert data types behind the scenes to complete an operation. This is known as type coercion. For example, a string 'l ' could be converted to a number 1 in the following expression:(' 1' > 0). As a result, the above expression would evaluate to true.

JavaScript is said to use weak typing because the data type for a value can change. Some other languages require that you specify what data type each variable will be. They are said to use strong typing.

**TRUTHY & FALSY VALUES**

*Due to type coercion, every value in JavaScript can be treated as if it were true or false; and this has some interesting side effects.*

*Falsy* values are treated as if they are fa 1 se. The table to the left shows a hi ghScore variable with a series of va lues, all of which are falsy.

*Truthy* values are treated as if they are true. Almost everything that is not in the falsy table can be treated as if it were true.

*SHORT CIRCUIT VALUES*

Logical operators are processed left to right. They short-circuit (stop) as soon as they have a result - but they return the value that stopped the processing (not necessarily true or fa 1 se).

**JavaScript Loops**

*Loops are handy, if you want to run the same code over and over again, each time with a different value.*

*Different Kinds of Loops*

JavaScript supports different kinds of loops:

for - loops through a block of code a number of times

for/in - loops through the properties of an object

for/of - loops through the values of an iterable object

while - loops through a block of code while a specified condition is true

do/while - also loops through a block of code while a specified condition is true

*KEY LOOP CONCEPTS*

Here are three points to consider when you are working with loops. Each is illustrated in examples on the following three pages.

*break* This keyword causes the termination of the loop and tells the interpreter to go onto the next statement of code outside of the loop. (You may also see it used in functions.)

*continue* This keyword te lls the interpreter to continue with the current iteration, and then check the condition again. (If it is true, the code runs again.)

*LOOPS & ARRAYS* Loops are very helpful when dealing with arrays if you want to run the same code for each item in the array.








