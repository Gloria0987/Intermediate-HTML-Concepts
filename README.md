# Intermediate-HTML-Concepts
A refresh of Emmet, SVG and Tables

# 1. SVG
“SVG” stands for “Scalable Vector Graphic”. Vector graphics are simply images defined by math, as opposed to traditional “raster graphics,” where your image is defined by a grid of pixels.

With raster graphics, the detail is limited to the size of that pixel grid. If you want to increase the size of the image (scale it), you have to increase the size of that grid. How do you decide what all those new pixels should look like? There’s no simple solution. Additionally, the larger the grid, the bigger your filesize grows.

With vector graphics on the other hand, there’s no grid. Instead, you have formulas for different shapes and lines. Since these are just formulas, it doesn’t matter how large or small you want them to appear–they can scale to any size you want, and it will have no effect on the quality or the size of the file.

SVGs have another interesting aspect to them: they’re defined using XML. XML (aka, “Extensible Markup Language”) is an HTML-like syntax which is used for lots of things, from APIs, to RSS, to spreadsheet and word editor software.

# Benefits of SVG
1. First, it means that it is *human-readable*.

If you were to open up a JPEG in a text editor, it would just look like gobbledygook. If you were to open up an SVG, however, it would look something like this:

![carbon](https://user-images.githubusercontent.com/48117356/188074626-5b4ab3f4-8bee-4406-8a76-6d1e57ddeae8.png)

2. *Interoperability* with HTML
This means one can put the above code directly in an HTML file, without any changes, and it should display the image. And because these can become elements in the DOM just like HTML elements, you can target them with CSS and create them using the [Element WebAPI](https://developer.mozilla.org/en-US/docs/Web/API/Element)
 you’ve already been using!
 
# Drawbacks of SVG
1.Extremely inefficient at storing complex image.

If your image is supposed to be photo-realistic, or it has fine detail or texture (“[grunge textures](https://unsplash.com/s/photos/grunge-texture)” are a great example), then SVGs are the wrong tool for the job.
