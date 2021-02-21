# Object-Oriented Programming, HTML Tables

***Domain Modeling***

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

**Model epic fails videos**

Imagine you've been tasked to build a program that models the popularity of epic fail videos. After months of painstaking research, you've determined that the two essential metrics for gauging popularity are an epic rating and whether or not the video has animals.

Since you'll be modeling the popularity of many types of videos—parkour epic fails, corgi epic fails, etc.you'll want to build self-contained objects with the same attributes and behaviors. That way, when you need to change the algorithm for determining popularity, the changes will be small and targeted.



As you read this article, type out and run all code samples you come across. Do not copy and paste. Writing out and testing your code will help you remember how to implement domain models in JavaScript later.

**Define a constructor and initialize properties**
To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an EpicFailVideo object.

As you can see, the constructor function is defined using a function expression. In other words, the variable EpicFailVideo is declared and then assigned a function with two parameters called epicRating and hasAnimals.

When the function is called, the data inside these parameters are stored inside the this.epicRating and this.hasAnimals properties respectively. Storing data within properties ensures any newly created object can access that data later.

After the constructor function definition, two objects are instantiated with the new keyword and their properties are initialized by calling the EpicFailVideo constructor function. After being instantiated and initialized, these objects are stored inside the parkourFail and corgiFail variables.

**Generate random numbers**

To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a Math.random() function for just this sort of occasion.

As you can see, methods can be added to a constructor function's prototype. Think of the prototype as an object's stunt double. Whenever a scene is too dangerous, you can substitute in the prototype to do the work while the object takes all the glory. More on how that works below.



EpicFailVideo's prototype is given a generateRandom method which is assigned a function with two parameters called min and max. The function uses both Math.floor and Math.random to calculate and return a random integer between min and max.

When parkourFail is asked to run the generateRandom() method, it searches through all of its own methods. When it doesn't find the generateRandom() method there, parkourFail then searches through all of the methods on its prototype object. When it finds the generateRandom() method on its prototype object, parkourFail calls the method, passing in 1 and 5 as the arguments. The generateRandom(1, 5) method runs and returns a random number between 1 and 5. The exact same process happens for corgiFail too.

While it certainly takes longer to locate a method on the prototype object, this technique is an established best practice in JavaScript. When a prototype is shared between two or more objects, like it is for parkourFail and corgiFail, those objects execute the same code when the generateRandom() method is called. And shared code means a running program consumes less memory which is important for devices like smart phones and tablets.

**Calculate daily Likes**

Popularity of a video is measured in Likes. And the formula for calculating Likes is the number of viewers times the percentage of viewers who'll Like a video. In other words, viewers times percentage.

To calculate the number of viewers per day, generate a random number between 10 and 30 and then multiply it by the epic rating of that video.

The dailyLikes() method on EpicFailVideo's prototype is assigned a function with no parameters. This method starts by defining two variables called viewers and percentage.

The viewers variable is assigned the value of this.generateRandom(10, 30) multiplied by this.epicRating. Using the this variable, methods can access any property or method on the same object that called the dailyLikes() method.

**Calculate weekly Likes**

In addition to modeling the daily Likes, your boss has asked you to model the weekly Likes too. Little does your boss know how easy it is to add behaviors to your domain model.

The weeklyLikes() method on EpicFailVideo's prototype is assigned a function with no parameters. This method starts by declaring a total variable that's initialized to 0.

The weeklyLikes() method proceeds to call this.dailyLikes() seven times and adds the returning number of Likes to total using the += operator. Afterwards, total is returned.

***Summary***

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

2. Model its attributes with a constructor function that defines and initializes properties.

3. Model its behaviors with small methods that focus on doing one job well.

4. Create instances using the new keyword followed by a call to a constructor function.

5. Store the newly created object in a variable so you can access its properties and methods from outside.

6. Use the this variable within methods so you can access the object's properties and methods from inside.


# TABLES

*There are several types of information that need to be displayed in a grid or table. For example: sports results, stock reports, train timetables*

*What's a Table?*

A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.

**Basic Table St ructure**

1. <table> :
The .<table> element is used to create a table. The contents of the table are written out row by row.

2. <tr> :
You indicate the start of each row using the opening <tr> tag. (The tr stands for table row.) It is followed by one or more <td> elements (one for each cell in that row).

 At the end of the row you use a closing </tr> tag.

3. <td> :
Each cell of a table is represented using a <td> element. (The td stands for table data.)

At the end of each cell you use a closing </td> tag.

**Table Headings**

*<th>*
The <th> element is used just like the <td> element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.)

Even if a cell has no content, you should still use a <td> or <th> element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example
shows an empty cell.)

Using <th> elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.

You can use the scope attribute on the <th> element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column.

**Long Tables**

There are three elements that help distinguish between the main content of the table and the first and last rows (which can contain different content).

These elements help people who use screen readers and also allow you to style these sections
in a different manner than the rest of the table (as you will see when you learn about CSS).

1. <thead> The headings of the table should sit inside the <thead> element.

2. <tbody> The body should sit inside the <tbody> element.

3. <tfoot> The footer belongs inside the <tfoot> element.

**Old Code: Width & Spacing**

There are some outdated attributes which you should not use on new websites. You may, however, come across some of them when looking at older code, so I will mention themhere. All of these attributes have been replaced by the use of CSS.

The width attribute was used on the opening <table> tag to indicate how wide that table should be and on some opening <th> and <td> tags to specify the width of individual cells. The value of this attribute is the width of the table or cell in pixels.

The columns in a table need to form a straight line, so you often only see the width attribute on the first row (and all subsequent rows would use that setting).

The opening <table> tag could also use the cellpadding attribute to add space inside each cell of the table, and the cellspacing attribute to create space between each cell of the table. The values for these attributes were given in pixels

***Summary***

1. A table is drawn out row by row. Each row is created with the <tr> element.

2. Inside each row there are a number of cells represented by the <td> element (or <th> if it is a header).

3. You can make cells of a table span more than one row or column using the rowspan and colspan attributes

4. For long tables you can split the table into a <thead>, <tbody>, and <tfoot>.

***FUNCTIONS, METHODS & OBJECTS***

**CREATE & ACCESS OBJECTS CONSTRUCTOR NOTATION**

To get a better idea of why you might want to create mult iple objects on the same page, here is an example that shows room availability in two hotels.

First, a constructor function defines a template for the setuation .

Next, two different instances of this type of hotel object are created. The first represents a hotel called Quay and the second a hotel called Park.

Having created instances of these objects, you can then access their properties and methods using the same dot notation that you use with all other objects.

**ADDING AND REMOVING PROPERTIES**

Once you have created an object (using literal or constructor notation), you can add new properties to it.

In this example, you can see that an instance of the hotel object is created using an object literal.

Immediately after t his, the hotel object is given two extra properties that show the facilities (whether or not it has a gym and/or a pool). These properties are given values that are Booleans (true or false).

Having added these properties to the object, you can access them just like any of the objects other properties. Here, they update the value of the cl ass attribute on their respective elements to show either a check mark or a cross mark.

To delete a property, you use the keyword delete, and then use dot notation to identify the property or method you want to remove from the object.

In this case, the booked property is removed from the object.

**RECAP: STORING DATA**

In JavaScript, data is represented using name/value pairs. To organize your data, you can use an array or object to group a set of related values. In arrays and objects the name is also known as a key.

If you want to access items via a property name or key, use an object (but note that each key in the object must be unique). If the order of the items is important, use an array.

**WHAT ARE BUILT-IN OBJECTS?**

Browsers come with a set of built-in objects that represent things like the browser window and the current web page shown in that window. These built-in objects act like a toolkit for creating interactive web pages.

**DATA TYPES REVISITED**

In JavaScript there are six data types: Five of them are described as simple (or primitive) data types. The sixth is the object (and is referred to as a complex data type).

***summary***

1. Functions allow you to group a set of related statements together that represent a single task.

2. Functions can take parameters (informatiorJ required to do their job) and may return a value.

3. An object is a series of variables and functions that represent something from the world around you.

4. In an object, variables are known as properties of the object; functions are known as methods of the object.

5. Web browsers implement objects that represent both the browser window and the document loaded into the browser window.

6. JavaScript also has several built-in objects such as String, Number, Math, and Date. Their properties and methods offer functionality that help you write scripts.

7. Arrays and objects can be used to create complex data sets (and both can contain the other).

