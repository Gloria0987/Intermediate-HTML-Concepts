# Intermediate-HTML-Concepts
A refresh of Emmet, SVG and Tables

# 1. SVG
“SVG” stands for “Scalable Vector Graphic”. Vector graphics are simply images defined by math, as opposed to traditional “raster graphics,” where your image is defined by a grid of pixels.

With raster graphics, the detail is limited to the size of that pixel grid. If you want to increase the size of the image (scale it), you have to increase the size of that grid. How do you decide what all those new pixels should look like? There’s no simple solution. Additionally, the larger the grid, the bigger your filesize grows.

With vector graphics on the other hand, there’s no grid. Instead, you have formulas for different shapes and lines. Since these are just formulas, it doesn’t matter how large or small you want them to appear–they can scale to any size you want, and it will have no effect on the quality or the size of the file.

SVGs have another interesting aspect to them: they’re defined using XML. XML (aka, “Extensible Markup Language”) is an HTML-like syntax which is used for lots of things, from APIs, to RSS, to spreadsheet and word editor software.

# Benefits of SVG
1.First, it means that it is *human-readable*.

If you were to open up a JPEG in a text editor, it would just look like gobbledygook. If you were to open up an SVG, however, it would look something like this:

![carbon](https://user-images.githubusercontent.com/48117356/188074626-5b4ab3f4-8bee-4406-8a76-6d1e57ddeae8.png)

2.*Interoperability* with HTML.

This means one can put the above code directly in an HTML file, without any changes, and it should display the image. And because these can become elements in the DOM just like HTML elements, you can target them with CSS and create them using the [Element WebAPI](https://developer.mozilla.org/en-US/docs/Web/API/Element) you’ve already been using!
 
# Drawbacks of SVG
1.Extremely inefficient at storing complex image.

If your image is supposed to be photo-realistic, or it has fine detail or texture (“[grunge textures](https://unsplash.com/s/photos/grunge-texture)” are a great example), then SVGs are the wrong tool for the job.

Typically, you will not want to create SVGs from scratch in your code. Most often, you will download the file or copy the code either from a website or from an image editor that can create them (Adobe Illustrator and Figma are two popular apps that can create SVGs). However, it’s pretty common to download an SVG and want to tweak or adjust it just a little bit, so knowing what all the bits and pieces are, and how they work is very useful.

1.**xmlns** - stands for “XML NameSpace”. This specifies what dialect of XML you’re using–in our case, that dialect is the SVG language spec. Without it, some browsers will not render your image or will render it incorrectly.

2.**viewBox** - defines the bounds of your SVG. When you have to define the positions of different points of the elements in your SVG, this is what that’s referencing. It also defines the aspect ratio and the origin of your SVG. So it’s doing quite a lot! Be sure to play around with different values in the example above to get a feel for how it affects the shapes.

3.**class**, **id** - these attributes function just like they do in HTML. Using these in SVGs allows you to easily target an element via CSS or JavaScript, or to reuse an element via the use element.

4.Elements such as**ircle,rect,path and text** defined by the SVG namespace. These are our basic building-blocks. Although you can make extremely complex images with SVG, they are mostly created with just a dozen or so of these basic elements.
