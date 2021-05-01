# HTML Images; CSS Color & Text
<!-- Chapter 5: “Images” (pp.94-125) -->
## Images
A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.<br />
Images can be used to set the tone for a site in less time than it takes to read a description. If you do not have photographs to use on your website, there are companies who sell stock images; these are images you pay to use. Remember that some images are subject to copyright, and you can get in trouble for simply taking photographs from another website. If you have a page that shows several images (such as product photographs or members of a team) then putting them on a simple, consistent background helps them look better as a group.<br />
As a website grows, keeping images in a separate folder helps you understand how the site is organized. you can store the files on a website; we can store all of the images in a folder called images.On a big site you might like to add subfolders inside the imagesfolder. For example, images such as logos and buttons might sit in a folder called interface, product photographs might sit in a page called products, and images related to news might live in a folder called news.<br />
- Adding Images:<br />
To add an image into the page 
you need to use an ```<img>``` element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:<br />
    - src:<br />
        This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images. 
    - alt:<br />
        This provides a text description of the image which describes the image if you cannot see it.
    - title:(Optional)<br />
    You can also use the title attribute with the ```<img>``` element to provide additional information about the image. Most browsers will display the content of this attribute in a tootip when the user hovers over the image.
- Where to Place Images in Your Code:<br />
Where an image is placed in the code will affect how it is displayed. Here are three examples of image placement that produce different results:<br />
    1. before a paragraphThe paragraph starts on a new line after the image.
    2. inside the start of a paragraphThe first row of text aligns with the bottom of the image.
    3. in the middle of a paragraphThe image is placed between the words of the paragraph that it appears in.
<br />
- Three Rules for Creating Images<br />
There are three rules to remember when you are creating images for your website which are summarized below:<br />
    1. Save images in the right format:<br />
    Websites mainly use images in jpeg, gif, or png format. If you choose the wrong image format then your image might not look as sharp as it should and can make the web page slower to load.
    2. Save images at the right size:<br />
    You should save the image at the same width and height it will appear on the website. If the image is smaller than the width or height that you have specified, the image can be distorted and stretched. If the image is larger than the width and height if you have specified, the image will take longer to display on the page.
    3. Use the correct resolution:<br />
    Computer screens are made up of dots known as pixels. Images used on the web are also made up of tiny dots. Resolution refers to the number of dots per inch, and most computer screens only show web pages at 72 pixels per inch. So saving images at a higher resolution results in images that are larger than necessary and take longer to download.
<br />
<!-- Chapter 11: “Color” (pp.246-263) -->
## Color
The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:<br />
  - **RGB values** These express colors in terms of how much red, green and blue are used to make it up. *For example: rgb(100,100,90)*.<br />
  - **HEX codes** These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. *For example: #ee3e80*.<br />
  - **color names** There are 147 predefined color names that are recognized by browsers. *For example: DarkCyan*.<br />

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names. If you do not specify a background color, then the background is transparent.By default, most browser windows have a white background, but browser users can set a background color for their windows, so if you want to be sure that the background is white you can use the background-color property on the <body> element.<br />


- CSS introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5 is 50% opacity and 0.15 is 15% opacity). This value is known as an alpha value and is a number between 0.0 and 1.0(so a value of 0.5 is 50% opacity and 0.15 is 15% opacity). The rgba value will only affect the element on which it is applied (not child elements). The hsl color property has been introduced in CSS3 as an alternative way to specify colors. The value of the property starts with the letters hsl, followed by individual values inside parentheses for:<br />
  - **HUE**: This is expressed as an angle (between 0 and 360 degrees).<br />
  - **saturation**: This is expressed as a percentage.<br />
  - **lightness**: This is expressed as a percentage with 0% being white, 50% being normal, and 100% being black.The hsla color property allows you to specify color properties     using hue, saturation, and lightness as above, and adds a fourth value which represents transparency (just like   the rgbaproperty). which is:<br />
  - **AlPHA**: This is expressed as a number between 0 and 1.0. For example, 0.5 represents 50% transparency, and 0.75represents 75% transparency.
  <br />
  

[Home]( https://kztahat.github.io/reading-notes/)