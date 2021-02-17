# Images, Color, Text

***Images***

*There are many reasons why you might want to add an image to a web page: you might want to include a logo, photograph, illustration, diagram, or chart.*

There are several things to consider when selecting and preparing images for your site, but taking time to get them right will make it look more attractive and professional. In this chapter you will learn how to:

1. Include an image in your web pages using HTML

2. Pick which image format to use

3. Show an image at the right size

4. Optimize an image for use on the web to make pages load faster

**Choosing Images for Your Site**

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.

Images can be used to set the tone for a site in less time than it takes to read a description. If you do not have photographs to use on your website, there are companies who sell stock images; these are images youpay to use (there is a list of stock photography websites below). Remember that all images are subject to copyright, and you can get in trouble for simply taking photographs from another website.If you have a page that shows several images (such as product photographs or members of a team) then putting them on a simple, consistent background helps them look better as a group.

**Images should:**

Be relevant, Convey information, Convey the right mood, Be instantly recognisable, Fit the color palette,

**Stock photos**

1. www.istockphoto.com

2. www.gettyimages.com

3. www.veer.com

4. www.sxc.hu

5. www.fotolia.com

*Storing Images on Your Site*

If you are building a site from scratch, it is good practice to create a folder for all of the images the site uses.

**Adding Images**

.<img>: images.html HTML To add an image into the page you need to use an <img> element. This is an empty element (which means there is zo closing tag). It must carry the following two attributes: src This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images

This provides a text description of the image which describes the image if you cannot see it.

**Summary**

1. The <img> element is used to add images to a web page.

2. You must always specify a src attribute to indicate the source of an image and an alt attribute to describe the content of an image.

3. You should save images at the size you will be using them on the web page and in the appropriate format.

4. Photographs are best saved as JPEGs; illustrations or logos that use flat colors are better saved as GIFs.

***Color***

*Color can really bring your pages to life.*

**Foreground Color**

*The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:*

1. *rgb values*

These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

2.*hex codes*

These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80

3. *color names*

There are 147 predefined color names that are recognized by browsers. For example: DarkCyan

**Example**

This example shows a pH scale to demonstrate the different ways that colors can be specified using CSS (using color names, hex codes, RGB, and HSL).

The rule for the <body> element sets a default color for all the text as well as the default background color for the page. Both use color names.

The rule for the <h1> element sets the color of the heading using a hex zode. There are two values for the background-color property of the <h1> element. The first provides a fallback color using a hex code and the second is an HSLA value for browsers that support this method.

Each paragraph is then shown in a different color to represent the varying levels of acidity or alkalinity, and these are specified using RGB values.

**Summary**

1. Color not only brings your s XX ite to life, but also helps convey the mood and evokes reactions.

2. There are three ways to specify colors in CSS: RGB values, hex codes, and color names.

3. Color pickers can help you find the color you want.

4. It is important to ensure that there is enough contrast between any text and the background color (otherwise people will not be able to read your content).

5. CSS3 has introduced an extra value for RGB colors to indicate opacity. It is known as RGBA.

6. CSS3 also allows you to specify colors as HSL values, with an optional opacity value. It is known as HSLA.

***Text***

The properties that allow you to control the appearance of text can be split into two groups:

1. Those that directly affect the font and its appearance (including the typeface, whether it is regular, bold or italic, and the size of the text)

2. Those that would have the same effect on text no matter what font you were using (including the color of text and the spacing between words and letters)

3. The formatting of your text can have a significant effect on how readable your pages are. As we look through these properties I will also give you some design tips on how to display your type.

*There are properties to control the choice of font, size, weight, style, and spacing.

*There is a limited choice of fonts that you can assume most people will have installed.*

*If you want to use a wider range of typefaces there are several options, but you need to have the right license to use them.*

*You can control the space between lines of text, individual letters, and words. Text can also be aligned to the left, right, center, or justified. It can also be indented.*

*You can use pseudo-classes to change the style of an element when a user hovers over or clicks on text, or when they have visited a link.*

***JPEG vs PNG vs GIF — which image format to use and when?***

There are hundreds of image formats available each with a specific use case. I bet most of us wouldn’t have come across 90% of the image formats listed on Wikipedia.
In this post, we would only be looking at the three most commonly used image formats in websites and mobile applications — JPEG, PNG and GIF. Several statistics reports, including the one from HTTP Archive, indicate that these 3 formats together comprise of more than 95% of all images loaded on websites. However, these 3 image formats have significant differences amongst themselves thus making each of them suitable for specific use cases. Understanding these major differences would help us deliver the best possible images to our website and mobile app users.


**TL;DR**

Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. Use GIF format for images that contain animations.

**Compression**

Almost all forms of data that we see on the internet — text, image, video etc. — are compressed to reduce the size of data and ensure faster transmission. Choosing the correct format and compression is a major factor that determines image size.

**Transparency**

In a simple form, transparency indicates something that is completely invisible. Logos and icons often need to be placed on backgrounds with variable colours. Hence it is desirable, that the background of these logos and icons is made transparent so that a single image can be used over multiple background variations.

*Colours*
There is a significant difference in the number of colours that can be supported by these 3 formats.

JPEG images can support around 16 million colours. This is what makes them suitable for storing images of natural scenes.

PNG images mainly have two modes — PNG8 and PNG24. PNG8 can support upto 256 colours whereas PNG24 can handle upto 16 million colours like a JPEG image. Use PNG8 for simple shapes with fewer colours and PNG24 for high quality, complex logos and shapes with rounded corners on a transparent background.

**Animation**

Animation, in this case, refers to any change or movement in the image. It doesn’t necessarily have to have frame rates like an animated video, but essentially a part or the entire image changes with time.

Of these 3 formats, only GIF supports animation. This capability makes GIF format suitable for delivering engaging ads and banners. Of late, with the advent of companies Tumblr, 9Gag, Giphy etc. the use of GIF format for memes has picked up.
