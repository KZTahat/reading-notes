 # Assorted Topics
 <!-- Chapter 16: “Images” (pp.406-427) -->
 ## Images
Controlling the size and alignment of your images using CSS keeps rules that affect the presentation of your page in the CSS and out of the HTML markup. You can control the size of an image using the width and height properties in CSS, just like you can for any other box. Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.You might think that your site is likely to have images of all different sizes, but a lot of sites use the same sized image across many of their pages.<br />
First you need to determine the sizes of images that will be used commonly throughout the site, then give each size a name.For example: (small, medium, larg) eWhere the ```<img>``` elements appear in the HTML, rather than using width and heightattributes you can use these names as values for the classattribute. In the CSS, you add selectors for each of the class names, then use the CSS width and heightproperties to control the image dimensions.<br />
- **Aligning Images using css**:<br />
    Rather than using the ```<img>``` element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:<br />
    1. The float property is added to the class that was created to represent the size of the image (such as the small class in our example).<br />
    2. New classes are created with names such as align-left or align-right to align the images to the left or right of the page. These class names are used in addition to classes that indicate the size of the image.<br />
- **Centering images Using Css**:<br />
    By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a blocklevel element using the displayproperty with a value of block. Once it has been made into a block-level element, there are two common ways in which you can horizontally center an image:<br />
    1. On the containing element, you can use the text-alignproperty with a value of center.
    2. On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.<br />
    You can specify class names that allow any element to be centered, in the same way that you can for the dimensions or alignment of images.<br />






[Home]( https://kztahat.github.io/reading-notes/)