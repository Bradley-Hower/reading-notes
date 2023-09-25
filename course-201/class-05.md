# *Course 201, Entry 5: Images, Color, Text*

## HTML Media

Adding images to a web page brings a lot more life. It is important however to implement image content correctly for accessibility and usability to all.

### Alt Attribute

The `alt` attribute (accessible link text) describes what the image is of and perhaps some context. Detail is helpful. This attribute has a few meaningful purposes.

One, if the page can not fully load due to a poor or slow connection, the user can at least get a sense of what was to be there. This can be a meaningful time-saver. If the user decides based on what they were looking for that the image is not meaningful to them, they don't have to continue to wait for the computer to download the remaining content.

A second reason for the alt attribute is accessibility. Persons with a vision disability might heavily rely on these alt texts to get a sense of the content via a screen reader. To improve access to these folks, it is important to have alt attributes with quality describers.

Next, search engines use alt text to populate their search results.

Some users purposely turn off images to save on data costs or to focus.

And lastly, if all else fails, some information will get to the user. If an image becomes corrupted or the source link to the image breaks (hopefully not applicable as you should always host your images), it is good to be able to rely on some backup so that there isn't a complete void where there was to be an image.

Proper alt scribing for specific parts:

Content - Write a quality describer if the image is especially relevant. If your page also holds text, it is even better to describe the image in the text and tie it in contextually. Try to avoid redundancy in the alt attribute with the article text.

Decoration - Alt attributes for these are quite pointless. When possible, CSS is preferred. But if you must use an image and it is purely decorative, then keep the alt attribute blank.

Link - Links still need describers. In the case where a link is also an image, the describer can either be in the anchor tags title or the image's alt attribute. Consider the context.

Text - Avoid putting text into images. Use CSS whenever possible. If it can't be done due to artistic characteristics, put the image text as the alt attribute.

### Figures

With screen readers, it becomes difficult for the software to know what figure caption is tied to which content. This can produce unpredictable and confusing outputs. Instead, using the `<figure>` and `<figurecaption>` tags makes this very clear.

### Image Types

Image and video elements are known as **replaced elements**. Meaning, the element's size is determined by the source content. To help avoid the annoyances of moving text caused by this displacement when the image is loading, set an image height and width, even if it's the same as the source (it should be).

Image types:

**APNG** - Animated clips. Lossless. So-so performance.

**AVIF** - Animated and stills. Animated is not yet supported in Firefox. Royalty-free image format. Best compression. Higher color depths. Does not support progressive rendering.

**GIF** - Animated and stills. Strong browser support. Quality is lacking.

**JPEG** - Images. Strong browser support. Good for lossy compression. Not the best compression. Not good for reproducibility.

**PNG** - Images. Strong browser support. Good compression and reproduction, but not the best.

**SVG** - Vector images. Strong browser support.

**WebP** - Animated and stills. Great compression. Higher color depths.

Which is the best? The type of picture or animated clip is not significant. Screenshots, photos, animated clips, or art, the answers are all the same. If you want Firefox support or to use large files, WebP. Otherwise, AVIF. For a fallback on still pictures, PNG. The fallback for an animated clip is GIF. To implement a fallback, use the `<picture>` tag and have your two sources, in order of priority. A third source can be added to the source attribute in the image tag, the image tag being third, after the prior two source tags.

```
<picture>
  <source srcset="bouncingball.avif" type="image/AVIF" />
  <source srcset="bouncingball.webp" type="image/WebP" />
  <img
    src="bouncingball.gif"
    width="900"
    height="500"
    alt="Clip of 3D animated red ball bouncing" />
</picture>
```

What is the difference between a GIF image and an SVG image?

A gif image is an old animated clip format. It is of relatively lower quality. An SVG image is a vector image. What is a vector image? It is an image which is generated strictly by coordinates. SVG is great for graphical images.

#### Garbage Image Formats

The following image formats should never be used to due a lack of support and lower image quality: BMP, ICO, and TIFF.

## CSS - Color and Typeface
Color and typeface add a lot of character to a page. A lot. What are the ways to implement such?

### Color
When speaking of color, there are two primary properties. The text color (foreground) and the background color. The text color gives all the ASCII characters color. The background color is what colors the element that the text resides in.

If one were to start coloring a website, the person should first pick a nice set of colors that have complementary contrasts, 2-4 colors are sufficient. It is important to ensure these colors can be seen by all. Thus, using Lighthouse analysis can assist. Next, chose a dominant color to color the major elements, the big ones. Next, choose the secondary color, which will color the other elements. These elements should be something more stationary, such as banners or navigation. The last color is good for accenting and is optional. It can be used to color borders and perhaps text. A secondary accent color can also fill this role.

### Typeface

Typeface is what dictates the styling and layout of text. There are various ways to change the style.

Font. What is there to consider? When choosing a font via the `font-family` property, it is important to try to choose something that is reliably found on other machines, *web safe fonts*. Otherwise, the browser default will take over. Font-family allows use to stack font styles in case a font style is not present on the user's computer. [Cssfontstack.com](https://www.cssfontstack.com/) is a great resource to know what fonts are supported across macOS and Windows. Consider stacking fonts in order of priority in case of failure.

The five generic font names:

Predictable Output
+ Serif
+ Sans-serif
+ Monospace

Unpredictable Output
+ Cursive
+ Fantasy

**font-size** - commonly expressed as `px`, `em`, and `rem`. The `px` unit scales the size by height in pixels. The `em` unit sets it relative to the parent element. And the `rem` unit is similar to `em` except the reference is the root element. The standard font-size is 16px. The h1 element has a size of 2em or 32px.

**font-weight** - sets font boldness. Can be set as normal, bold, lighter or bolder (relative to the parent element), and numerically between 100 and 900.

**font-style** - normal, italic, and oblique (simulated italic).

**text-transform** - none, uppercase, lowercase, capitalize, full-width.

**letter-spacing** - sets spacing around letters.

**word-spacing** - sets spacing around words.

To add spacing to an h1 element, other than letter spacing described above, alternatively, spacing can be achieved by setting `text-transform` to full-width so as to fill the element. Another option is to use the `font-stretch` property.

## Things I want to know more about
Having a detailed list of useful and generally not useful font styling properties would be nice. I see there are a lot that are very specific or make tweaks that are generally not even desirable.
