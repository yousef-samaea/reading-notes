***Mastering Markdown***

Markdown is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in, like # or *.

You can use Markdown most places around GitHub:

Gists
Comments in Issues and Pull Requests
Files with the .md or .markdown extension

**GitHub Flavored Markdown**
GitHub.com uses its own version of the Markdown syntax that provides an additional set of useful features, many of which make it easier to work with content on GitHub.com.

Note that some features of GitHub Flavored Markdown are only available in the descriptions and comments of Issues and Pull Requests. These include @mentions as well as references to SHA-1 hashes, Issues, and Pull Requests. Task Lists are also available in Gist comments and in Gist Markdown files.

**SHA references**
Any reference to a commit’s SHA-1 hash will be automatically converted into a link to that commit on GitHub.

***GitHub Pages***
GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website. You can see examples of GitHub Pages sites in the GitHub Pages examples collection.

You can host your site on GitHub's github.io domain or your own custom domain. For more information, see "Using a custom domain with GitHub Pages."

If your project site is published from a private or internal repository owned by an organization using GitHub Enterprise Cloud, you can manage access control for the site. For more information, see "Changing the visibility of your GitHub Pages site."

To get started, see "Creating a GitHub Pages site."

Organization owners can disable the publication of GitHub Pages sites from the organization's repositories. For more information, see "Managing the publication of GitHub Pages sites for your organization."
Development of the GitHub.com platform began on October 19, 2007.[60][61][62] The site was launched in April 2008 by Tom Preston-Werner, Chris Wanstrath, P. J. Hyett and Scott Chacon after it had been made available for a few months prior as a beta release.[63]

Projects on GitHub.com can be accessed and managed using the standard Git command-line interface; all standard Git commands work with it. GitHub.com also allows users to browse public repositories on the site. Multiple desktop clients and Git plugins are also available. The site provides social networking-like functions such as feeds, followers, wikis (using wiki software called Gollum) and a social network graph to display how developers work on their versions ("forks") of a repository and what fork (and branch within that fork) is newest.

Anyone can browse and download public repositories but only registered users can contribute content to repositories. With a registered user account, users are able to have discussions, manage repositories, submit contributions to others' repositories, and review changes to code. GitHub.com began offering unlimited private repositories at no cost in January 2019 (limited to three contributors per project). Previously, only public repositories were free.[64][65][66] On April 14, 2020, GitHub made "all of the core GitHub features" free for everyone, including "private repositories with unlimited collaborators".[67]

The fundamental software that underpins GitHub is Git itself, written by Linus Torvalds, creator of Linux. The additional software that provides the GitHub user interface was written using Ruby on Rails and Erlang by GitHub, Inc. developers Wanstrath,[68] Hyett, and Preston-Werner.

***Basic writing and formatting syntax***

**Create sophisticated formatting for your prose and code on GitHub with simple syntax.**
*Headings*
To create a heading, add one to six # symbols before your heading text. The number of # you use will determine the size of the heading.

# The largest heading
## The second largest heading
###### The smallest heading
*Styling text*
You can indicate emphasis with bold, italic, or strikethrough text.
*Quoting code*
You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted.
*Links*
You can create an inline link by wrapping link text in brackets [ ], and then wrapping the URL in parentheses ( ). You can also use the keyboard shortcut command + k to create a link.

This site was built using [GitHub Pages](https://pages.github.com/).


*Lists*
You can make an unordered list by preceding one or more lines of text with - or *.

- George Washington
- John Adams
- Thomas Jefferson
*Referencing issues and pull requests*
You can bring up a list of suggested issues and pull requests within the repository by typing #. Type the issue or pull request number or title to filter the list, and then press either tab or enter to complete the highlighted result.
*Ignoring Markdown formatting*
You can tell GitHub to ignore (or escape) Markdown formatting by using \ before the Markdown character.

Let's rename \*our-new-project\* to \*our-old-project\*.

