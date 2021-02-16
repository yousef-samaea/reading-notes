# HTML Links, JS Functions, and Intro to CSS Layout

# Links

*Links are the defining feature of the web because they allow you to move from one web page to another.*

**Writing Links:**

Links are created using the <a> element. Users can click on anything between the opening <a> tag and the closing </a> tag. You specify which page you want to link to using the href attribute.

.<a>:

Links are created using the <a> element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link.

Users can click on anything that appears between the opening <a> tag and the closing </a> tag and will be taken to the page specified in the href attribute.

When you link to a different website, the value of the href attribute will be the full web address for the site, which is known as an absolute URL.

**Linking to Other Pages on the Sa me Site:**

When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL.

If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file.

**Directory Structure:**

On larger websites it's a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as directories.

**Rela tive URLs:**

*Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files.*

When you are linking to a page on your own website, you do not need to specify the domain name. You can use relative URLs which are a shorthand way to tell the browser where a page is in relation to the current page.

This is especially helpful when creating a new website or learning about HTML because you can create links between pages when they are only on your personal computer (before you have got a domain name and uploaded them to the web).

**Rela tive Link Type:**


*Same Folder*

To link to a file in the same folder, just use the file name. (Nothing else is needed.)

*Child Folder*


For a child folder, use the name of the child folder, followed by a forward slash, then the file name.

*Grandchild Folder*

Use the name of the child folder, followed by a forward slash, then the name of the grandchild folder, followed by another forward slash, then the file name.

*Parent Folder*

Use ../ to indicate the folder above the current one, then follow it with the file name.

*GrandParent Folder*

Repeat the ../ to indicate that you want to go up two folders (rather than one), then follow it with the file name.

**Email Links:**

*mailto:*
To create a link that starts up the user's email program and addresses an email to a specified email address, you use the <a> element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the email to be sent to.

On the right you can see that an email link looks just like any other link but, when it is clicked on, the user's email program will open a new email message and address it to the person specified in the link.

**Summary:**

1. Links are created using the <a> element
2. The <a> element uses the href attribute to indicate the page you are linking to.
3. If you are linking to a page within your own site, it is best to use relative links rather than qualified URLs.
4. You can create links to open email programs with an email address in the "to" field.
5. You can use the id attribute to target elements within a page that can be linked to.

# Layout

**Key Concepts in Positioning El ements:**

*Building Blocks*

CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.

*Containing Elements*

If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

**Layout Grids**

Composition in any visual art (such as design, painting, or photography) is the placement or arrangement of visual elements — how they are organized on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web designers.

**CSS Frameworks**

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.

**Summary:**

1. <div> elements are often used as containing elements to group together sections of a page.

2. Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.

3. The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)

4. Pages can be fixed width or liquid (stretchy) layouts.

5. Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).

6. Grids help create professional and flexible designs.

7. CSS Frameworks provide rules for common tasks.

8. You can include multiple CSS files in one page.

# FUNCTIONS, METHODS & OBJECTS

*Browsers require very detailed instructions about what we want them to do. Therefore, complex scripts can run to hundreds (even thousands) of lines. Programmers use functions, methods, and objects to organize their code. This chapter is divided into three sections that introduce:*

1. FUNCTIONS & METHODS

2. OBJECTS

3. BUILT-IN OBJECTS

*WHAT IS A FUNCTION?*

Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of st atements).

**A BASIC FUNCTION:**

In this example, the user is shown a message at the top of the page. The message is held in an HTML element whose id attribute has a value of message. The message is going to be changed using JavaScript.

Before the closing </body> tag, you can see the link to the JavaScript file. The JavaScript file starts with a variable used to hold a new message, and is followed by a function ca lled updateMessage().

You do not need to worry about how this function works yet - you will learn about that over the next few pages. For the moment, it is just worth noting that inside the curly braces of the function are two statements.

# 6 Reasons for Pair Programming

1. *Greater efficiency:*
It is a common misconception that pair programming takes a lot longer and is less efficient. In reality, when two people focus on the same code base, it is easier to catch mistakes in the making. Research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging (let alone exposing users to a broken product). So, in the long-run, it’s often actually more efficient than two people working on separate features. When coming up with ideas and discussing solutions out loud, two programmers may come to a solution faster than one programmer on their own. Also, when the pair is stuck, both programmers can research the problem and reach a solution faster. Researches also identified pairing enhances technical skills, team communication, and even enjoyability of coding in the workplace.

2. *Engaged collaboration:*
When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone. It is harder to procrastinate or get off track when someone else is relying on you to complete the work. Popping open your Facebook timeline is just that less enticing when someone else is looking at your screen.

Another important aspect of learning to program is knowing when to ask for help. We advise our students to spend no more than fifteen minutes stuck on a problem before asking a teaching assistant or instructor for help. When developers pair program, they rely more on each other and can often find a solution together without needing to ask for additional help. Ultimately, this boosts overall confidence.

3. *Learning from fellow students:*
Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.

Often times, the developers in a pairing have different skill sets. If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area. The less experienced developer benefits from the experienced developer’s knowledge and guidance, and the latter benefits from explaining the topic in their own words, further solidifying their own understanding.

4. *Social skills:*
Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. Pair programming not only improves programming skills, but can also help programmers develop their interpersonal skills. When just grabbing the keyboard and taking over isn’t an option, getting good at finding the right words is a skill unto itself.

This has long-term career impacts. As much as employers want strong programmers, they know it’s essential to hire people who can work well with others.

5. *Job interview readiness:*
A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.

For most roles, the ability to work with and learn from others and stellar communication skills are as (or more!) important to a company than specific technical skills. Pair programming strengthens all of those skills.

6. *Work environment readiness:*
Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.

# the end.


